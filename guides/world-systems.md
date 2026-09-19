# World systems

This guide covers particles, the sun, skyboxes, time of day, reflection, fog,
bloom, and weather. `Engine` advances built-in systems; game code owns policy
such as day/night state transitions.

## Frame order

1. Sun orbit advances with simulation time.
2. Physics and particles advance.
3. `GameLogic.update` changes weather and time-of-day state.
4. The renderer draws shadows, lit objects, transparent objects, particles,
   the skybox, bloom, and GUI.

Use the `dt` passed to `GameLogic.update` for gameplay transitions. It already
includes simulation time scaling.

## Particles

Every scene owns one `ParticleSystem`. Emitters are pooled and GPU-instanced:

```java
ParticleConfig rainConfig = new ParticleConfig()
        .setMaxParticles(10000)
        .setLifetime(2f)
        .setEmissionRate(2500f)
        .setScale(0.03f, 0.8f, 0.03f)
        .setMovementDirection(0f, -1f, 0f)
        .setTransparency(0.65f)
        .setBillboardMode(ParticleBillboardMode.BILLBOARD);

ParticleEmitter rain = scene.particles().createEmitter("rain", rainConfig)
        .setSpawnArea(40f, 0f, 40f)
        .setEnabled(false);
```

Use `FACE_UP` for ground fog or decals and `ROTATE_TO_CAMERA` for upright
sprites that turn around world Y. Keep model variants limited; each mesh group
requires a separate instanced draw.

## Sun

```java
scene.sun()
        .setDirection(-0.4f, -1f, -0.2f)
        .setColor(1f, 0.94f, 0.82f)
        .setIntensity(1.2f)
        .setShadows(true);
```

Directions are normalized automatically. Orbital motion uses radians per second
and simulation time:

```java
scene.sun().setOrbit(0f, 1f, 0f, 0.08f);
```

`stopOrbit()` freezes the current direction. Orbiting pauses with simulation.

## Skybox

Scenes start with a procedural skybox. Rebuild it with:

```java
scene.setSkyColors(
        new Vector3f(0.35f, 0.50f, 0.75f),
        new Vector3f(0.08f, 0.08f, 0.12f));
```

Authored cube-map faces use `Skybox.fromFiles(right, left, top, bottom, front,
back)` and `scene.setSkybox(...)`. The skybox is both the background and the
environment sampled by reflective PBR materials.

## Time of day

Time of day is an application-level state machine. Interpolate sky, sun, and
exposure together:

```java
float smooth = progress * progress * (3f - 2f * progress);
scene.setSkyColors(new Vector3f(dayTop).lerp(nightTop, smooth),
        new Vector3f(dayBottom).lerp(nightBottom, smooth))
        .setExposure(1f - 0.55f * smooth);
scene.sun().setDirection(new Vector3f(daySun)
        .lerp(nightSun, smooth).normalize())
        .setIntensity(1.2f - 1.05f * smooth);
```

Use a delayed second phase for street lights or emissive objects if they should
activate after dusk.

## Reflection

Environment reflection samples the skybox and is weighted by PBR Fresnel,
roughness, and material reflectivity. Screen-space reflection is separate:

```java
scene.setScreenSpaceReflectionsEnabled(true)
        .setScreenSpaceReflectionStrength(0.5f);
```

It samples the previous scene-color frame, so it cannot reflect off-screen or
behind occluders. Reflected light is a third, cheap ground-bounce approximation:

```java
scene.setReflectedLightEnabled(true)
        .setReflectedLightStrength(0.18f);
```

Keep reflected-light strength modest or it will wash out albedo colors.

## Fog and bloom

```java
scene.setFog(0.65f, 0.70f, 0.75f, 0.012f)
        .setBloomThreshold(1.1f)
        .setBloomStrength(0.45f)
        .setExposure(0.95f);
```

Fog density zero disables fog. Bloom extracts bright pixels and blurs them;
high exposure, bloom, and environment reflection together can make metal look
white, so lower those values when diagnosing brightness.

## Weather

Weather should toggle existing systems instead of recreating them:

```java
boolean rainy = weather == Weather.RAINY;
rain.setEnabled(rainy);
scene.setScreenSpaceReflectionsEnabled(rainy)
        .setScreenSpaceReflectionStrength(rainy ? 0.75f : 0f)
        .setFog(0.48f, 0.55f, 0.62f, rainy ? 0.012f : 0f);
```

Disable emitters and hide weather geometry during transitions. Reusing emitters
avoids allocation spikes.

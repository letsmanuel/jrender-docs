# Particles and weather

The engine integrates particle simulation into the normal `Engine` lifecycle.
Every active scene has one particle system, so game code only needs to create
emitters and configure them. The system supports:

* runtime scale, direction, rotation and transparency changes;
* predefined code configurations such as `rain` and `fog`;
* one initial force per spawned particle;
* optional gravity/physics assembly and manually specified particle weight;
* image particles that billboard, remain face-up, or rotate toward the camera;
* 3D model particles with a random model selected per spawn.

Rendering is GPU-instanced: particles sharing a mesh are submitted in batches
instead of one draw call per particle. Dead particle objects are reused and
removed with swap-removal to reduce allocation spikes in large effects.

```java
ParticleConfig smokeConfig = ParticleConfig.predefined("fog")
        .setPhysicsAssembled(true)
        .setParticleWeight(0.8f)
        .setScale(2f, 0.5f, 2f);
ParticleEmitter smoke = scene.particles().createEmitter("smoke", smokeConfig);
smoke.setPosition(0f, 1f, 0f);
```

`ParticleSystem.update` is called once per simulation frame and rendering is
performed by the renderer. Emitters can be disabled without destroying their
existing particles, which is useful for weather transitions.
Use `setSpawnArea(width, height, depth)` to distribute particles around the
emitter instead of spawning every particle at one point.

An emitter can optionally follow a moving `GameObject`:

```java
ParticleEmitter smoke = scene.particles().createEmitter("smoke", smokeConfig)
        .setPosition(0f, 1.5f, 0f)
        .bindTo chimney;
```

The emitter position is local to the bound object. Existing particles are
transformed with the object on every update, so a moving, rotating, or scaled
parent carries both newly spawned and already emitted particles. Call
`unbind()` to return to world-space simulation.

The public `Particle` state is live and mutable. `position()`, `velocity()`,
`rotation()`, and `scale()` return the actual runtime vectors. `age()`,
`lifetime()`, `alpha()`, `weight()`, `modelIndex()`, and `alive()` are useful
for diagnostics and custom effects, but ownership remains with the emitter.

Use `BILLBOARD` for camera-facing sprites, `FACE_UP` for ground fog or decals,
and `ROTATE_TO_CAMERA` for upright sprites that turn around world Y.

The BirdWorld sample combines this API with moving cloud volumes, fog density,
reflective puddle materials, and a four-state weather control. Clear weather
disables the weather effects; Cloudy adds moving cloud shadows; Foggy enables
screen fog and fog particles; Rainy enables falling particles and puddles.

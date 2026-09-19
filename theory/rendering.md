# Rendering and assets

Rendering is OpenGL-backed and scene-owned. `Renderer` draws opaque geometry,
sorted transparent geometry, particles, the skybox, and post-processing.

## Materials and PBR

```java
Material steel = new Material()
        .setTexture(albedoTexture)
        .setNormalMap(normalTexture)
        .setMetallicMap(metallicTexture)
        .setRoughnessMap(roughnessTexture)
        .setMetalness(0.9f)
        .setRoughness(0.28f)
        .setReflectivity(0.45f);
```

The lit shader uses GGX distribution, Schlick Fresnel, Smith geometry, direct
lights, derivative-based normal mapping, and roughness-weighted skybox
reflection. Base-color maps are sRGB. Normal, metallic, roughness, and packed
metallic-roughness maps are linear data. glTF packed maps use blue for metallic
and green for roughness.

## Supported model formats

| Format | Loader | Textures | Scope |
|---|---|---|---|
| OBJ | `OBJLoader` | caller-managed | static mesh |
| GLB/glTF | `GltfLoader` | embedded images | static nodes and PBR materials |
| FBX | `FbxLoader` | external filename-to-bytes map | static Assimp import |

FBX loading uses Assimp and pre-transforms node geometry. External texture keys
are matched by basename, so `textures/rifle_albedo.jpg` is supplied as
`rifle_albedo.jpg`.

```java
FbxLoader.Model rifle = FbxLoader.load(fbxBytes, textureBytesByFilename);
Vector3f center = rifle.center();
Vector3f size = rifle.size();
float largest = Math.max(size.x, Math.max(size.y, size.z));
float scale = targetSize / largest;
for (FbxLoader.Part part : rifle.parts()) {
    scene.createObject("rifle-part", part.mesh(), part.material())
            .setPosition(-center.x * scale, -center.y * scale, -center.z * scale)
            .setSize(scale);
}
```

GLB materials preserve base-color factor, alpha mode, UV selection, metalness,
roughness, normal maps, and packed metallic-roughness maps. Static skinning and
animation are not implemented.

## Transparency

Opaque and masked objects render first. Blended objects are detected from
material alpha mode, opacity, and texture alpha, then sorted back-to-front with
depth writes disabled. Use `MASK` for cutouts and `BLEND` for glass or smoke.

## Texture color spaces

```java
Texture color = Texture.fromEncodedImage(colorBytes);
Texture normal = Texture.fromEncodedImage(normalBytes, false);
Texture roughness = Texture.fromEncodedImage(roughnessBytes, false);
```

Do not use a normal or roughness map as an albedo map. A blue/purple surface
usually means a normal map was assigned to `setTexture`.

## Reflections and lighting

```java
scene.setSun(-0.35f, -1f, -0.2f, 1f, 0.92f, 0.72f, 1.25f)
        .setReflectedLightEnabled(true)
        .setReflectedLightStrength(0.2f)
        .setScreenSpaceReflectionsEnabled(true)
        .setScreenSpaceReflectionStrength(0.4f);
```

Screen-space reflection uses the previous scene color. Skybox reflection is the
environment term used by PBR materials. Both are approximations, not ray
tracing.

## Performance

Particle rendering is GPU-instanced. Reuse meshes and textures, keep an
emitter’s mesh set small, and combine static geometry when possible.

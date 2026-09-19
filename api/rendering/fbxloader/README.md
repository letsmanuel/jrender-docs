# FbxLoader

`FbxLoader` imports binary FBX data through Assimp. The loader accepts the FBX
bytes separately from a filename-to-bytes texture map, which makes ZIP or
classpath packages straightforward to use.

## `load(byte[] fbx, Map<String, byte[]> textures)`

The texture map is matched by basename. A path such as
`textures/sniperRifle_albedo2.jpg` is therefore resolved with the key
`sniperRifle_albedo2.jpg`. The loader recognizes albedo/base-color/diffuse,
normal, metallic, and roughness maps. Metallic, roughness, and normal maps are
uploaded as linear data textures.

```java
byte[] modelBytes = readResource("/models/sniper.fbx");
Map<String, byte[]> textureBytes = new HashMap<>();
textureBytes.put("sniper_albedo.jpg", readResource("/models/sniper_albedo.jpg"));
textureBytes.put("sniper_normal.jpg", readResource("/models/sniper_normal.jpg"));
textureBytes.put("sniper_metallic.jpg", readResource("/models/sniper_metallic.jpg"));
textureBytes.put("sniper_roughness.jpg", readResource("/models/sniper_roughness.jpg"));

FbxLoader.Model model = FbxLoader.load(modelBytes, textureBytes);
for (FbxLoader.Part part : model.parts()) {
    scene.createObject("rifle-part", part.mesh(), part.material());
}
```

Assimp pre-transforms FBX node geometry and triangulates faces. Animation,
skinning, and material animation are not exposed by this static loader.

## `Model`

- `parts()` returns imported mesh/material pairs.
- `min()`, `max()`, `size()`, and `center()` describe the combined bounds.

## `Part`

- `mesh()` returns the imported geometry.
- `material()` returns the imported PBR material.

## Common mistakes

- Passing ZIP paths instead of decoded bytes.
- Using full texture paths as map keys when the FBX only stores basenames.
- Uploading normal, metallic, or roughness images as sRGB color data.
- Forgetting to normalize the model using `Model.size()` before placing it.

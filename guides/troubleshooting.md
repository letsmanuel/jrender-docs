# Troubleshooting

## Model is white

Check the albedo assignment before changing lighting. A white albedo texture
and a metallic value near one produce a white reflective metal by design. For
GLB files, inspect the embedded image and `baseColorFactor`. For FBX files,
verify that the texture map uses the basename expected by `FbxLoader`.

## Metallic parts are too bright

Use a correctly authored albedo map and linear metallic/roughness maps. Do not
upload metallic or roughness data as sRGB. Keep `setReflectivity` moderate and
remember that a metallic surface takes its specular color from its albedo.

## Normal map looks purple or inflates color

Assign it with `setNormalMap`, not `setTexture`. Load it with
`Texture.fromEncodedImage(bytes, false)` so the map remains linear data.

## Transparent geometry is opaque

Set `Material.AlphaMode.BLEND` or `MASK`. `BLEND` needs texture alpha or an
opacity below one. `MASK` also needs an appropriate `setAlphaCutoff` value.

## FBX has geometry but no textures

Pass a map keyed by filenames without directories. Assimp may report a path such
as `textures/rifle_albedo.jpg`, while the loader looks up
`rifle_albedo.jpg`. Include the albedo, normal, metallic, and roughness files in
the ZIP or resource package.

## Textures appear inverted

Use the loader appropriate for the asset format and do not flip the same image
twice. GLB embedded images use the glTF orientation path. Inspect a directional
decal or label rather than a symmetric test texture.

## Particles stutter

Reuse emitters and meshes. Particle rendering is instanced, but creating and
destroying emitters, textures, or models every frame still causes allocations.
Keep model particle variants limited and use `setMaxParticles` deliberately.

# Material

**Package:** `game.letsmanuel.engine.render`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/render/Material.java`

## Purpose

Material is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [tint](./1-tint.md)
- [setTint](./2-settint-float-r-float-g-float-b.md)
- [setTint](./3-settint-vector3f-v.md)
- [albedoMap](./4-albedomap.md)
- [setTexture](./5-settexture-texture-t.md)
- [specularStrength](./6-specularstrength.md)
- [setSpecular](./7-setspecular-float-v.md)
- [shininess](./8-shininess.md)
- [setShininess](./9-setshininess-float-v.md)
- [emissive](./10-emissive.md)
- [setEmissive](./11-setemissive-float-v.md)
- [reflectivity](./12-reflectivity.md)
- [setReflectivity](./13-setreflectivity-float-v.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

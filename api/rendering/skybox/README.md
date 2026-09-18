# Skybox

**Package:** `game.letsmanuel.engine.render`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/render/Skybox.java`

## Purpose

Skybox is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [procedural](./1-procedural-vector3f-topcolor-vector3f-bottomcolor.md)
- [fromFiles](./2-fromfiles-string-right-string-left-string-top-string-bottom-string-front-string-back.md)
- [textureId](./3-textureid.md)
- [bind](./4-bind-int-unit.md)
- [close](./5-close.md)
- [dispose](./6-dispose.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

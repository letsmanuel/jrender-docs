# Texture

**Package:** `game.letsmanuel.engine.render`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/render/Texture.java`

## Purpose

Texture is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [load](./1-load-string-path.md)
- [fromImage](./2-fromimage-bufferedimage-img.md)
- [bind](./3-bind-int-unit.md)
- [unbind](./4-unbind-int-unit.md)
- [id](./5-id.md)
- [width](./6-width.md)
- [height](./7-height.md)
- [close](./8-close.md)
- [dispose](./9-dispose.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

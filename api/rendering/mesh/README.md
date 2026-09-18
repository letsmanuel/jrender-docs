# Mesh

**Package:** `game.letsmanuel.engine.render`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/render/Mesh.java`

## Purpose

Mesh is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [h](./1-h-float-positions-float-normals-float-uvs-int-indices.md)
- [draw](./2-draw.md)
- [indexCount](./3-indexcount.md)
- [positions](./4-positions.md)
- [normals](./5-normals.md)
- [indices](./6-indices.md)
- [close](./7-close.md)
- [dispose](./8-dispose.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

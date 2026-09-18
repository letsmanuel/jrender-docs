# MeshFactory

**Package:** `game.letsmanuel.engine.render`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/render/MeshFactory.java`

## Purpose

MeshFactory is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [cube](./1-cube.md)
- [plane](./2-plane-float-size.md)
- [sphere](./3-sphere-int-xsegments-int-ysegments.md)
- [screenQuad](./4-screenquad.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

# Raycaster

**Package:** `game.letsmanuel.engine.ray`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/ray/Raycaster.java`

## Purpose

Raycaster is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [screenRay](./1-screenray-camera-camera-float-screenx-float-screeny-float-screenwidth-float-screenheight.md)
- [cast](./2-cast-scene-scene-ray-ray-float-maxdistance.md)
- [first](./3-first-scene-scene-ray-ray-float-maxdistance.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

# Camera

**Package:** `game.letsmanuel.engine.core`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/core/Camera.java`

## Purpose

Camera is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [viewMatrix](./1-viewmatrix.md)
- [projectionMatrix](./2-projectionmatrix.md)
- [forward](./3-forward.md)
- [right](./4-right.md)
- [position](./5-position.md)
- [setPosition](./6-setposition-float-x-float-y-float-z.md)
- [setPosition](./7-setposition-vector3f-v.md)
- [addYaw](./8-addyaw-float-degrees.md)
- [addPitch](./9-addpitch-float-degrees.md)
- [setYaw](./10-setyaw-float-deg.md)
- [setPitch](./11-setpitch-float-deg.md)
- [setFov](./12-setfov-float-deg.md)
- [setNear](./13-setnear-float-n.md)
- [setFar](./14-setfar-float-f.md)
- [setAspect](./15-setaspect-float-a.md)
- [yaw](./16-yaw.md)
- [pitch](./17-pitch.md)
- [aspect](./18-aspect.md)
- [fov](./19-fov.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

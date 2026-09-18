# Transform

**Package:** `game.letsmanuel.engine.core`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/core/Transform.java`

## Purpose

Transform is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [localMatrix](./1-localmatrix.md)
- [worldMatrix](./2-worldmatrix.md)
- [worldPosition](./3-worldposition.md)
- [position](./4-position.md)
- [rotation](./5-rotation.md)
- [scale](./6-scale.md)
- [parent](./7-parent.md)
- [setParent](./8-setparent-transform-parent.md)
- [setPosition](./9-setposition-float-x-float-y-float-z.md)
- [setPosition](./10-setposition-vector3f-v.md)
- [translate](./11-translate-float-x-float-y-float-z.md)
- [translate](./12-translate-vector3f-v.md)
- [setRotation](./13-setrotation-quaternionf-q.md)
- [setRotationDeg](./14-setrotationdeg-float-x-float-y-float-z.md)
- [rotateDeg](./15-rotatedeg-float-dx-float-dy-float-dz.md)
- [setScale](./16-setscale-float-sx-float-sy-float-sz.md)
- [setScale](./17-setscale-float-s.md)
- [setScale](./18-setscale-vector3f-v.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

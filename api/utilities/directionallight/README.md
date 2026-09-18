# DirectionalLight

**Package:** `game.letsmanuel.engine.light`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/light/DirectionalLight.java`

## Purpose

DirectionalLight is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [direction](./1-direction.md)
- [color](./2-color.md)
- [intensity](./3-intensity.md)
- [setDirection](./4-setdirection-float-x-float-y-float-z.md)
- [setDirection](./5-setdirection-vector3f-dir.md)
- [setColor](./6-setcolor-float-r-float-g-float-b.md)
- [setColor](./7-setcolor-vector3f-c.md)
- [setIntensity](./8-setintensity-float-v.md)
- [castsShadow](./9-castsshadow.md)
- [setShadows](./10-setshadows-boolean-enabled.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

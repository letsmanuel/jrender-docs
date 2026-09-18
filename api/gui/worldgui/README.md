# WorldGui

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/WorldGui.java`

## Purpose

WorldGui is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [i](./1-i-float-width-float-height.md)
- [gui](./2-gui.md)
- [add](./3-add-guielement-element.md)
- [open](./4-open-float-x-float-y-float-z.md)
- [open](./5-open-vector3f-position.md)
- [close](./6-close.md)
- [close](./7-close-guiopenanimation-animation-float-duration.md)
- [isOpen](./8-isopen.md)
- [position](./9-position.md)
- [update](./10-update-window-window-camera-camera-float-dt.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

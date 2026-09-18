# GuiBlur

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/GuiBlur.java`

## Purpose

GuiBlur is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [r](./1-r-float-x-float-y-float-w-float-h.md)
- [setBlur](./2-setblur-float-radius-float-strength.md)
- [setGradient](./3-setgradient-float-start-float-end.md)
- [setGradientDirection](./4-setgradientdirection-float-x-float-y.md)
- [setTint](./5-settint-float-r-float-g-float-b.md)
- [setOpacity](./6-setopacity-float-opacity.md)
- [fitViewport](./7-fitviewport.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

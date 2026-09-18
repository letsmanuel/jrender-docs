# GuiSlider

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/GuiSlider.java`

## Purpose

GuiSlider is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [r](./1-r-float-x-float-y-float-w-float-h.md)
- [setValue](./2-setvalue-float-value.md)
- [value](./3-value.md)
- [setOnChanged](./4-setonchanged-java.util.function.consumer-float-listener.md)
- [setColors](./5-setcolors-float-trackr-float-trackg-float-trackb-float-fillr-float-fillg-float-fillb-float-thumbr-float-thumbg-float-thumbb.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

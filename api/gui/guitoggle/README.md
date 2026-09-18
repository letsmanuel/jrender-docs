# GuiToggle

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/GuiToggle.java`

## Purpose

GuiToggle is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [constructor](./1-constructor.md)
- [setOn](./2-seton-boolean-value.md)
- [isOn](./3-ison.md)
- [setTrackColors](./4-settrackcolors-float-offr-float-offg-float-offb-float-onr-float-ong-float-onb.md)
- [setKnobColor](./5-setknobcolor-float-r-float-g-float-b.md)
- [setOnChanged](./6-setonchanged-java.util.function.consumer-boolean-listener.md)




## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

# GuiCategory

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/GuiCategory.java`

## Purpose

GuiCategory is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [y](./1-y-string-title-guifont-font-float-x-float-y-float-width.md)
- [addSetting](./2-addsetting-guielement-element.md)
- [setExpanded](./3-setexpanded-boolean-expanded.md)
- [expanded](./4-expanded.md)
- [content](./5-content.md)
- [toggle](./6-toggle.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

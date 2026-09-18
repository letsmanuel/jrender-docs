# Gui

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/Gui.java`

## Purpose

Gui is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [setReferenceSize](./1-setreferencesize-float-width-float-height.md)
- [setTooltipStyle](./2-settooltipstyle-guitooltipstyle-style.md)
- [add](./3-add-guielement-e.md)
- [remove](./4-remove-guielement-e.md)
- [clear](./5-clear.md)
- [roots](./6-roots.md)
- [hovered](./7-hovered.md)
- [update](./8-update-window-window-float-dt.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

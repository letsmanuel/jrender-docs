# GuiImage

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/GuiImage.java`

## Purpose

GuiImage is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [constructor](./1-constructor.md)
- [setTint](./2-settint-float-r-float-g-float-b-float-a.md)
- [texture](./3-texture.md)
- [tintR](./4-tintr.md)
- [tintG](./5-tintg.md)
- [tintB](./6-tintb.md)
- [tintA](./7-tinta.md)




## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

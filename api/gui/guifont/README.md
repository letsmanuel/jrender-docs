# GuiFont

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/GuiFont.java`

## Purpose

GuiFont is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [create](./1-create-string-fontname-int-size.md)
- [glyph](./2-glyph-char-c.md)
- [width](./3-width-string-line.md)
- [measureWidth](./4-measurewidth-string-text.md)
- [lineHeight](./5-lineheight.md)
- [ascent](./6-ascent.md)
- [spaceAdvance](./7-spaceadvance.md)
- [atlas](./8-atlas.md)
- [dispose](./9-dispose.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

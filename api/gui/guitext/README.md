# GuiText

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/GuiText.java`

## Purpose

GuiText is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [t](./1-t-string-text-guifont-font-float-x-float-y.md)
- [setText](./2-settext-string-text.md)
- [setFont](./3-setfont-guifont-font.md)
- [setColor](./4-setcolor-float-r-float-g-float-b.md)
- [setBackground](./5-setbackground-float-r-float-g-float-b-float-a.md)
- [clearBackground](./6-clearbackground.md)
- [lineCount](./7-linecount.md)
- [text](./8-text.md)
- [font](./9-font.md)
- [r](./10-r.md)
- [g](./11-g.md)
- [b](./12-b.md)
- [hasBackground](./13-hasbackground.md)
- [backgroundR](./14-backgroundr.md)
- [backgroundG](./15-backgroundg.md)
- [backgroundB](./16-backgroundb.md)
- [backgroundA](./17-backgrounda.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

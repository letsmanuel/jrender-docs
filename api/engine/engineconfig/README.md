# EngineConfig

**Package:** `game.letsmanuel.engine`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/EngineConfig.java`

## Purpose

EngineConfig is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [g](./1-g.md)
- [g](./2-g-string-title-int-width-int-height-boolean-vsync.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

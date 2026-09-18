# SettingsStore

**Package:** `game.letsmanuel.engine`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/SettingsStore.java`

## Purpose

SettingsStore is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [constructor](./1-constructor.md)
- [save](./2-save-string-savename-string-key-object-value.md)
- [save](./3-save-string-savename-map-string-object-table.md)
- [load](./4-load-string-savename.md)
- [get](./5-get-string-savename-string-key.md)
- [directory](./6-directory.md)




## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

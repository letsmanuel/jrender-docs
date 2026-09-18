# SceneManager

**Package:** `game.letsmanuel.engine.scene`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/scene/SceneManager.java`

## Purpose

SceneManager is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [create](./1-create-string-name.md)
- [has](./2-has-string-name.md)
- [get](./3-get-string-name.md)
- [getOrCreate](./4-getorcreate-string-name.md)
- [current](./5-current.md)
- [switchTo](./6-switchto-string-name.md)
- [switchTo](./7-switchto-scene-scene.md)
- [remove](./8-remove-string-name.md)
- [all](./9-all.md)
- [isEmpty](./10-isempty.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

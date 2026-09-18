# SoundEngine

**Package:** `game.letsmanuel.engine`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/SoundEngine.java`

## Purpose

SoundEngine is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [init](./1-init.md)
- [play](./2-play-string-id.md)
- [loop](./3-loop-string-id.md)
- [loopRandom](./4-looprandom-string-id.md)
- [stop](./5-stop-string-id.md)
- [fadeIn](./6-fadein-string-id-float-targetvolume-float-duration.md)
- [fadeOut](./7-fadeout-string-id-float-duration.md)
- [fadeTo](./8-fadeto-string-id-float-targetvolume-float-duration.md)
- [update](./9-update-float-dt.md)
- [unload](./10-unload-string-id.md)
- [dispose](./11-dispose.md)
- [setVolume](./12-setvolume-string-id-float-volume.md)
- [volume](./13-volume-string-id.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

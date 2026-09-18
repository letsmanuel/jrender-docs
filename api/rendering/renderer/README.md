# Renderer

**Package:** `game.letsmanuel.engine.render`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/render/Renderer.java`

## Purpose

Renderer is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [r](./1-r-window-window.md)
- [init](./2-init.md)
- [render](./3-render-scene-scene-camera-camera-float-time.md)
- [setShadowsEnabled](./4-setshadowsenabled-boolean-enabled.md)
- [shadowsEnabled](./5-shadowsenabled.md)
- [setQuality](./6-setquality-int-quality.md)
- [quality](./7-quality.md)
- [sceneTexture](./8-scenetexture.md)
- [capture](./9-capture-string-path.md)
- [dispose](./10-dispose.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

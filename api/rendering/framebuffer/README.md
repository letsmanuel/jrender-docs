# Framebuffer

**Package:** `game.letsmanuel.engine.render`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/render/Framebuffer.java`

## Purpose

Framebuffer is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [r](./1-r-int-width-int-height-boolean-withdepth.md)
- [depthOnly](./2-depthonly-int-width-int-height.md)
- [resize](./3-resize-int-newwidth-int-newheight.md)
- [bind](./4-bind.md)
- [id](./5-id.md)
- [colorTexture](./6-colortexture.md)
- [depthTexture](./7-depthtexture.md)
- [width](./8-width.md)
- [height](./9-height.md)
- [unbind](./10-unbind.md)
- [close](./11-close.md)
- [dispose](./12-dispose.md)



## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

# Utilities API

Lighting, ray casting, and small rendering-support primitives.

- [Directional light](directionallight/README.md)
- [Point light](pointlight/README.md)
- [Ray](ray/README.md)
- [Ray caster](raycaster/README.md)
- [Ray hit](rayhit/README.md)
- [Drop shadow](dropshadow/README.md)
- [Easing](easing/README.md)


## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

# API reference

The API reference is grouped by responsibility rather than package name. Every class page lists its public functions, and every function page includes its signature, arguments, return behavior, sample code, common issues, a reusable template, and agent instructions.

- [Engine and window](engine/README.md)
- [Core math and transforms](core/README.md)
- [GUI](gui/README.md)
- [Rendering](rendering/README.md)
- [Scenes and world objects](scene/README.md)
- [Audio and persistence](audio/README.md)
- [Utilities, lighting, and ray casting](utilities/README.md)

## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

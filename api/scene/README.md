# Scene and world-object API

Scene management, world objects, and active-scene access.

- [Scene](scene/README.md)
- [Scene manager](scenemanager/README.md)
- [Game objects](gameobject/README.md)


## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

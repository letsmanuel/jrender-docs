# Rendering API

OpenGL resources and the scene rendering pipeline.

- [Renderer](renderer/README.md)
- [Materials](material/README.md)
- [Meshes](mesh/README.md)
- [Mesh factory](meshfactory/README.md)
- [Textures](texture/README.md)
- [Shaders](shader/README.md)
- [Framebuffers](framebuffer/README.md)
- [OBJ loading](objloader/README.md)
- [Skyboxes](skybox/README.md)


## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

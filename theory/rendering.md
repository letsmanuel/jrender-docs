# Rendering and assets

The renderer supports scene framebuffers, bloom, shadows, materials, meshes, textures, OBJ loading, skyboxes, and shader-backed post-processing. GUI blur samples the scene texture. GUI coordinates are reference-resolution coordinates with uniform scaling and letterboxing; child coordinates are relative to the parent top-left.

## Frame flow

```text
world scene -> scene framebuffer -> bloom/post-processing -> world GUI -> screen GUI
```

The renderer produces the scene texture before `GuiRenderer` draws blur layers. This is why a GUI blur can soften the rendered world without tinting the source scene.

## Quality and resolution

The window owns the actual framebuffer size. The renderer resizes its targets when that size changes, while the GUI keeps a stable reference coordinate system and applies uniform scaling.

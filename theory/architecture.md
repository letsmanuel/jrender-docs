# Architecture

`Engine` owns the main loop and coordinates `Window`, `Renderer`, `GuiRenderer`,
`SceneManager`, `SettingsStore`, `SoundEngine`, and world GUIs. `Scene` owns
world state, cameras, lights, objects, physics, and one `ParticleSystem`.

The renderer has these broad passes:

1. directional shadow map;
2. opaque and masked lit objects;
3. sorted alpha-blended objects;
4. instanced particles;
5. skybox;
6. bloom extraction, blur, and composite;
7. world and root GUI.

GUI is a retained tree with parent-relative coordinates, animation, hit testing,
clipping, tooltips, and responsive scaling. Rendering, audio, Assimp, and
texture resources use native APIs and must follow lifecycle and thread rules.

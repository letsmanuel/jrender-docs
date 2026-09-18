# Architecture

`Engine` owns the main loop and coordinates `Window`, `Renderer`, `GuiRenderer`, `SceneManager`, `SettingsStore`, `SoundEngine`, and world GUIs. `Scene` owns world state, cameras, lights, and objects. GUI is a retained tree with parent-relative coordinates, animation, hit testing, clipping, tooltips, and responsive scaling. Rendering and audio use native OpenGL and OpenAL resources and must follow lifecycle rules.

## Dependency direction

Prefer dependencies that point toward the engine services:

```text
GameLogic -> Engine services
Engine    -> Window, Renderer, GUI, SceneManager, Audio, Settings
Renderer  -> Scene data and GPU resources
GUI       -> Window input and renderer output
```

Keep gameplay rules in game code. Keep reusable rendering, GUI, audio, and persistence behavior in engine services. Avoid making a renderer know about a specific game screen or making a GUI callback contain scene-generation logic.

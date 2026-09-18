# Architecture

`Engine` owns the main loop and coordinates `Window`, `Renderer`, `GuiRenderer`, `SceneManager`, `SettingsStore`, `SoundEngine`, and world GUIs. `Scene` owns world state, cameras, lights, and objects. GUI is a retained tree with parent-relative coordinates, animation, hit testing, clipping, tooltips, and responsive scaling. Rendering and audio use native OpenGL and OpenAL resources and must follow lifecycle rules.

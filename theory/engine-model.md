# Engine model

JRender is a coordinator around a single game loop. The `Engine` owns the runtime services and exposes them to `GameLogic`.

## Runtime services

| Service | Responsibility |
|---|---|
| `Window` | GLFW window, input, framebuffer size, VSync, and fullscreen |
| `SceneManager` | Scene creation, lookup, and active-scene selection |
| `Renderer` | OpenGL scene rendering, shadows, bloom, and quality |
| `Gui` | Root GUI tree, input dispatch, layout, and animation |
| `SoundEngine` | OpenAL playback, decoding, volume, and fades |
| `SettingsStore` | Compressed typed persistence under the project ID |

## The important rule

Game code describes state in `init` and `update`; the engine owns the order in which input, simulation, UI, rendering, and resource cleanup happen.

```java
Engine engine = new Engine(new EngineConfig("Example", 1280, 720, true));
engine.run(new GameLogic() {
    @Override
    public void init(Engine engine) {
        engine.createScene("main");
    }

    @Override
    public void update(float dt, Engine engine) {
        // Gameplay receives the simulation-scaled delta.
    }
});
```

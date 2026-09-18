# Lifecycle and threading

Initialization creates the window and native contexts before invoking `GameLogic.init`. Each frame polls input, advances sound fades, computes simulation and UI deltas, updates game logic and GUI, renders scenes, renders world GUIs, and renders the root GUI. The engine is intended for a single engine/render thread. Call `Engine.dispose()` once to release native resources.

## Safe lifecycle pattern

```java
public final class Game implements GameLogic {
    private static final String SCENE_ID = "main";
    private Scene scene;

    @Override
    public void init(Engine engine) {
        scene = engine.createScene(SCENE_ID);
        initialiseWorld(scene);
        initialiseUi(engine);
        initialiseAudio(engine);
    }

    @Override
    public void update(float dt, Engine engine) {
        updateGameplay(dt);
    }

    private void initialiseWorld(Scene scene) {
        // Create meshes, materials, lights, and objects here.
    }

    private void initialiseUi(Engine engine) {
        // Create fonts and GUI roots here.
    }

    private void initialiseAudio(Engine engine) {
        // Configure sound IDs and initial volume here.
    }

    private void updateGameplay(float dt) {
        // Mutate existing gameplay state using dt.
    }
}
```

Do not perform expensive construction in `update`. If an object must be spawned during gameplay, create it through a dedicated factory and define who owns its resources.

## Time scaling

Simulation and UI time are separate. Use simulation time for gameplay, and UI time for animations or menus that should remain responsive while gameplay is slowed.

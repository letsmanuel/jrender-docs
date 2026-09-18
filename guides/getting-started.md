# Getting started

Use the exported engine coordinates `game.letsmanuel:engine:1.0`, or distribute the version 1.0 engine JAR with its runtime dependencies.

```gradle
repositories {
    maven { url = uri("path/to/engine/build/repository") }
}

dependencies {
    implementation "game.letsmanuel:engine:1.0"
}
```

A minimal game creates an `EngineConfig`, supplies a `GameLogic` implementation, creates a scene, and calls `Engine.run`. Initialize game-owned resources in `GameLogic.init` and update gameplay in `GameLogic.update`.

```java
public final class Main {
    private static final String WINDOW_TITLE = "My Game";
    private static final int WINDOW_WIDTH = 1280;
    private static final int WINDOW_HEIGHT = 720;
    private static final boolean ENABLE_VSYNC = true;
    private static final String MAIN_SCENE = "main";

    public static void main(String[] args) {
        EngineConfig config = new EngineConfig(
                WINDOW_TITLE,
                WINDOW_WIDTH,
                WINDOW_HEIGHT,
                ENABLE_VSYNC
        );
        new Engine(config).run(new GameLogic() {
            @Override
            public void init(Engine engine) {
                engine.createScene(MAIN_SCENE);
            }

            @Override
            public void update(float dt, Engine engine) {
                // Update gameplay with the simulation-scaled delta.
            }
        });
    }
}
```

Resources use classpath paths: shaders under `/shaders/`, sounds under `/sounds/`, and other assets under the resource root.

Use `Engine.getFPS()` for the current measured frame rate. Dispose the engine once at shutdown.

## Recommended project structure

```text
src/main/java/
  game/
    Main.java
    Game.java
    world/
    ui/
src/main/resources/
  shaders/
  sounds/
  textures/
```

Keep game-specific code outside the engine package. Store resource IDs and tuning values in named constants or configuration classes instead of repeating literals.

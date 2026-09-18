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
    public static void main(String[] args) {
        EngineConfig config = new EngineConfig("My Game", 1280, 720, true);
        new Engine(config).run(new GameLogic() {
            @Override
            public void init(Engine engine) {
                engine.createScene("main");
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

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
public final class SampleGame implements GameLogic {
    private Scene scene;

    @Override
    public void init(Engine engine) {
        scene = engine.createScene("main");
        scene.createObject("ground", MeshFactory.plane(40f), new Material());
    }

    @Override
    public void update(float dt, Engine engine) {
        // Use dt for simulation. It already includes simulation time scaling.
    }
}
```

Resources use classpath paths: shaders under `/shaders/`, sounds under `/sounds/`, and other assets under the resource root.

Use `Engine.getFPS()` for the current measured frame rate. Dispose the engine once at shutdown.

## Dependencies

The engine uses LWJGL OpenGL, GLFW, OpenAL, STB, and Assimp natives. Keep the
engine dependency and matching native runtime artifacts together. FBX support
requires the Assimp native library supplied by the engine Gradle module.

## Resource ownership

Create OpenGL-backed `Texture`, `Mesh`, `Shader`, `Skybox`, and `Framebuffer`
objects after the engine has created its context. Do not load them from worker
threads unless the worker owns a valid shared context. Release scene and engine
resources through `Engine.dispose()`.

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

Resources use classpath paths: shaders under `/shaders/`, sounds under `/sounds/`, and other assets under the resource root.

Use `Engine.getFPS()` for the current measured frame rate. Dispose the engine once at shutdown.

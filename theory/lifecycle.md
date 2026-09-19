# Lifecycle and threading

Initialization creates the window and native contexts before invoking
`GameLogic.init`. Each frame polls input, advances sound fades, computes
simulation and UI deltas, advances active-scene physics and particles, updates
game logic and GUI, renders scenes, renders world GUIs, and renders the root
GUI. The engine is intended for a single engine/render thread. Call
`Engine.dispose()` once to release native resources.

Particle simulation and physics use the simulation time scale. GUI animation
uses the independent UI time scale. Audio updates use the real frame delta, so
audio fades do not pause when simulation is paused.

```java
engine.setSimulationTimeScale(0f);
engine.setUiTimeScale(1f);
engine.setTimeScale(0.5f, true);
```

Both setters clamp negative values to zero. `GameLogic.update` receives the
scaled simulation delta; GUI callbacks receive the scaled UI delta.

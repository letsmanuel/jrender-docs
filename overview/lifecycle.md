# Lifecycle and threading

Initialization creates the window and native contexts before invoking `GameLogic.init`. Each frame polls input, advances sound fades, computes simulation and UI deltas, updates game logic and GUI, renders scenes, renders world GUIs, and renders the root GUI. The engine is intended for a single engine/render thread. Call `Engine.dispose()` once to release native resources.

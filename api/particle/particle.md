# Particle

`Particle` is the mutable runtime state of one emitted particle. The vectors
returned by `position()`, `velocity()`, `rotation()`, and `scale()` are live
objects; mutating them changes the simulation immediately.

## State

- `position()` — world-space position.
- `velocity()` — world-space velocity.
- `rotation()` — Euler rotation in degrees.
- `scale()` — per-axis render scale.
- `age()` and `lifetime()` — simulation age and configured lifetime.
- `alpha()` — current render alpha after emitter fade calculation.
- `weight()` — configured particle weight.
- `modelIndex()` — selected emitter model index, or `-1` for the default quad.
- `alive()` — true while `age() < lifetime()`.

Particle instances are owned by `ParticleEmitter`; game code normally observes
them rather than constructing or recycling them directly.

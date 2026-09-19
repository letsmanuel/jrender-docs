# ParticleSystem

**Package:** `game.letsmanuel.engine.particle`

Scene-owned simulation and rendering service. The `Engine` calls `update` and
the renderer calls `render` automatically.

The renderer batches particles with GPU instancing. One draw is issued per
emitter mesh group rather than per particle. `dispose()` releases the quad and
particle shader resources and must run while the OpenGL context is current.

## Functions

- [createEmitter](./1-createemitter-string-name.md)
- [createEmitter with config](./2-createemitter-string-name-particleconfig-config.md)
- [emitter](./3-emitter-string-name.md)
- `addEmitter`, `removeEmitter`, `emitters`, `setGravity`, and `gravity`
  provide collection and simulation-gravity control.
- `update`, `render`, and `dispose` are lifecycle methods normally called by
  the engine.

Large effects should reuse one emitter, set a bounded `maxParticles`, and avoid
changing model collections while rendering.

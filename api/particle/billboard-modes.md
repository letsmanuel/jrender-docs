# ParticleBillboardMode

Orientation modes for image and quad particles:

- `BILLBOARD` faces the camera using the camera basis.
- `FACE_UP` preserves a world-up style orientation and applies particle Euler
  rotation.
- `ROTATE_TO_CAMERA` rotates around the world Y axis toward the camera while
  preserving vertical orientation.

Use the enum through `ParticleConfig.setBillboardMode(...)`.

```java
ParticleConfig sparks = new ParticleConfig()
        .setBillboardMode(ParticleBillboardMode.ROTATE_TO_CAMERA)
        .setScale(0.08f, 0.08f, 0.08f);
```

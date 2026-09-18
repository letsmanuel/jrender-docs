# Build a scene

Create a scene during initialization, configure its camera, add a mesh and material, then update gameplay from the engine loop.

```java
public final class DemoGame implements GameLogic {
    @Override
    public void init(Engine engine) {
        Scene scene = engine.createScene("main");
        scene.camera()
                .setPosition(0f, 2f, 8f)
                .setYaw(0f)
                .setPitch(-12f);

        Material material = new Material()
                .setTint(0.8f, 0.45f, 0.2f)
                .setSpecular(0.2f)
                .setShininess(16f);

        scene.createObject("crate", MeshFactory.cube(), material)
                .setPosition(0f, 1f, 0f)
                .setSize(2f);
    }

    @Override
    public void update(float dt, Engine engine) {
        GameObject crate = engine.currentScene().object("crate");
        crate.rotate(0f, 45f * dt, 0f);
    }
}
```

Keep scene creation in `init` and use the scaled `dt` supplied to `update` for deterministic gameplay motion.

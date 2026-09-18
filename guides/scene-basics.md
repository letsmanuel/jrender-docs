# Build a scene

Create a scene during initialization, configure its camera, add a mesh and material, then update gameplay from the engine loop.

```java
public final class DemoGame implements GameLogic {
    private static final String MAIN_SCENE = "main";
    private static final String CRATE_ID = "crate";
    private static final float CAMERA_HEIGHT = 2.0f;
    private static final float CAMERA_DISTANCE = 8.0f;
    private static final float CAMERA_PITCH = -12.0f;
    private static final float OBJECT_HEIGHT = 1.0f;
    private static final float OBJECT_SIZE = 2.0f;
    private static final float ROTATION_DEGREES_PER_SECOND = 45.0f;

    @Override
    public void init(Engine engine) {
        Scene scene = engine.createScene(MAIN_SCENE);
        scene.camera()
                .setPosition(0.0f, CAMERA_HEIGHT, CAMERA_DISTANCE)
                .setYaw(0.0f)
                .setPitch(CAMERA_PITCH);

        Material material = new Material()
                .setTint(0.8f, 0.45f, 0.2f)
                .setSpecular(0.2f)
                .setShininess(16.0f);

        scene.createObject(CRATE_ID, MeshFactory.cube(), material)
                .setPosition(0.0f, OBJECT_HEIGHT, 0.0f)
                .setSize(OBJECT_SIZE);
    }

    @Override
    public void update(float dt, Engine engine) {
        GameObject crate = engine.currentScene().object(CRATE_ID);
        crate.rotate(0.0f, ROTATION_DEGREES_PER_SECOND * dt, 0.0f);
    }
}
```

Keep scene creation in `init` and use the scaled `dt` supplied to `update` for deterministic gameplay motion.

## Scene setup checklist

1. Create the scene once and retain references to frequently updated objects.
2. Configure the camera before evaluating visual placement.
3. Give objects stable IDs instead of relying on list positions.
4. Keep material tuning in named constants or a material factory.
5. Multiply movement and rotation rates by `dt`.

# Best practices

Use these rules when building a game with JRender. They keep gameplay deterministic, native resources safe, and UI behavior predictable.

## Keep lifecycle boundaries clear

Create scenes, fonts, meshes, textures, GUI trees, and persistent settings during `GameLogic.init`. Use `GameLogic.update` for state changes. Do not create OpenGL or OpenAL resources from static initializers.

```java
public final class Game implements GameLogic {
    private static final String MAIN_SCENE = "main";
    private Scene scene;

    @Override
    public void init(Engine engine) {
        scene = engine.createScene(MAIN_SCENE);
    }

    @Override
    public void update(float dt, Engine engine) {
        // Update already-created objects and state here.
    }
}
```

## Name configuration values

Use constants or configuration objects for dimensions, speeds, colors, durations, and IDs. This makes tuning safe and makes the meaning of a value obvious.

```java
private static final float CAMERA_HEIGHT = 2.0f;
private static final float CAMERA_DISTANCE = 8.0f;
private static final float OBJECT_SIZE = 2.0f;
private static final float ROTATION_DEGREES_PER_SECOND = 45.0f;
```

Avoid scattering raw literals through scene and GUI construction.

## Use the supplied delta time

Multiply rates by `dt`; never assume a fixed frame rate. The engine supplies simulation-scaled time to gameplay and UI-scaled time to GUI updates.

```java
private static final float MOVE_UNITS_PER_SECOND = 5.0f;

position.x += MOVE_UNITS_PER_SECOND * dt;
```

## Keep ownership explicit

The subsystem that creates a native resource owns it. Let `Engine.dispose()` release engine-owned resources. Do not delete OpenGL or OpenAL handles from unrelated game code.

## Prefer fluent configuration, but keep references

Chaining is useful for immutable-looking setup, but keep a field for anything that must be updated later.

```java
private GuiSlider volumeSlider;

volumeSlider = new GuiSlider(SLIDER_X, SLIDER_Y, SLIDER_WIDTH, SLIDER_HEIGHT)
        .setValue(initialVolume);
```

## Validate persisted values

Settings files are user-controlled application data. Clamp numbers, provide fallbacks, and validate enums before applying them to a renderer, window, or audio source.

## Keep UI coordinates intentional

Define a reference resolution and use named layout constants. Prefer parent-relative children, `center()`, and scroll insets over manually compensating for window size.

## Avoid hidden side effects in callbacks

Button, slider, and toggle callbacks should update one clear piece of state, call the owning subsystem, and persist the new value if appropriate. Avoid rebuilding the entire GUI tree from a click callback.

## Debug systematically

When a visual or timing issue appears:

1. Confirm the element’s parent and coordinate space.
2. Confirm the actual framebuffer size and reference GUI scale.
3. Check visibility, alpha, clipping, and sticky status.
4. Confirm that the callback is not being fired repeatedly.
5. Test at both the reference resolution and a resized window.

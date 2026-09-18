# `render`

**Declaring type:** [Renderer](./README.md)  
**Visibility:** `public`  
**Signature:** `public void render(Scene scene, Camera camera, float time)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Renderer` and performs the operation represented by `render`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `scene` | `Scene` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `camera` | `Camera` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `time` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Scene scene`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Camera camera`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float time`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.render(scene, camera, time);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.render(scene, camera, time);
```

## Agent instructions

When modifying code that calls `render`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


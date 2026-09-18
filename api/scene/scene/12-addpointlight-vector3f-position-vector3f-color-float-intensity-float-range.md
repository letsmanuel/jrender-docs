# `addPointLight`

**Declaring type:** [Scene](./README.md)  
**Visibility:** `public`  
**Signature:** `public PointLight addPointLight(Vector3f position, Vector3f color, float intensity, float range)`

## What it does

This function belongs to `game.letsmanuel.engine.scene.Scene` and performs the operation represented by `addPointLight`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `position` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `color` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `intensity` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `range` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Vector3f position`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Vector3f color`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float intensity`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float range`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `PointLight`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
PointLight result = instance.addPointLight(position, color, intensity, range);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
PointLight result = instance.addPointLight(position, color, intensity, range);
```

## Agent instructions

When modifying code that calls `addPointLight`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


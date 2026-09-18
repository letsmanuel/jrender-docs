# `t`

**Declaring type:** [RayHit](./README.md)  
**Visibility:** `public`  
**Signature:** `public RayHi t(GameObject object, float distance, Vector3f point, Vector3f normal)`

## What it does

This function belongs to `game.letsmanuel.engine.ray.RayHit` and performs the operation represented by `t`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `object` | `GameObject` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `distance` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `point` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `normal` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `GameObject object`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float distance`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Vector3f point`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Vector3f normal`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `RayHi`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
RayHi result = instance.t(object, distance, point, normal);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
RayHi result = instance.t(object, distance, point, normal);
```

## Agent instructions

When modifying code that calls `t`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


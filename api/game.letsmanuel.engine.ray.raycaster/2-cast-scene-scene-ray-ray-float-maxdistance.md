# `cast`

**Declaring type:** [Raycaster](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static List<RayHit> cast(Scene scene, Ray ray, float maxDistance)`

## What it does

This function belongs to `game.letsmanuel.engine.ray.Raycaster` and performs the operation represented by `cast`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `scene` | `Scene` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `ray` | `Ray` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `maxDistance` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Scene scene`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Ray ray`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float maxDistance`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `List<RayHit>`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
List<RayHit> result = instance.cast(scene, ray, maxDistance);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
List<RayHit> result = instance.cast(scene, ray, maxDistance);
```

## Agent instructions

When modifying code that calls `cast`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


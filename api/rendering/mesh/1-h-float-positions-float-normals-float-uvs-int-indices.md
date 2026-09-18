# `h`

**Declaring type:** [Mesh](./README.md)  
**Visibility:** `public`  
**Signature:** `public Mes h(float[] positions, float[] normals, float[] uvs, int[] indices)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Mesh` and performs the operation represented by `h`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `positions` | `float[]` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `normals` | `float[]` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `uvs` | `float[]` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `indices` | `int[]` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float[] positions`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float[] normals`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float[] uvs`: validate type, range, coordinate space, ownership, and nullability before calling.
- `int[] indices`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Mes`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Mes result = instance.h(positions, normals, uvs, indices);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Mes result = instance.h(positions, normals, uvs, indices);
```

## Agent instructions

When modifying code that calls `h`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


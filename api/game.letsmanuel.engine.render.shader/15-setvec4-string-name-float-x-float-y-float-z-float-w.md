# `setVec4`

**Declaring type:** [Shader](./README.md)  
**Visibility:** `public`  
**Signature:** `public void setVec4(String name, float x, float y, float z, float w)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Shader` and performs the operation represented by `setVec4`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `name` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `x` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `y` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `z` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `w` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String name`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float x`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float y`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float z`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float w`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.setVec4(name, x, y, z, w);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.setVec4(name, x, y, z, w);
```

## Agent instructions

When modifying code that calls `setVec4`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


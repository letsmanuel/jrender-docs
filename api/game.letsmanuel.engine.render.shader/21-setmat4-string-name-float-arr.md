# `setMat4`

**Declaring type:** [Shader](./README.md)  
**Visibility:** `public`  
**Signature:** `public void setMat4(String name, float[] arr)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Shader` and performs the operation represented by `setMat4`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `name` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `arr` | `float[]` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String name`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float[] arr`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.setMat4(name, arr);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.setMat4(name, arr);
```

## Agent instructions

When modifying code that calls `setMat4`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


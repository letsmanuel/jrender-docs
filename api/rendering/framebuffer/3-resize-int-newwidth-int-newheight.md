# `resize`

**Declaring type:** [Framebuffer](./README.md)  
**Visibility:** `public`  
**Signature:** `public void resize(int newWidth, int newHeight)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Framebuffer` and performs the operation represented by `resize`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `newWidth` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `newHeight` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `int newWidth`: validate type, range, coordinate space, ownership, and nullability before calling.
- `int newHeight`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.resize(newWidth, newHeight);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.resize(newWidth, newHeight);
```

## Agent instructions

When modifying code that calls `resize`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


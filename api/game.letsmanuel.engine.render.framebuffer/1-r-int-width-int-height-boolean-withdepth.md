# `r`

**Declaring type:** [Framebuffer](./README.md)  
**Visibility:** `public`  
**Signature:** `public Framebuffe r(int width, int height, boolean withDepth)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Framebuffer` and performs the operation represented by `r`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `width` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `height` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `withDepth` | `boolean` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `int width`: validate type, range, coordinate space, ownership, and nullability before calling.
- `int height`: validate type, range, coordinate space, ownership, and nullability before calling.
- `boolean withDepth`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Framebuffe`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Framebuffe result = instance.r(width, height, withDepth);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Framebuffe result = instance.r(width, height, withDepth);
```

## Agent instructions

When modifying code that calls `r`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


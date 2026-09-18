# `depthOnly`

**Declaring type:** [Framebuffer](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static Framebuffer depthOnly(int width, int height)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Framebuffer` and performs the operation represented by `depthOnly`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `width` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `height` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `int width`: validate type, range, coordinate space, ownership, and nullability before calling.
- `int height`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Framebuffer`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Framebuffer result = instance.depthOnly(width, height);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Framebuffer result = instance.depthOnly(width, height);
```

## Agent instructions

When modifying code that calls `depthOnly`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

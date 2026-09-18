# `setColor`

**Declaring type:** [PointLight](./README.md)  
**Visibility:** `public`  
**Signature:** `public PointLight setColor(float r, float g, float b)`

## What it does

This function belongs to `game.letsmanuel.engine.light.PointLight` and performs the operation represented by `setColor`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `r` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `g` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `b` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float r`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float g`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float b`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `PointLight`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
PointLight result = instance.setColor(r, g, b);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
PointLight result = instance.setColor(r, g, b);
```

## Agent instructions

When modifying code that calls `setColor`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

# `setPosition`

**Declaring type:** [PointLight](./README.md)  
**Visibility:** `public`  
**Signature:** `public PointLight setPosition(float x, float y, float z)`

## What it does

This function belongs to `game.letsmanuel.engine.light.PointLight` and performs the operation represented by `setPosition`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `x` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `y` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `z` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float x`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float y`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float z`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `PointLight`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
PointLight result = instance.setPosition(x, y, z);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
PointLight result = instance.setPosition(x, y, z);
```

## Agent instructions

When modifying code that calls `setPosition`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

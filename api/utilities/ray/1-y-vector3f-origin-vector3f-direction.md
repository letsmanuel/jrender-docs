# `y`

**Declaring type:** [Ray](./README.md)  
**Visibility:** `public`  
**Signature:** `public Ra y(Vector3f origin, Vector3f direction)`

## What it does

This function belongs to `game.letsmanuel.engine.ray.Ray` and performs the operation represented by `y`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `origin` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `direction` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Vector3f origin`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Vector3f direction`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Ra`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Ra result = instance.y(origin, direction);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Ra result = instance.y(origin, direction);
```

## Agent instructions

When modifying code that calls `y`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

# `procedural`

**Declaring type:** [Skybox](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static Skybox procedural(Vector3f topColor, Vector3f bottomColor)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Skybox` and performs the operation represented by `procedural`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `topColor` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `bottomColor` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Vector3f topColor`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Vector3f bottomColor`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Skybox`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Skybox result = instance.procedural(topColor, bottomColor);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Skybox result = instance.procedural(topColor, bottomColor);
```

## Agent instructions

When modifying code that calls `procedural`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

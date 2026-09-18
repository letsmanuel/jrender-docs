# `setFloat`

**Declaring type:** [Shader](./README.md)  
**Visibility:** `public`  
**Signature:** `public void setFloat(String name, float v)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Shader` and performs the operation represented by `setFloat`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `name` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `v` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String name`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float v`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.setFloat(name, v);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.setFloat(name, v);
```

## Agent instructions

When modifying code that calls `setFloat`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

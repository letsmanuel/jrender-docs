# `setUiTimeScale`

**Declaring type:** [Engine](./README.md)  
**Visibility:** `public`  
**Signature:** `public Engine setUiTimeScale(float scale)`

## What it does

This function belongs to `game.letsmanuel.engine.Engine` and performs the operation represented by `setUiTimeScale`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `scale` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float scale`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Engine`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Engine result = instance.setUiTimeScale(scale);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Engine result = instance.setUiTimeScale(scale);
```

## Agent instructions

When modifying code that calls `setUiTimeScale`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

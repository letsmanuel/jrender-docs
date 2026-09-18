# `update`

**Declaring type:** [Gui](./README.md)  
**Visibility:** `public`  
**Signature:** `public void update(Window window, float dt)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.Gui` and performs the operation represented by `update`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `window` | `Window` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `dt` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Window window`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float dt`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.update(window, dt);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.update(window, dt);
```

## Agent instructions

When modifying code that calls `update`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

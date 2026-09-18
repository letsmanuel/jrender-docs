# `setTrackColors`

**Declaring type:** [GuiToggle](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiToggle setTrackColors(float offR, float offG, float offB,
                                    float onR, float onG, float onB)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiToggle` and performs the operation represented by `setTrackColors`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `offR` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `offG` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `offB` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `onR` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `onG` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `onB` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float offR`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float offG`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float offB`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float onR`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float onG`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float onB`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiToggle`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiToggle result = instance.setTrackColors(offR, offG, offB, onR, onG, onB);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiToggle result = instance.setTrackColors(offR, offG, offB, onR, onG, onB);
```

## Agent instructions

When modifying code that calls `setTrackColors`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

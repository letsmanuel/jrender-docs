# `setScrollInsets`

**Declaring type:** [GuiScrollFrame](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiScrollFrame setScrollInsets(float top, float bottom, float left, float right)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiScrollFrame` and performs the operation represented by `setScrollInsets`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `top` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `bottom` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `left` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `right` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float top`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float bottom`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float left`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float right`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiScrollFrame`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiScrollFrame result = instance.setScrollInsets(top, bottom, left, right);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiScrollFrame result = instance.setScrollInsets(top, bottom, left, right);
```

## Agent instructions

When modifying code that calls `setScrollInsets`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

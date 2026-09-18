# `y`

**Declaring type:** [GuiCategory](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiCategor y(String title, GuiFont font, float x, float y, float width)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiCategory` and performs the operation represented by `y`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `title` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `font` | `GuiFont` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `x` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `y` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `width` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String title`: validate type, range, coordinate space, ownership, and nullability before calling.
- `GuiFont font`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float x`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float y`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float width`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiCategor`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiCategor result = instance.y(title, font, x, y, width);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiCategor result = instance.y(title, font, x, y, width);
```

## Agent instructions

When modifying code that calls `y`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

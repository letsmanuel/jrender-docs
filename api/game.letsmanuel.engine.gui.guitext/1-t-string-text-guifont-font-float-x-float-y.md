# `t`

**Declaring type:** [GuiText](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiTex t(String text, GuiFont font, float x, float y)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiText` and performs the operation represented by `t`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `text` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `font` | `GuiFont` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `x` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `y` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String text`: validate type, range, coordinate space, ownership, and nullability before calling.
- `GuiFont font`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float x`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float y`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiTex`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiTex result = instance.t(text, font, x, y);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiTex result = instance.t(text, font, x, y);
```

## Agent instructions

When modifying code that calls `t`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


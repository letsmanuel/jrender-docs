# `n`

**Declaring type:** [GuiButton](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiButto n(String label, GuiFont font, float x, float y, float w, float h)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiButton` and performs the operation represented by `n`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `label` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `font` | `GuiFont` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `x` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `y` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `w` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `h` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String label`: validate type, range, coordinate space, ownership, and nullability before calling.
- `GuiFont font`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float x`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float y`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float w`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float h`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiButto`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiButto result = instance.n(label, font, x, y, w, h);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiButto result = instance.n(label, font, x, y, w, h);
```

## Agent instructions

When modifying code that calls `n`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


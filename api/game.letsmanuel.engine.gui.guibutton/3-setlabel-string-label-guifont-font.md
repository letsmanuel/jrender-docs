# `setLabel`

**Declaring type:** [GuiButton](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiButton setLabel(String label, GuiFont font)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiButton` and performs the operation represented by `setLabel`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `label` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `font` | `GuiFont` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String label`: validate type, range, coordinate space, ownership, and nullability before calling.
- `GuiFont font`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiButton`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiButton result = instance.setLabel(label, font);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiButton result = instance.setLabel(label, font);
```

## Agent instructions

When modifying code that calls `setLabel`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


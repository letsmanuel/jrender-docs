# `setFont`

**Declaring type:** [GuiText](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiText setFont(GuiFont font)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiText` and performs the operation represented by `setFont`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `font` | `GuiFont` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `GuiFont font`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiText`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiText result = instance.setFont(font);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiText result = instance.setFont(font);
```

## Agent instructions

When modifying code that calls `setFont`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


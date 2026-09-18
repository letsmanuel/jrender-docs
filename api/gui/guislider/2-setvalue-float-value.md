# `setValue`

**Declaring type:** [GuiSlider](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiSlider setValue(float value)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiSlider` and performs the operation represented by `setValue`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `value` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float value`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiSlider`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiSlider result = instance.setValue(value);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiSlider result = instance.setValue(value);
```

## Agent instructions

When modifying code that calls `setValue`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


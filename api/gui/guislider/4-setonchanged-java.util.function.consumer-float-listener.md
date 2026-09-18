# `setOnChanged`

**Declaring type:** [GuiSlider](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiSlider setOnChanged(java.util.function.Consumer<Float> listener)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiSlider` and performs the operation represented by `setOnChanged`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `listener` | `java.util.function.Consumer<Float>` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `java.util.function.Consumer<Float> listener`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiSlider`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiSlider result = instance.setOnChanged(listener);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiSlider result = instance.setOnChanged(listener);
```

## Agent instructions

When modifying code that calls `setOnChanged`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


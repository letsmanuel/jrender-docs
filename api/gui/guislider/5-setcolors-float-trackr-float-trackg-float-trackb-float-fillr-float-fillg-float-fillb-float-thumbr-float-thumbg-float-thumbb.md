# `setColors`

**Declaring type:** [GuiSlider](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiSlider setColors(float trackR, float trackG, float trackB,
                               float fillR, float fillG, float fillB,
                               float thumbR, float thumbG, float thumbB)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiSlider` and performs the operation represented by `setColors`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `trackR` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `trackG` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `trackB` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `fillR` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `fillG` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `fillB` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `thumbR` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `thumbG` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `thumbB` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float trackR`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float trackG`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float trackB`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float fillR`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float fillG`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float fillB`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float thumbR`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float thumbG`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float thumbB`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiSlider`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiSlider result = instance.setColors(trackR, trackG, trackB, fillR, fillG, fillB, thumbR, thumbG, thumbB);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiSlider result = instance.setColors(trackR, trackG, trackB, fillR, fillG, fillB, thumbR, thumbG, thumbB);
```

## Agent instructions

When modifying code that calls `setColors`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


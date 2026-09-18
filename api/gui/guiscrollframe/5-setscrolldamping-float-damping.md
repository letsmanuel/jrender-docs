# `setScrollDamping`

**Declaring type:** [GuiScrollFrame](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiScrollFrame setScrollDamping(float damping)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiScrollFrame` and performs the operation represented by `setScrollDamping`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `damping` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float damping`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiScrollFrame`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiScrollFrame result = instance.setScrollDamping(damping);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiScrollFrame result = instance.setScrollDamping(damping);
```

## Agent instructions

When modifying code that calls `setScrollDamping`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


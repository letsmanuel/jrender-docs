# `setScrollSpeed`

**Declaring type:** [GuiScrollFrame](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiScrollFrame setScrollSpeed(float speed)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiScrollFrame` and performs the operation represented by `setScrollSpeed`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `speed` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float speed`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiScrollFrame`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiScrollFrame result = instance.setScrollSpeed(speed);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiScrollFrame result = instance.setScrollSpeed(speed);
```

## Agent instructions

When modifying code that calls `setScrollSpeed`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


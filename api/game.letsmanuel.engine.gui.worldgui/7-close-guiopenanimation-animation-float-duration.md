# `close`

**Declaring type:** [WorldGui](./README.md)  
**Visibility:** `public`  
**Signature:** `public WorldGui close(GuiOpenAnimation animation, float duration)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.WorldGui` and performs the operation represented by `close`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `animation` | `GuiOpenAnimation` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `duration` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `GuiOpenAnimation animation`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float duration`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `WorldGui`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
WorldGui result = instance.close(animation, duration);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
WorldGui result = instance.close(animation, duration);
```

## Agent instructions

When modifying code that calls `close`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


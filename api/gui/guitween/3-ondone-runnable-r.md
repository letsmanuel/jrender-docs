# `onDone`

**Declaring type:** [GuiTween](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiTween onDone(Runnable r)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiTween` and performs the operation represented by `onDone`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `r` | `Runnable` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Runnable r`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiTween`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiTween result = instance.onDone(r);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiTween result = instance.onDone(r);
```

## Agent instructions

When modifying code that calls `onDone`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


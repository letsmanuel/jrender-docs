# `n`

**Declaring type:** [GuiTween](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiTwee n(Prop prop, float from, float to, float duration, Easing easing)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiTween` and performs the operation represented by `n`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `prop` | `Prop` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `from` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `to` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `duration` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `easing` | `Easing` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Prop prop`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float from`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float to`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float duration`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Easing easing`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiTwee`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiTwee result = instance.n(prop, from, to, duration, easing);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiTwee result = instance.n(prop, from, to, duration, easing);
```

## Agent instructions

When modifying code that calls `n`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


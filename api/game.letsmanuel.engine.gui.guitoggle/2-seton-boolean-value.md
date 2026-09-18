# `setOn`

**Declaring type:** [GuiToggle](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiToggle setOn(boolean value)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiToggle` and performs the operation represented by `setOn`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `value` | `boolean` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `boolean value`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiToggle`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiToggle result = instance.setOn(value);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiToggle result = instance.setOn(value);
```

## Agent instructions

When modifying code that calls `setOn`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


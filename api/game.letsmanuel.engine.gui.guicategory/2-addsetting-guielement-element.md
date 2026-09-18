# `addSetting`

**Declaring type:** [GuiCategory](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiCategory addSetting(GuiElement element)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiCategory` and performs the operation represented by `addSetting`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `element` | `GuiElement` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `GuiElement element`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiCategory`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiCategory result = instance.addSetting(element);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiCategory result = instance.addSetting(element);
```

## Agent instructions

When modifying code that calls `addSetting`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


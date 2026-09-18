# `setExpanded`

**Declaring type:** [GuiCategory](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiCategory setExpanded(boolean expanded)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiCategory` and performs the operation represented by `setExpanded`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `expanded` | `boolean` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `boolean expanded`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiCategory`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiCategory result = instance.setExpanded(expanded);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiCategory result = instance.setExpanded(expanded);
```

## Agent instructions

When modifying code that calls `setExpanded`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

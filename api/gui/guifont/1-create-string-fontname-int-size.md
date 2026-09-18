# `create`

**Declaring type:** [GuiFont](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static GuiFont create(String fontName, int size)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiFont` and performs the operation represented by `create`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `fontName` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `size` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String fontName`: validate type, range, coordinate space, ownership, and nullability before calling.
- `int size`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GuiFont`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiFont result = instance.create(fontName, size);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiFont result = instance.create(fontName, size);
```

## Agent instructions

When modifying code that calls `create`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

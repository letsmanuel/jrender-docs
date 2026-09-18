# `content`

**Declaring type:** [GuiCategory](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiFrame content()`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiCategory` and performs the operation represented by `content`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `GuiFrame`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiFrame result = instance.content();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiFrame result = instance.content();
```

## Agent instructions

When modifying code that calls `content`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

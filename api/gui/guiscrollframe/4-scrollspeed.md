# `scrollSpeed`

**Declaring type:** [GuiScrollFrame](./README.md)  
**Visibility:** `public`  
**Signature:** `public float scrollSpeed()`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiScrollFrame` and performs the operation represented by `scrollSpeed`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `float`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
float result = instance.scrollSpeed();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
float result = instance.scrollSpeed();
```

## Agent instructions

When modifying code that calls `scrollSpeed`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

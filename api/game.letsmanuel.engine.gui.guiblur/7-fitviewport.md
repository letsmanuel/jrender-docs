# `fitViewport`

**Declaring type:** [GuiBlur](./README.md)  
**Visibility:** `public`  
**Signature:** `public GuiBlur fitViewport()`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiBlur` and performs the operation represented by `fitViewport`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `GuiBlur`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GuiBlur result = instance.fitViewport();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GuiBlur result = instance.fitViewport();
```

## Agent instructions

When modifying code that calls `fitViewport`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


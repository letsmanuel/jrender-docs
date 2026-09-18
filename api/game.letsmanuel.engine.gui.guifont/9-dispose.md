# `dispose`

**Declaring type:** [GuiFont](./README.md)  
**Visibility:** `public`  
**Signature:** `public void dispose()`

## What it does

This function belongs to `game.letsmanuel.engine.gui.GuiFont` and performs the operation represented by `dispose`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.dispose();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.dispose();
```

## Agent instructions

When modifying code that calls `dispose`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


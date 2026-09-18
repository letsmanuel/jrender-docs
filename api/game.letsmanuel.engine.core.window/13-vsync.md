# `vsync`

**Declaring type:** [Window](./README.md)  
**Visibility:** `public`  
**Signature:** `public boolean vsync()`

## What it does

This function belongs to `game.letsmanuel.engine.core.Window` and performs the operation represented by `vsync`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `boolean`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
boolean result = instance.vsync();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
boolean result = instance.vsync();
```

## Agent instructions

When modifying code that calls `vsync`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


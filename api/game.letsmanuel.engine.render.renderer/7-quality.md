# `quality`

**Declaring type:** [Renderer](./README.md)  
**Visibility:** `public`  
**Signature:** `public int quality()`

## What it does

This function belongs to `game.letsmanuel.engine.render.Renderer` and performs the operation represented by `quality`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `int`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
int result = instance.quality();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
int result = instance.quality();
```

## Agent instructions

When modifying code that calls `quality`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


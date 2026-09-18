# `positions`

**Declaring type:** [Mesh](./README.md)  
**Visibility:** `public`  
**Signature:** `public float[] positions()`

## What it does

This function belongs to `game.letsmanuel.engine.render.Mesh` and performs the operation represented by `positions`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `float[]`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
float[] result = instance.positions();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
float[] result = instance.positions();
```

## Agent instructions

When modifying code that calls `positions`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


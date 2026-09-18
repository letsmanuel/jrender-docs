# `skyTop`

**Declaring type:** [Scene](./README.md)  
**Visibility:** `public`  
**Signature:** `public Vector3f skyTop()`

## What it does

This function belongs to `game.letsmanuel.engine.scene.Scene` and performs the operation represented by `skyTop`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `Vector3f`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Vector3f result = instance.skyTop();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Vector3f result = instance.skyTop();
```

## Agent instructions

When modifying code that calls `skyTop`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


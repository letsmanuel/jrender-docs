# `localMatrix`

**Declaring type:** [Transform](./README.md)  
**Visibility:** `public`  
**Signature:** `public Matrix4f localMatrix()`

## What it does

This function belongs to `game.letsmanuel.engine.core.Transform` and performs the operation represented by `localMatrix`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `Matrix4f`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Matrix4f result = instance.localMatrix();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Matrix4f result = instance.localMatrix();
```

## Agent instructions

When modifying code that calls `localMatrix`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


# `cube`

**Declaring type:** [MeshFactory](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static Mesh cube()`

## What it does

This function belongs to `game.letsmanuel.engine.render.MeshFactory` and performs the operation represented by `cube`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `Mesh`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Mesh result = instance.cube();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Mesh result = instance.cube();
```

## Agent instructions

When modifying code that calls `cube`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


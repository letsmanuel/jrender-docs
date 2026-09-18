# `sun`

**Declaring type:** [Scene](./README.md)  
**Visibility:** `public`  
**Signature:** `public DirectionalLight sun()`

## What it does

This function belongs to `game.letsmanuel.engine.scene.Scene` and performs the operation represented by `sun`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `DirectionalLight`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
DirectionalLight result = instance.sun();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
DirectionalLight result = instance.sun();
```

## Agent instructions

When modifying code that calls `sun`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


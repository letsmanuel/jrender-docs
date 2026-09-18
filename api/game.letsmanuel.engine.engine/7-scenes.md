# `scenes`

**Declaring type:** [Engine](./README.md)  
**Visibility:** `public`  
**Signature:** `public SceneManager scenes()`

## What it does

This function belongs to `game.letsmanuel.engine.Engine` and performs the operation represented by `scenes`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `SceneManager`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
SceneManager result = instance.scenes();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
SceneManager result = instance.scenes();
```

## Agent instructions

When modifying code that calls `scenes`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


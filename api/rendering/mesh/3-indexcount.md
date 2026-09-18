# `indexCount`

**Declaring type:** [Mesh](./README.md)  
**Visibility:** `public`  
**Signature:** `public int indexCount()`

## What it does

This function belongs to `game.letsmanuel.engine.render.Mesh` and performs the operation represented by `indexCount`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `int`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
int result = instance.indexCount();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
int result = instance.indexCount();
```

## Agent instructions

When modifying code that calls `indexCount`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

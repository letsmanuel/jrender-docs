# `right`

**Declaring type:** [Camera](./README.md)  
**Visibility:** `public`  
**Signature:** `public Vector3f right()`

## What it does

This function belongs to `game.letsmanuel.engine.core.Camera` and performs the operation represented by `right`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

This function takes no arguments.

## Return value

Returns a value of type `Vector3f`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Vector3f result = instance.right();
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Vector3f result = instance.right();
```

## Agent instructions

When modifying code that calls `right`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

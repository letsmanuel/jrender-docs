# `setPitch`

**Declaring type:** [Camera](./README.md)  
**Visibility:** `public`  
**Signature:** `public Camera setPitch(float deg)`

## What it does

This function belongs to `game.letsmanuel.engine.core.Camera` and performs the operation represented by `setPitch`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `deg` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float deg`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Camera`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Camera result = instance.setPitch(deg);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Camera result = instance.setPitch(deg);
```

## Agent instructions

When modifying code that calls `setPitch`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


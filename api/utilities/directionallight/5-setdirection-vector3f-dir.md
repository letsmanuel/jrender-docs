# `setDirection`

**Declaring type:** [DirectionalLight](./README.md)  
**Visibility:** `public`  
**Signature:** `public DirectionalLight setDirection(Vector3f dir)`

## What it does

This function belongs to `game.letsmanuel.engine.light.DirectionalLight` and performs the operation represented by `setDirection`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `dir` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Vector3f dir`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `DirectionalLight`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
DirectionalLight result = instance.setDirection(dir);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
DirectionalLight result = instance.setDirection(dir);
```

## Agent instructions

When modifying code that calls `setDirection`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


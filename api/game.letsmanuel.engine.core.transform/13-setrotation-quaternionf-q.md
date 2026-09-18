# `setRotation`

**Declaring type:** [Transform](./README.md)  
**Visibility:** `public`  
**Signature:** `public Transform setRotation(Quaternionf q)`

## What it does

This function belongs to `game.letsmanuel.engine.core.Transform` and performs the operation represented by `setRotation`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `q` | `Quaternionf` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Quaternionf q`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Transform`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Transform result = instance.setRotation(q);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Transform result = instance.setRotation(q);
```

## Agent instructions

When modifying code that calls `setRotation`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


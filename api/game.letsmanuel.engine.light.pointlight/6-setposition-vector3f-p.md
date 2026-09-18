# `setPosition`

**Declaring type:** [PointLight](./README.md)  
**Visibility:** `public`  
**Signature:** `public PointLight setPosition(Vector3f p)`

## What it does

This function belongs to `game.letsmanuel.engine.light.PointLight` and performs the operation represented by `setPosition`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `p` | `Vector3f` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Vector3f p`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `PointLight`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
PointLight result = instance.setPosition(p);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
PointLight result = instance.setPosition(p);
```

## Agent instructions

When modifying code that calls `setPosition`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


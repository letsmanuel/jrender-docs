# `removePointLight`

**Declaring type:** [Scene](./README.md)  
**Visibility:** `public`  
**Signature:** `public void removePointLight(PointLight light)`

## What it does

This function belongs to `game.letsmanuel.engine.scene.Scene` and performs the operation represented by `removePointLight`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `light` | `PointLight` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `PointLight light`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.removePointLight(light);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.removePointLight(light);
```

## Agent instructions

When modifying code that calls `removePointLight`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


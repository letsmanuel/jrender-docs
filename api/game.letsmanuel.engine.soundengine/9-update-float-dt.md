# `update`

**Declaring type:** [SoundEngine](./README.md)  
**Visibility:** `public`  
**Signature:** `public void update(float dt)`

## What it does

This function belongs to `game.letsmanuel.engine.SoundEngine` and performs the operation represented by `update`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `dt` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float dt`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.update(dt);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.update(dt);
```

## Agent instructions

When modifying code that calls `update`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


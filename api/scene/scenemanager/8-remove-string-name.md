# `remove`

**Declaring type:** [SceneManager](./README.md)  
**Visibility:** `public`  
**Signature:** `public void remove(String name)`

## What it does

This function belongs to `game.letsmanuel.engine.scene.SceneManager` and performs the operation represented by `remove`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `name` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String name`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.remove(name);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.remove(name);
```

## Agent instructions

When modifying code that calls `remove`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


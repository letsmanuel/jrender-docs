# `setSize`

**Declaring type:** [GameObject](./README.md)  
**Visibility:** `public`  
**Signature:** `public GameObject setSize(float s)`

## What it does

This function belongs to `game.letsmanuel.engine.object.GameObject` and performs the operation represented by `setSize`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `s` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float s`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GameObject`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GameObject result = instance.setSize(s);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GameObject result = instance.setSize(s);
```

## Agent instructions

When modifying code that calls `setSize`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

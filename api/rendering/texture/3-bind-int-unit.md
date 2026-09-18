# `bind`

**Declaring type:** [Texture](./README.md)  
**Visibility:** `public`  
**Signature:** `public void bind(int unit)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Texture` and performs the operation represented by `bind`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `unit` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `int unit`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.bind(unit);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.bind(unit);
```

## Agent instructions

When modifying code that calls `bind`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

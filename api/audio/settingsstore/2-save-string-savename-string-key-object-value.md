# `save`

**Declaring type:** [SettingsStore](./README.md)  
**Visibility:** `public`  
**Signature:** `public void save(String saveName, String key, Object value)`

## What it does

This function belongs to `game.letsmanuel.engine.SettingsStore` and performs the operation represented by `save`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `saveName` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `key` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `value` | `Object` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String saveName`: validate type, range, coordinate space, ownership, and nullability before calling.
- `String key`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Object value`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Does not return a value.

## Code sample

```java
// Obtain or construct the owning instance before this call.
instance.save(saveName, key, value);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
instance.save(saveName, key, value);
```

## Agent instructions

When modifying code that calls `save`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

# `keyDown`

**Declaring type:** [Window](./README.md)  
**Visibility:** `public`  
**Signature:** `public boolean keyDown(int key)`

## What it does

This function belongs to `game.letsmanuel.engine.core.Window` and performs the operation represented by `keyDown`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `key` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `int key`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `boolean`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
boolean result = instance.keyDown(key);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
boolean result = instance.keyDown(key);
```

## Agent instructions

When modifying code that calls `keyDown`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


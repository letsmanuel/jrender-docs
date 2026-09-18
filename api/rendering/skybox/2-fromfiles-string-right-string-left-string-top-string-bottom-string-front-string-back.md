# `fromFiles`

**Declaring type:** [Skybox](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static Skybox fromFiles(String right, String left, String top, String bottom, String front, String back)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Skybox` and performs the operation represented by `fromFiles`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `right` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `left` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `top` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `bottom` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `front` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `back` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String right`: validate type, range, coordinate space, ownership, and nullability before calling.
- `String left`: validate type, range, coordinate space, ownership, and nullability before calling.
- `String top`: validate type, range, coordinate space, ownership, and nullability before calling.
- `String bottom`: validate type, range, coordinate space, ownership, and nullability before calling.
- `String front`: validate type, range, coordinate space, ownership, and nullability before calling.
- `String back`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Skybox`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Skybox result = instance.fromFiles(right, left, top, bottom, front, back);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Skybox result = instance.fromFiles(right, left, top, bottom, front, back);
```

## Agent instructions

When modifying code that calls `fromFiles`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


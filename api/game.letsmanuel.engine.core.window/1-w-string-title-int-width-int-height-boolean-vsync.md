# `w`

**Declaring type:** [Window](./README.md)  
**Visibility:** `public`  
**Signature:** `public Windo w(String title, int width, int height, boolean vsync)`

## What it does

This function belongs to `game.letsmanuel.engine.core.Window` and performs the operation represented by `w`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `title` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `width` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `height` | `int` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `vsync` | `boolean` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String title`: validate type, range, coordinate space, ownership, and nullability before calling.
- `int width`: validate type, range, coordinate space, ownership, and nullability before calling.
- `int height`: validate type, range, coordinate space, ownership, and nullability before calling.
- `boolean vsync`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Windo`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Windo result = instance.w(title, width, height, vsync);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Windo result = instance.w(title, width, height, vsync);
```

## Agent instructions

When modifying code that calls `w`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


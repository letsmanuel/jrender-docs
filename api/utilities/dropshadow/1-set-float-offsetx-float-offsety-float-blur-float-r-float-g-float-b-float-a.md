# `set`

**Declaring type:** [DropShadow](./README.md)  
**Visibility:** `public`  
**Signature:** `public DropShadow set(float offsetX, float offsetY, float blur, float r, float g, float b, float a)`

## What it does

This function belongs to `game.letsmanuel.engine.gui.DropShadow` and performs the operation represented by `set`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `offsetX` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `offsetY` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `blur` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `r` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `g` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `b` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `a` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `float offsetX`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float offsetY`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float blur`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float r`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float g`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float b`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float a`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `DropShadow`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
DropShadow result = instance.set(offsetX, offsetY, blur, r, g, b, a);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
DropShadow result = instance.set(offsetX, offsetY, blur, r, g, b, a);
```

## Agent instructions

When modifying code that calls `set`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


# `r`

**Declaring type:** [Renderer](./README.md)  
**Visibility:** `public`  
**Signature:** `public Rendere r(Window window)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Renderer` and performs the operation represented by `r`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `window` | `Window` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Window window`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Rendere`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Rendere result = instance.r(window);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Rendere result = instance.r(window);
```

## Agent instructions

When modifying code that calls `r`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


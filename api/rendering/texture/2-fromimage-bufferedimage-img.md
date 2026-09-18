# `fromImage`

**Declaring type:** [Texture](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static Texture fromImage(BufferedImage img)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Texture` and performs the operation represented by `fromImage`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `img` | `BufferedImage` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `BufferedImage img`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Texture`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Texture result = instance.fromImage(img);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Texture result = instance.fromImage(img);
```

## Agent instructions

When modifying code that calls `fromImage`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


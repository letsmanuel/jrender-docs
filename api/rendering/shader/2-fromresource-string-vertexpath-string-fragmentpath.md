# `fromResource`

**Declaring type:** [Shader](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static Shader fromResource(String vertexPath, String fragmentPath)`

## What it does

This function belongs to `game.letsmanuel.engine.render.Shader` and performs the operation represented by `fromResource`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `vertexPath` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `fragmentPath` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String vertexPath`: validate type, range, coordinate space, ownership, and nullability before calling.
- `String fragmentPath`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Shader`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Shader result = instance.fromResource(vertexPath, fragmentPath);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Shader result = instance.fromResource(vertexPath, fragmentPath);
```

## Agent instructions

When modifying code that calls `fromResource`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

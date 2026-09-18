# `load`

**Declaring type:** [OBJLoader](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static Mesh load(String objContent)`

## What it does

This function belongs to `game.letsmanuel.engine.render.OBJLoader` and performs the operation represented by `load`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `objContent` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String objContent`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Mesh`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Mesh result = instance.load(objContent);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Mesh result = instance.load(objContent);
```

## Agent instructions

When modifying code that calls `load`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


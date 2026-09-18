# `setMesh`

**Declaring type:** [GameObject](./README.md)  
**Visibility:** `public`  
**Signature:** `public GameObject setMesh(Mesh mesh)`

## What it does

This function belongs to `game.letsmanuel.engine.object.GameObject` and performs the operation represented by `setMesh`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `mesh` | `Mesh` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Mesh mesh`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GameObject`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GameObject result = instance.setMesh(mesh);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GameObject result = instance.setMesh(mesh);
```

## Agent instructions

When modifying code that calls `setMesh`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


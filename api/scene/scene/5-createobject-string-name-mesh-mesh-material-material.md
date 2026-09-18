# `createObject`

**Declaring type:** [Scene](./README.md)  
**Visibility:** `public`  
**Signature:** `public GameObject createObject(String name, Mesh mesh, Material material)`

## What it does

This function belongs to `game.letsmanuel.engine.scene.Scene` and performs the operation represented by `createObject`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `name` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `mesh` | `Mesh` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `material` | `Material` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String name`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Mesh mesh`: validate type, range, coordinate space, ownership, and nullability before calling.
- `Material material`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `GameObject`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
GameObject result = instance.createObject(name, mesh, material);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
GameObject result = instance.createObject(name, mesh, material);
```

## Agent instructions

When modifying code that calls `createObject`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


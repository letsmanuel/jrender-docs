# `screenRay`

**Declaring type:** [Raycaster](./README.md)  
**Visibility:** `public static`  
**Signature:** `public static Ray screenRay(Camera camera, float screenX, float screenY, float screenWidth, float screenHeight)`

## What it does

This function belongs to `game.letsmanuel.engine.ray.Raycaster` and performs the operation represented by `screenRay`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `camera` | `Camera` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `screenX` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `screenY` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `screenWidth` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |
| `screenHeight` | `float` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Camera camera`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float screenX`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float screenY`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float screenWidth`: validate type, range, coordinate space, ownership, and nullability before calling.
- `float screenHeight`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Ray`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Ray result = instance.screenRay(camera, screenX, screenY, screenWidth, screenHeight);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Ray result = instance.screenRay(camera, screenX, screenY, screenWidth, screenHeight);
```

## Agent instructions

When modifying code that calls `screenRay`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


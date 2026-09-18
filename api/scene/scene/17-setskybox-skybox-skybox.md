# `setSkybox`

**Declaring type:** [Scene](./README.md)  
**Visibility:** `public`  
**Signature:** `public Scene setSkybox(Skybox skybox)`

## What it does

This function belongs to `game.letsmanuel.engine.scene.Scene` and performs the operation represented by `setSkybox`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `skybox` | `Skybox` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Skybox skybox`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Scene`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Scene result = instance.setSkybox(skybox);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Scene result = instance.setSkybox(skybox);
```

## Agent instructions

When modifying code that calls `setSkybox`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

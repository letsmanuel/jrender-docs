# `switchTo`

**Declaring type:** [SceneManager](./README.md)  
**Visibility:** `public`  
**Signature:** `public Scene switchTo(Scene scene)`

## What it does

This function belongs to `game.letsmanuel.engine.scene.SceneManager` and performs the operation represented by `switchTo`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `scene` | `Scene` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `Scene scene`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `Scene`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
Scene result = instance.switchTo(scene);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
Scene result = instance.switchTo(scene);
```

## Agent instructions

When modifying code that calls `switchTo`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


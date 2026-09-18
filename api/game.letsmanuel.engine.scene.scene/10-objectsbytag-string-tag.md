# `objectsByTag`

**Declaring type:** [Scene](./README.md)  
**Visibility:** `public`  
**Signature:** `public List<GameObject> objectsByTag(String tag)`

## What it does

This function belongs to `game.letsmanuel.engine.scene.Scene` and performs the operation represented by `objectsByTag`. Use it according to the lifecycle and ownership rules of the declaring type.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `tag` | `String` | Caller-supplied input; verify range, units, lifecycle, and nullability. |

### Argument details

- `String tag`: validate type, range, coordinate space, ownership, and nullability before calling.

## Return value

Returns a value of type `List<GameObject>`.

## Code sample

```java
// Obtain or construct the owning instance before this call.
List<GameObject> result = instance.objectsByTag(tag);
```

## Common issues

- Calling before the owning subsystem is initialized.
- Passing values in the wrong coordinate space, unit, or range.
- Retaining native resources after their owner is disposed.
- Assuming a fluent return when the declared return type is `void`.

## Template

```java
List<GameObject> result = instance.objectsByTag(tag);
```

## Agent instructions

When modifying code that calls `objectsByTag`, preserve argument order and types, search existing call sites first, keep lifecycle ownership explicit, and update this page if behavior changes.


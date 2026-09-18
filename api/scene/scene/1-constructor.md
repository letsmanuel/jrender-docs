# `Scene` constructor

**Declaring type:** [Scene](./README.md)  
**Signature:** `public Scene(String name)`

## What it does

Creates a new `Scene` instance and initializes its required constructor state.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `name` | `String` | Required constructor input. |

## Return value

Returns the new `Scene` instance.

## Code sample

```java
Scene instance = new Scene(String name);
```

## Common issues

- Supplying null or invalid dimensions, paths, IDs, or native configuration.
- Constructing the object before its required engine subsystem is initialized.

## Template

```java
Scene instance = new Scene(String name);
```

## Agent instructions

Preserve constructor argument order, validate inputs at the call site, and follow the declaring type lifecycle rules.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

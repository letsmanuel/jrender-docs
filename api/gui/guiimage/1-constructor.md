# `GuiImage` constructor

**Declaring type:** [GuiImage](./README.md)  
**Signature:** `public GuiImage(Texture texture, float x, float y, float w, float h)`

## What it does

Creates a new `GuiImage` instance and initializes its required constructor state.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `texture` | `Texture` | Required constructor input. |
| `x` | `float` | Required constructor input. |
| `y` | `float` | Required constructor input. |
| `w` | `float` | Required constructor input. |
| `h` | `float` | Required constructor input. |

## Return value

Returns the new `GuiImage` instance.

## Code sample

```java
GuiImage instance = new GuiImage(Texture texture, float x, float y, float w, float h);
```

## Common issues

- Supplying null or invalid dimensions, paths, IDs, or native configuration.
- Constructing the object before its required engine subsystem is initialized.

## Template

```java
GuiImage instance = new GuiImage(Texture texture, float x, float y, float w, float h);
```

## Agent instructions

Preserve constructor argument order, validate inputs at the call site, and follow the declaring type lifecycle rules.


### Sample hygiene

For production code, replace placeholder values with named constants or a configuration object. Keep units explicit in names such as FADE_DURATION_SECONDS, BUTTON_WIDTH, or MOVE_UNITS_PER_SECOND.

# `GuiFrame` constructor

**Declaring type:** [GuiFrame](./README.md)  
**Signature:** `public GuiFrame(float x, float y, float w, float h)`

## What it does

Creates a new `GuiFrame` instance and initializes its required constructor state.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `x` | `float` | Required constructor input. |
| `y` | `float` | Required constructor input. |
| `w` | `float` | Required constructor input. |
| `h` | `float` | Required constructor input. |

## Return value

Returns the new `GuiFrame` instance.

## Code sample

```java
GuiFrame instance = new GuiFrame(float x, float y, float w, float h);
```

## Common issues

- Supplying null or invalid dimensions, paths, IDs, or native configuration.
- Constructing the object before its required engine subsystem is initialized.

## Template

```java
GuiFrame instance = new GuiFrame(float x, float y, float w, float h);
```

## Agent instructions

Preserve constructor argument order, validate inputs at the call site, and follow the declaring type lifecycle rules.


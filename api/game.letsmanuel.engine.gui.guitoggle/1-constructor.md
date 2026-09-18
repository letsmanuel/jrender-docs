# `GuiToggle` constructor

**Declaring type:** [GuiToggle](./README.md)  
**Signature:** `public GuiToggle(float x, float y, float w, float h)`

## What it does

Creates a new `GuiToggle` instance and initializes its required constructor state.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `x` | `float` | Required constructor input. |
| `y` | `float` | Required constructor input. |
| `w` | `float` | Required constructor input. |
| `h` | `float` | Required constructor input. |

## Return value

Returns the new `GuiToggle` instance.

## Code sample

```java
GuiToggle instance = new GuiToggle(float x, float y, float w, float h);
```

## Common issues

- Supplying null or invalid dimensions, paths, IDs, or native configuration.
- Constructing the object before its required engine subsystem is initialized.

## Template

```java
GuiToggle instance = new GuiToggle(float x, float y, float w, float h);
```

## Agent instructions

Preserve constructor argument order, validate inputs at the call site, and follow the declaring type lifecycle rules.


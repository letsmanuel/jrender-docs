# `Engine` constructor

**Declaring type:** [Engine](./README.md)  
**Signature:** `public Engine(EngineConfig config)`

## What it does

Creates a new `Engine` instance and initializes its required constructor state.

## Arguments

| Name | Type | Detail |
|---|---|---|
| `config` | `EngineConfig` | Required constructor input. |

## Return value

Returns the new `Engine` instance.

## Code sample

```java
Engine instance = new Engine(EngineConfig config);
```

## Common issues

- Supplying null or invalid dimensions, paths, IDs, or native configuration.
- Constructing the object before its required engine subsystem is initialized.

## Template

```java
Engine instance = new Engine(EngineConfig config);
```

## Agent instructions

Preserve constructor argument order, validate inputs at the call site, and follow the declaring type lifecycle rules.


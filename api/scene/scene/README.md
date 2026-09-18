# Scene

**Package:** `game.letsmanuel.engine.scene`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/scene/Scene.java`

## Purpose

Scene is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [constructor](./1-constructor.md)
- [name](./2-name.md)
- [camera](./3-camera.md)
- [createObject](./4-createobject-string-name.md)
- [createObject](./5-createobject-string-name-mesh-mesh-material-material.md)
- [addObject](./6-addobject-gameobject-obj.md)
- [removeObject](./7-removeobject-string-name.md)
- [getObject](./8-getobject-string-name.md)
- [objects](./9-objects.md)
- [objectsByTag](./10-objectsbytag-string-tag.md)
- [sun](./11-sun.md)
- [addPointLight](./12-addpointlight-vector3f-position-vector3f-color-float-intensity-float-range.md)
- [addPointLight](./13-addpointlight.md)
- [removePointLight](./14-removepointlight-pointlight-light.md)
- [pointLights](./15-pointlights.md)
- [skybox](./16-skybox.md)
- [setSkybox](./17-setskybox-skybox-skybox.md)
- [setSkyColors](./18-setskycolors-vector3f-top-vector3f-bottom.md)
- [skyTop](./19-skytop.md)
- [skyBottom](./20-skybottom.md)
- [bloomThreshold](./21-bloomthreshold.md)
- [setBloomThreshold](./22-setbloomthreshold-float-v.md)
- [bloomStrength](./23-bloomstrength.md)
- [setBloomStrength](./24-setbloomstrength-float-v.md)
- [exposure](./25-exposure.md)
- [setExposure](./26-setexposure-float-v.md)




## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

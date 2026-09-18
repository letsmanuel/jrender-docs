# Engine

**Package:** `game.letsmanuel.engine`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/Engine.java`

## Purpose

Engine is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [constructor](./1-constructor.md)
- [run](./2-run-gamelogic-logic.md)
- [createScene](./3-createscene-string-name.md)
- [switchScene](./4-switchscene-string-name.md)
- [getScene](./5-getscene-string-name.md)
- [sceneExists](./6-sceneexists-string-name.md)
- [scenes](./7-scenes.md)
- [currentScene](./8-currentscene.md)
- [gui](./9-gui.md)
- [createWorldGui](./10-createworldgui-float-width-float-height.md)
- [worldGuis](./11-worldguis.md)
- [settings](./12-settings.md)
- [sound](./13-sound.md)
- [window](./14-window.md)
- [renderer](./15-renderer.md)
- [time](./16-time.md)
- [getFPS](./17-getfps.md)
- [simulationTimeScale](./18-simulationtimescale.md)
- [uiTimeScale](./19-uitimescale.md)
- [setSimulationTimeScale](./20-setsimulationtimescale-float-scale.md)
- [setUiTimeScale](./21-setuitimescale-float-scale.md)
- [setTimeScale](./22-settimescale-float-scale-boolean-includeui.md)
- [dispose](./23-dispose.md)




## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

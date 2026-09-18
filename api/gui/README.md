# GUI API

Retained-mode screen GUI, animation, tooltips, scrolling, blur, and world-anchored UI.

- [GUI root](gui/README.md)
- [GUI elements and frames](guiframe/README.md)
- [Buttons](guibutton/README.md)
- [Text and fonts](guitext/README.md)
- [Images](guiimage/README.md)
- [Sliders and toggles](guislider/README.md)
- [Scrolling](guiscrollframe/README.md)
- [Tooltips](guitooltip/README.md)
- [Blur](guiblur/README.md)
- [World GUI](worldgui/README.md)
- [Animation](guitween/README.md)
- [Open/close animation presets](guiopenanimation/README.md)
- [Hover presets](hoveranim/README.md)
- [Tooltip styling](guitooltipstyle/README.md)
- [Categories](guicategory/README.md)
- [GUI renderer](guirenderer/README.md)

## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

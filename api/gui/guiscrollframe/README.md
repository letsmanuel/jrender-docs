# GuiScrollFrame

**Package:** `game.letsmanuel.engine.gui`  
**Source path:** `engine/src/main/java/game/letsmanuel/engine/gui/GuiScrollFrame.java`

## Purpose

GuiScrollFrame is part of the Letsmanuel engine API. Each function page documents its signature, arguments, return behavior, sample usage, common issues, reusable template, and agent instructions.

## Functions

- [constructor](./1-constructor.md)
- [setContentHeight](./2-setcontentheight-float-height.md)
- [setScrollSpeed](./3-setscrollspeed-float-speed.md)
- [scrollSpeed](./4-scrollspeed.md)
- [setScrollDamping](./5-setscrolldamping-float-damping.md)
- [scrollY](./6-scrolly.md)
- [maxScroll](./7-maxscroll.md)
- [setScrollLimitToContentEnd](./8-setscrolllimittocontentend.md)
- [setScrollLimitToContent](./9-setscrolllimittocontent.md)
- [setScrollLimitHeight](./10-setscrolllimitheight-float-height.md)
- [scrollLimitMode](./11-scrolllimitmode.md)
- [scrollLimitHeight](./12-scrolllimitheight.md)
- [setScrollInsets](./13-setscrollinsets-float-top-float-bottom-float-left-float-right.md)
- [insetTop](./14-insettop.md)
- [insetBottom](./15-insetbottom.md)
- [insetLeft](./16-insetleft.md)
- [insetRight](./17-insetright.md)
- [addSticky](./18-addsticky-guielement-child.md)
- [setScrollY](./19-setscrolly-float-value.md)




## Best practices

- Keep IDs, dimensions, speeds, durations, colors, and ranges in named constants or configuration objects.
- Initialize the declaring type from the engine lifecycle stage described in the relevant theory page.
- Retain references to objects that must be updated; avoid repeated construction inside the frame loop.
- Validate external values before passing them to native rendering, audio, window, or persistence APIs.
- Preserve ownership: the subsystem that creates a native resource is responsible for releasing it.

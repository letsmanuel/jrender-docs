# GUI system

The GUI tree includes frames, text, images, buttons, sliders, toggles, blur layers, tooltips, categories, scrolling frames, and world-anchored GUIs. Any element can receive click behavior. Scroll frames support sticky controls, inertial motion, reserved insets, content-end limits, and custom-height limits. Tooltips render above normal GUI.

## Create a button

```java
GuiFont font = GuiFont.create("Trebuchet MS", 22);
GuiButton play = new GuiButton("PLAY", font, 40f, 40f, 180f, 56f);
play.setRadius(14f)
        .setHoverAnim(HoverAnim.LIFT)
        .setOnClick(() -> startGame());
engine.gui().add(play);
```

## Build a scrolling settings panel

```java
GuiScrollFrame panel = new GuiScrollFrame(240f, 80f, 640f, 520f);
panel.setContentHeight(1100f)
        .setScrollLimitToContentEnd()
        .setScrollInsets(96f, 72f, 0f, 0f);

GuiFrame content = new GuiFrame(16f, 0f, 608f, 1000f);
panel.add(content);
engine.gui().add(panel);
```

Use `addSticky` for headers and footer controls that should not move with the content.

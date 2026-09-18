# GUI system

The GUI tree includes frames, text, images, buttons, sliders, toggles, blur layers, tooltips, categories, scrolling frames, and world-anchored GUIs. Any element can receive click behavior. Scroll frames support sticky controls, inertial motion, reserved insets, content-end limits, and custom-height limits. Tooltips render above normal GUI.

## Create a button

```java
private static final String UI_FONT_NAME = "Trebuchet MS";
private static final int UI_FONT_SIZE = 22;
private static final float BUTTON_X = 40.0f;
private static final float BUTTON_Y = 40.0f;
private static final float BUTTON_WIDTH = 180.0f;
private static final float BUTTON_HEIGHT = 56.0f;

GuiFont font = GuiFont.create(UI_FONT_NAME, UI_FONT_SIZE);
GuiButton play = new GuiButton(
        "PLAY",
        font,
        BUTTON_X,
        BUTTON_Y,
        BUTTON_WIDTH,
        BUTTON_HEIGHT
);
play.setRadius(14f)
        .setHoverAnim(HoverAnim.LIFT)
        .setOnClick(() -> startGame());
engine.gui().add(play);
```

## Build a scrolling settings panel

```java
final float PANEL_X = 240.0f;
final float PANEL_Y = 80.0f;
final float PANEL_WIDTH = 640.0f;
final float PANEL_HEIGHT = 520.0f;
final float CONTENT_HEIGHT = 1100.0f;
final float HEADER_INSET = 96.0f;
final float FOOTER_INSET = 72.0f;
final float CONTENT_X = 16.0f;
final float CONTENT_WIDTH = 608.0f;
final float CONTENT_LAYOUT_HEIGHT = 1000.0f;

GuiScrollFrame panel = new GuiScrollFrame(
        PANEL_X, PANEL_Y, PANEL_WIDTH, PANEL_HEIGHT
);
panel.setContentHeight(CONTENT_HEIGHT)
        .setScrollLimitToContentEnd()
        .setScrollInsets(HEADER_INSET, FOOTER_INSET, 0.0f, 0.0f);

GuiFrame content = new GuiFrame(
        CONTENT_X, 0.0f, CONTENT_WIDTH, CONTENT_LAYOUT_HEIGHT
);
panel.add(content);
engine.gui().add(panel);
```

Use `addSticky` for headers and footer controls that should not move with the content.

## Layout recommendations

- Pick one reference resolution and keep layout constants in one UI layout class.
- Use the parent’s dimensions for alignment instead of duplicating screen coordinates.
- Reserve space with scroll insets when sticky controls occupy the frame.
- Keep visual styling separate from interaction callbacks.
- Use `setVisible` for state changes instead of removing and recreating controls every frame.

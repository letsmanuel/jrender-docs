# Coordinate spaces and layout

JRender uses different coordinate spaces for world rendering, screen GUI, and world GUI.

## World space

Meshes, lights, and camera positions use 3D world units. Camera projection converts this space to the rendered framebuffer.

## Screen GUI space

Screen GUI uses a reference resolution. The engine applies one uniform scale and letterboxes when the window aspect ratio differs. A child element’s `x` and `y` are relative to its parent’s top-left corner.

```java
GuiFrame panel = new GuiFrame(100f, 80f, 420f, 260f);
GuiText label = new GuiText("Options", font, 24f, 20f);
panel.add(label);
```

## World GUI space

`WorldGui` anchors a screen-sized GUI to a 3D position and updates it from the active camera. Use it for labels, panels, or interaction surfaces placed in the world.

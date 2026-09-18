# Audio and persistence

`SoundEngine` resolves WAV, OGG, and MP3 resources, caches decoded buffers, supports play/loop/stop, random loop offsets, volume, and smooth fades. `SettingsStore` stores typed maps and values as compressed binary files under the configured project ID. Validate loaded values and never store secrets in settings.

## Play and fade music

Put `theme.ogg`, `theme.wav`, or `theme.mp3` in `src/main/resources/sounds/`, then use the resource ID without its extension:

```java
engine.sound().setVolume("theme", 0.7f);
engine.sound().loopRandom("theme");
engine.sound().fadeIn("theme", 0.7f, 0.5f);

// Later, when leaving the menu:
engine.sound().fadeOut("theme", 0.4f);
```

## Save a settings table

```java
Map<String, Object> values = new LinkedHashMap<>();
values.put("fullscreen", true);
values.put("musicVolume", 0.7f);
values.put("scrollSpeed", 120f);

engine.settings().save("settings", values);
Map<String, Object> loaded = engine.settings().load("settings");
```

Save names and keys are application data, not a secure storage boundary. Validate loaded values before applying them.

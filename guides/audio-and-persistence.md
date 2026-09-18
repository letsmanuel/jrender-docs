# Audio and persistence

`SoundEngine` resolves WAV, OGG, and MP3 resources, caches decoded buffers, supports play/loop/stop, random loop offsets, volume, and smooth fades. `SettingsStore` stores typed maps and values as compressed binary files under the configured project ID. Validate loaded values and never store secrets in settings.

## Play and fade music

Put `theme.ogg`, `theme.wav`, or `theme.mp3` in `src/main/resources/sounds/`, then use the resource ID without its extension:

```java
private static final String MUSIC_ID = "theme";
private static final float MUSIC_VOLUME = 0.7f;
private static final float MUSIC_FADE_IN_SECONDS = 0.5f;
private static final float MUSIC_FADE_OUT_SECONDS = 0.4f;

engine.sound().setVolume(MUSIC_ID, MUSIC_VOLUME);
engine.sound().loopRandom(MUSIC_ID);
engine.sound().fadeIn(MUSIC_ID, MUSIC_VOLUME, MUSIC_FADE_IN_SECONDS);

// Later, when leaving the menu:
engine.sound().fadeOut(MUSIC_ID, MUSIC_FADE_OUT_SECONDS);
```

## Save a settings table

```java
private static final String SETTINGS_SAVE_NAME = "settings";
private static final String FULLSCREEN_KEY = "fullscreen";
private static final String MUSIC_VOLUME_KEY = "musicVolume";
private static final String SCROLL_SPEED_KEY = "scrollSpeed";

Map<String, Object> values = new LinkedHashMap<>();
values.put(FULLSCREEN_KEY, true);
values.put(MUSIC_VOLUME_KEY, 0.7f);
values.put(SCROLL_SPEED_KEY, 120.0f);

engine.settings().save(SETTINGS_SAVE_NAME, values);
Map<String, Object> loaded = engine.settings().load(SETTINGS_SAVE_NAME);
```

Save names and keys are application data, not a secure storage boundary. Validate loaded values before applying them.

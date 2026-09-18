# Audio and persistence

`SoundEngine` resolves WAV, OGG, and MP3 resources, caches decoded buffers, supports play/loop/stop, random loop offsets, volume, and smooth fades. `SettingsStore` stores typed maps and values as compressed binary files under the configured project ID. Validate loaded values and never store secrets in settings.

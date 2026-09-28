# Golden Hilal — background sound media

The filmed loops and field recordings behind the background sounds in the
Golden Hilal app (Listen → Sounds). The app downloads each file the first time
its sound is used, through jsDelivr:

    https://cdn.jsdelivr.net/gh/Winds7799/golden-hilal-media@v1/video/rain.mp4
    https://cdn.jsdelivr.net/gh/Winds7799/golden-hilal-media@v1/audio/rain.m4a

`video/` — 720×1280 H.264, no audio, 8–18 s, cut so the last frame flows into
the first. `audio/` — about two minutes each, AAC 96 kbps, loudness-matched
(−20 LUFS); the app cross-fades each loop into itself.

To change a file: add it, commit, and push a new tag (`v2`, …), then change
`MEDIA_VERSION` in `services/ambienceMedia.ts` in the app. Never move an
existing tag — phones that already have `v1` keep it, and jsDelivr caches tags.

Everything here is public domain (CC0). See LICENSES.md.

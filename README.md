# Golden Hilal — background sound media

The filmed loops and field recordings behind the background sounds in the
Golden Hilal app (Listen → Sounds). The app downloads each file the first time
its sound is used, through jsDelivr, pinned to the commit that holds them:

    https://cdn.jsdelivr.net/gh/Winds7799/golden-hilal-media@6bc1e5ff164cee96d72e2dde5a35445436769290/video/rain.mp4

`video/` — 1080×1920 H.264 (cropped from 4K or vertical footage), no audio,
6–30 s, up to about 8 MB, looped between two frames that match and cross-faded
so the last frame flows into the first. `audio/` — about two minutes each, AAC
128 kbps, loudness-matched (−20 LUFS); the app cross-fades each loop into
itself.

To change a file: commit the new one, then in the app's
`services/ambienceMedia.ts` point `MEDIA_COMMIT` at that commit and bump
`MEDIA_VERSION`. Files at a pinned commit never change, so phones that already
have them keep them. (jsDelivr reads `@v1` as a version range, not a branch —
always pin a full commit.) The `v1` branch marks the files the app first shipped.

Footage is from Pexels (free to use and modify), recordings from Freesound
(CC0). See LICENSES.md.

## `ocr/` — So'm Lens text reader (website)

The two networks goldenhilal.com/price-camera reads price tags with, in the browser
(ONNX Runtime Web), fetched through jsDelivr pinned to the commit that holds them, like
the app's models:

    https://cdn.jsdelivr.net/gh/Winds7799/golden-hilal-media@<commit>/ocr/det.onnx

`det.onnx` finds text (PaddleOCR PP-OCRv4 mobile detection, 4.7 MB), `rec-en.onnx` reads it
(PP-OCRv5 English recognition, 7.8 MB), `rec-en.txt` is its character list. The page checks
each file's size and SHA-256 and falls back to its own copy on goldenhilal.com.

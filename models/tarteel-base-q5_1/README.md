# Quran speech model (Recite mode)

`part0` … `part3` joined in order are `ggml-tarteel-base-q5_1.bin` (59,707,625 bytes,
SHA-256 `acc1f03c8b1468b674b4fab50e0b2312cff982ba0001cd16fe36ca23862b6536`). It is split
because jsDelivr serves files up to 20 MB. Golden Hilal downloads the parts once, joins
them on the phone and runs the model there with whisper.cpp; no audio leaves the phone.

| Part | Bytes | SHA-256 |
| --- | --- | --- |
| part0 | 15,000,000 | 89050578b9cfe5166e4f19b3a07d758c6c756d3c0cbd6868a64dd0cf904e8cbb |
| part1 | 15,000,000 | b259c3216f849660c821f328fd0079b23db8517a2a708b4ac4d52047a0620955 |
| part2 | 15,000,000 | f465f6366c5c42be25b3949257dd7a929b97d9dc1e9e2ca7ca4da1811bcd5a4e |
| part3 | 14,707,625 | abc68333c0f202e1f5eeab2a8a8d75384820dd241aa5040c45fdf8203660d4bf |

## Source and license

A converted copy of **Tarteel AI's `whisper-base-ar-quran`**
(https://huggingface.co/tarteel-ai/whisper-base-ar-quran), a fine-tune of OpenAI's
Whisper base model, licensed under the **Apache License 2.0** (full text: `LICENSE`).

Changes made: converted from the Hugging Face PyTorch weights to whisper.cpp's GGML format
(`models/convert-h5-to-ggml.py`, with the text context taken from `max_target_positions`
instead of `max_length`) and quantized to q5_1. The weights were not retrained.

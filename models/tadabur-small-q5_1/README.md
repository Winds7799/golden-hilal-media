# Quran speech model, Tadabur small (Recite mode)

`part0` … `part12` joined in order are `ggml-tadabur-small-q5_1.bin` (190,085,504 bytes,
SHA-256 `163dda0e934b9e85d96d6939f7d6fb059345e881e5ec30222efc8406c4189a7f`). It is split
because jsDelivr serves files up to 20 MB. Golden Hilal downloads the parts once, joins
them on the phone and runs the model there with whisper.cpp; no audio leaves the phone.

| Part | Bytes | SHA-256 |
| --- | --- | --- |
| part0 | 15,000,000 | 0f6548a25fe8d003a37a6bf7afece4a41e7c8c361892b4248506c2e36261d814 |
| part1 | 15,000,000 | 32c7f87c78d05af3208d2a5bc4a3971f9285fc8df465e530707f0e4075870e16 |
| part2 | 15,000,000 | f3bbc0cd1ae8676da566bbd632ba835e06e326d14f293eac7126e32eb839d5ae |
| part3 | 15,000,000 | c41affef5d1b8f8cc61aba9dd8dd7cb75256bdba1b75d0fea2cf68ef0cbb636c |
| part4 | 15,000,000 | f55f17b9cc2c04d9dba391e7205b36f41eef349e0f10a28b1ea2a00a68d0ee45 |
| part5 | 15,000,000 | a85d82dae6531e6708cd4e5e3b870b82dd6d696f21389fd32ffdc4144e28c113 |
| part6 | 15,000,000 | 876b00e706b1fa9473bcb183e0508744a5613f0af5aa7d42447a970a3fb1ab74 |
| part7 | 15,000,000 | a0e6597c5903c24ac69b3c21e706cce1ca8df99a706e1d968dce7d9f3e893579 |
| part8 | 15,000,000 | f455af6787c2c448a2f11f46114afb6e4934bcdc211afd05e006ac2f3032bc34 |
| part9 | 15,000,000 | 586c6259f919c5f0c6a0da760934fba210bf5fac2991ada1b2ae881678416805 |
| part10 | 15,000,000 | e4a3d9c2747b97eb44fe5cc3d690c6417c7457e697d2a51fb459fa8a6a417508 |
| part11 | 15,000,000 | 1073343eae2602a82d242543f07bdac11fb99489bda8fca7edc6d7824f285505 |
| part12 | 10,085,504 | ef22c8999ef9d879dde97e321b017b9295adf27c2a3f0421f2b4e5f1cdad897f |

## Source and license

A converted copy (whisper.cpp GGML, 5-bit q5_1) of **`FaisaI/tadabur-whisper-small`**
(https://huggingface.co/FaisaI/tadabur-whisper-small, revision
`956e899e9f7bd9ab4b75ec254f00310da7362b56`), a fine-tune of OpenAI's Whisper small model on
the Tadabur Qur'an recitation dataset ("Tadabur: A Large-Scale Quran Audio Dataset",
https://huggingface.co/papers/2604.18932). It was converted and compressed, not retrained.

The model is published under **CC BY-NC 4.0**. Golden Hilal redistributes it here, and uses
it in the app, under a separate license granted by its rights holder. That license does not
extend to anyone else: for any other use, the model's own terms (CC BY-NC 4.0) apply.

It replaced `../quran-small-q5_1` because it hears everyday voices better (words of the
verse right or nearly right in amateur recitations 69.6% against 63.8%, same size and speed).

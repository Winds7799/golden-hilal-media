# Quran speech model, small (Recite mode)

`part0` … `part12` joined in order are `ggml-quran-small-q5_1.bin` (190,085,504 bytes,
SHA-256 `f160e98d3b02696f949f1c20c6a23a1621b4c32354c5b2f07293779216e133d5`). It is split
because jsDelivr serves files up to 20 MB. Golden Hilal downloads the parts once, joins
them on the phone and runs the model there with whisper.cpp; no audio leaves the phone.

| Part | Bytes | SHA-256 |
| --- | --- | --- |
| part0 | 15,000,000 | 2f19539d336f8504eb0e8234db2aafd17870c7004331af7834b7fe1e74820886 |
| part1 | 15,000,000 | e5cecb04d10dca5046767cbb369fff2f715803e5ceebd0f8f3a11781bead0f8e |
| part2 | 15,000,000 | af29cfbe41a9202977b7d87238ce86469f4ba14397122d5d619b99c25602f9df |
| part3 | 15,000,000 | 128ca6bb1c5336e3d8aeb15f6ad619648b9191d9967c46ed08326289a65cd1fa |
| part4 | 15,000,000 | 294fdb5f5c68caf455bfd3aef56857c5ef515431752db4dde5c80f44ea1962b7 |
| part5 | 15,000,000 | 8c6df4102bf80a9403e3be044250d8688a44697cdaf3fbcc7f0038de193b7aec |
| part6 | 15,000,000 | abd07afa7b5fff5c4803968c93758971b346293f8567916c30ba17eab9dd1127 |
| part7 | 15,000,000 | bcc35f4f1704dc7023748f093f27f54920597e717341ad09acf270cc24a150f8 |
| part8 | 15,000,000 | 548cdf5b3a1dde0cbc49512559c2c3de3cdf43601fa64a592d39f7d1b1959397 |
| part9 | 15,000,000 | dcd4fd4258f21c15c3650e07ee1fbe9467fcbc9cd017009f12efe4bd40a4c6dc |
| part10 | 15,000,000 | eac7061aa793b88705fb28ed71f840665bbb80aca42ef4259db878746db57720 |
| part11 | 15,000,000 | 9e1686f267962ff6a7c205f2e4776fba9cffb469894a8b3d4cd80d53b9889ecf |
| part12 | 10,085,504 | 54f04020399dccdb860c9bf522a3a51e6ba7ff76d9ee27bcbd358827b60b8190 |

## Source and license

A converted copy (whisper.cpp GGML, 5-bit q5_1) of **`basharalrfooh/whisper-small-quran`**
(https://huggingface.co/basharalrfooh/whisper-small-quran, revision
`a3b54a9432bcf67549cb42c9eb1fe1870db92627`), a fine-tune of OpenAI's Whisper small model on
Qur'anic recitation (EveryAyah, 64 reciters). Both are under the **MIT License** (`LICENSE`).
It replaced `../tarteel-base-q5_1` because it hears everyday voices better (words right or
nearly right in amateur recitations: 64% against 52%).

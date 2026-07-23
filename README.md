# Khmer Text-to-Speech — ការបម្លែងអត្ថបទជាសំឡេងខ្មែរ 🗣️

**▶ Try it now (free): https://huggingface.co/spaces/sarunvisoth/khmer-tts-demo**

Type Khmer, hear natural Khmer speech — two voices, numbers and dates read
correctly, full paragraphs supported.

---

វាយអត្ថបទខ្មែរ ហើយស្តាប់សំឡេងអានភ្លាមៗ — ឥតគិតថ្លៃ។ អាចអានលេខ (២៥ → ម្ភៃប្រាំ)
កាលបរិច្ឆេទ និងកថាខណ្ឌវែងៗបានត្រឹមត្រូវ ដោយមានសំឡេងប្រុស និងស្រី។

**សាកល្បងនៅទីនេះ៖ https://huggingface.co/spaces/sarunvisoth/khmer-tts-demo**

---

## How good is it? Measured, not claimed

ASR round-trip evaluation: synthesize 30 held-out Khmer sentences, transcribe
them with a Khmer speech-recognition model, count character errors (CER — lower
is better). Real human recordings of the same sentences set the ASR's error
floor.

| system | mean CER ↓ |
|---|---|
| **this model (zero-shot voice)** | **0.176** |
| Google Translate's Khmer voice | 0.208 |
| *human recordings (ASR floor)* | *0.220* |
| Meta MMS (`facebook/mms-tts-khm`) | 0.337 |
| Community MMS fine-tune | 0.651 |

The model reads unseen text more intelligibly to the ASR than the original
human recordings — while simultaneously cloning a voice it never trained on.

## What's under the hood

- **F5-TTS** (flow-matching DiT) fine-tuned on **~1,000 hours** of Khmer speech
- A purpose-built **Khmer text front-end**: number verbalization
  (២៥ → ម្ភៃប្រាំ, ៛ → រៀល), sentence-integrity chunking with phrase-aware
  pauses (dates are never split), Khmer Unicode normalization and cross-script
  confusable repair (Thai lookalike marks → intended Khmer signs)
- Zero-shot voice cloning: a voice is just a short reference clip

## Status & roadmap

Active research project. Current model handles everyday Khmer well; formal/news
register and English code-switching are the next frontier (phoneme front-end +
domain data). Follow the Space for updates.

## Credits & license

- Speech data: [Digital Divide Data](https://huggingface.co/DDD-Cambodia)
  (CC-BY-SA-4.0) — the dataset that makes Khmer speech AI possible
- Base model: [F5-TTS](https://github.com/SWivid/F5-TTS) (checkpoint
  CC-BY-NC-4.0 → this is a **non-commercial research demo**)
- Also trained on [OpenSLR 42](https://openslr.org/42) and
  [FLEURS](https://huggingface.co/datasets/google/fleurs)
- Built by [@sarunvisoth](https://github.com/sarunvisoth)

*Model weights are not distributed.*

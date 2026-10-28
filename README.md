# Khmer Text-to-Speech 🗣️

**[▶ Try it now — free demo on HuggingFace](https://huggingface.co/spaces/sarunvisoth/khmer-tts-demo)**

Type Khmer, hear natural Khmer speech — two voices, numbers and dates read
correctly, full paragraphs supported.

> This repository is the project's landing page and documentation. The model and the app run on
> HuggingFace: [sarunvisoth/khmer-tts-demo](https://huggingface.co/spaces/sarunvisoth/khmer-tts-demo)
> (free, runs on ZeroGPU, no sign-up needed).

## How to use it

1. Open the [demo Space](https://huggingface.co/spaces/sarunvisoth/khmer-tts-demo).
2. Paste or type Khmer text.
3. Choose a voice and generate. A short reference clip also works as a voice (zero-shot cloning).

## What's under the hood

Text goes through a Khmer text pipeline (numbers, dates and punctuation are normalised into spoken
form), then the F5-TTS model generates the audio, conditioned on a reference voice clip.

- **F5-TTS** (flow-matching DiT) fine-tuned on **~1,000 hours** of Khmer speech
- A Khmer-specific text pipeline built and tested with native-speaker feedback
- Zero-shot voice cloning: a voice is just a short reference clip

## Status & roadmap

Active research project. The current model handles everyday Khmer well;
formal/news register and English code-switching are the next frontier.
Follow the Space for updates.

## Credits & license

- Speech data: [Digital Divide Data](https://huggingface.co/DDD-Cambodia)
  (CC-BY-SA-4.0) — the dataset that makes Khmer speech AI possible
- Base model: [F5-TTS](https://github.com/SWivid/F5-TTS) (checkpoint
  CC-BY-NC-4.0 → this is a **non-commercial research demo**)
- Also trained on [OpenSLR 42](https://openslr.org/42) and
  [FLEURS](https://huggingface.co/datasets/google/fleurs)
- Built by [@sarunvisoth](https://github.com/sarunvisoth)

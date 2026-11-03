# Bekitzur

Bekitzur records your meetings on your Mac and writes the notes: a transcript in Hebrew or English, who said what, and a summary with decisions, action items, and open questions. Everything runs on your Mac; nothing is sent anywhere.

## What you need

- A Mac with Apple silicon (M1 or later) and at least 32 GB of memory
- macOS 26 or later
- About 20 GB of free disk space, for the models

## Install

1. Download [Bekitzur.zip](https://github.com/GabrielYamin/Bekitzur-releases/releases/latest/download/Bekitzur.zip) and open it, which unpacks a Bekitzur folder.
2. Open Terminal and run:

   ```bash
   bash ~/Downloads/Bekitzur/install.sh
   ```

   It installs the app in the Applications folder of your home folder and opens it.
3. Bekitzur lives in the menu bar. Choose **Download** in its window to get its speech, language, and speaker models (about 18 GB) from Hugging Face. That takes about 10 minutes on a fast connection; if it's interrupted, Download picks up where it left off. The first recording asks for the microphone and for system audio (the other side of calls).

## Update

Bekitzur checks for new versions and asks before installing one. You can also choose **Check for Updates…** in its menu. Your Conversations, names, and settings stay.

Versions before 0.2.0 can't update themselves, so update those once by hand: download the latest Bekitzur.zip and run install.sh again, as above. It replaces the app and keeps your data and models, and it won't replace the app while it's recording.

## Privacy

Recording, transcription, speaker recognition, and notes all run on your Mac. Your audio, transcripts, and notes stay in `~/Library/Application Support/Bekitzur`. Bekitzur goes online only to download its models and to check this page for new versions.

## Disclaimer

Bekitzur is provided as is, without warranty of any kind, and its authors aren't liable for anything that comes of using it, like a recording that's lost or incomplete, a mistake in a transcript, the speakers, or the notes, or a decision made from them. Everything runs on your Mac: your recordings, transcripts, notes, and voices stay on it, and Bekitzur goes online only to download its models and updates. You're responsible for telling the people you record, and for following the law and your organization's rules on recording. The [MIT License](LICENSE) has the full terms.

## Remove

Quit Bekitzur, then delete `~/Applications/Bekitzur.app` and `~/Library/Application Support/Bekitzur` (your Conversations and the models).

## License and credits

Bekitzur is free to use under the [MIT License](LICENSE). It's built on [whisper.cpp](https://github.com/ggml-org/whisper.cpp) and [llama.cpp](https://github.com/ggml-org/llama.cpp) (MIT) and [FluidAudio](https://github.com/FluidInference/FluidAudio) (Apache 2.0), whose licenses come with the app, in `Bekitzur.app/Contents/Resources/Acknowledgements.txt`.

Bekitzur downloads each model from its publisher on Hugging Face, under that publisher's license: [ivrit.ai's Whisper large-v3-turbo](https://huggingface.co/ivrit-ai/whisper-large-v3-turbo-ggml) for Hebrew (Apache 2.0), [OpenAI's Whisper large-v3-turbo](https://huggingface.co/openai/whisper-large-v3-turbo) for English (MIT), and [Google's Gemma 4 26B-A4B](https://huggingface.co/google/gemma-4-26B-A4B-it-qat-q4_0-gguf) for the notes (Apache 2.0). The speaker models are [pyannote's community-1](https://huggingface.co/pyannote/speaker-diarization-community-1) (CC BY 4.0), [NVIDIA's Nemotron 3 Diarization](https://huggingface.co/nvidia/Nemotron-3-Diarization) (OpenMDW 1.1), and [Silero VAD](https://github.com/snakers4/silero-vad) (MIT), all converted to Core ML by Fluid Inference.

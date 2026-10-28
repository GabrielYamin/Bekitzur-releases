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

   It installs the app in the Applications folder of your home folder and downloads the speech and language models (about 18 GB) from Hugging Face. That takes about 10 minutes on a fast connection; if it's interrupted, run it again and it picks up where it left off.
3. Bekitzur opens, and lives in the menu bar. The first recording asks for the microphone and for system audio (the other side of calls), and the first Conversation downloads the speaker models once.

## Update

Bekitzur checks for new versions and asks before installing one. You can also choose **Check for Updates…** in its menu. Your Conversations, names, and settings stay.

Versions before 0.2.0 can't update themselves, so update those once by hand: download the latest Bekitzur.zip and run install.sh again, as above. It replaces the app and keeps your data and models, and it won't replace the app while it's recording.

## Privacy

Recording, transcription, speaker recognition, and notes all run on your Mac. Your audio, transcripts, and notes stay in `~/Library/Application Support/Bekitzur`. Bekitzur goes online only to download its models and to check this page for new versions.

## Remove

Quit Bekitzur, then delete `~/Applications/Bekitzur.app` and `~/Library/Application Support/Bekitzur` (your Conversations and the models).

## Models

The installer downloads each model from its publisher on Hugging Face, under that publisher's license: ivrit.ai's Whisper large-v3-turbo for Hebrew, OpenAI's Whisper large-v3-turbo for English, and Google's Gemma 4 26B-A4B for the notes. FluidAudio's speaker models download on first use.

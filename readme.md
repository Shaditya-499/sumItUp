# Meeting Summary Pipeline

This project processes a video file from Google Drive, extracts audio, transcribes it using Whisper, generates a summary with BART, extracts tasks with OPT, and sends the results via email using the Gmail API. It’s designed to run on Windows with Python 3.7.

## Features
- Downloads a video from Google Drive.
- Extracts audio using MoviePy.
- Transcribes audio with OpenAI Whisper.
- Summarizes the transcript using BART (`facebook/bart-large-cnn`).
- Extracts tasks using OPT (`facebook/opt-350m`).
- Sends the summary, transcript, and tasks to specified recipients via Gmail.

## Prerequisites
- **Python 3.7**: Installed at `C:\python37\python.exe`.
- **FFmpeg**: Required for audio extraction and transcription.
- **Google Cloud Project**: OAuth 2.0 credentials for Gmail API (`long-justice-452914-c1-4de2f1e04728.json`).

## Setup

### 1. Clone or Copy the Script
- git clone https://github.com/Shaditya-499/sumItUp.

### 2. Install FFmpeg
1. Download FFmpeg from [ffmpeg.org](https://ffmpeg.org/download.html) or [gyan.dev](https://www.gyan.dev/ffmpeg/builds/).
2. Extract to `C:\ffmpeg`.
3. Add to PATH:
   - Right-click “This PC” > Properties > Advanced system settings > Environment Variables.
   - Edit “Path” under System variables, add `C:\ffmpeg\bin`.
4. Verify:
   ```bash
   ffmpeg -version

# LoniEcho

This project utilizes OpenAI's Whisper model for speech recognition. For more information, visit the Whisper GitHub repository: [https://github.com/openai/whisper](https://github.com/openai/whisper)

## Setup Requirements

Before working with this project, ensure you have the following installed:

### FFmpeg
Whisper requires FFmpeg for audio processing. Install it based on your operating system:

- **Windows (using Chocolatey):**
  ```bash
  choco install ffmpeg
  ```
- **Windows (using Scoop):**
  ```bash
  scoop install ffmpeg
  ```
- **Ubuntu/Debian:**
  ```bash
  sudo apt update && sudo apt install ffmpeg
  ```
- **Arch Linux:**
  ```bash
  sudo pacman -S ffmpeg
  ```
- **macOS (using Homebrew):**
  ```bash
  brew install ffmpeg
  ```

Ensure that FFmpeg is correctly installed and accessible from your system's PATH.

## Current Setup Status

✅ **Project Structure**: Git repository initialized with proper .gitignore
✅ **Python Environment**: Python 3.13.7 available, virtual environment created
✅ **OpenAI Whisper**: Successfully installed with all dependencies

⚠️ **FFmpeg**: Requires manual installation (see instructions below)

## Manual FFmpeg Installation

Since automated installation requires administrator privileges, please install FFmpeg manually:

### Option 1: Download from Official Website
1. Visit https://ffmpeg.org/download.html
2. Download the Windows build (static version recommended)
3. Extract the ZIP file to a folder (e.g., `C:\ffmpeg`)
4. Add the `bin` folder to your system PATH:
   - Press `Win + X` and select "System"
   - Click "Advanced system settings"
   - Click "Environment Variables"
   - Under "System variables", find "Path" and click "Edit"
   - Click "New" and add the path to the `bin` folder (e.g., `C:\ffmpeg\bin`)
   - Restart your command prompt

### Option 2: Using Windows Package Managers (requires admin)
```powershell
# Using Chocolatey (run as Administrator)
choco install ffmpeg

# Using Scoop
scoop install ffmpeg
```

### Verify Installation
After installation, verify FFmpeg works:
```bash
ffmpeg -version
```

## Development Setup

To start developing:

1. Ensure FFmpeg is installed and accessible
2. Activate the virtual environment:
   ```bash
   whisper-env\Scripts\activate.bat
   ```
3. Use Whisper for speech recognition:
   ```bash
   whisper audio_file.mp3
   ```

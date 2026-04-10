# Project: Jarvis

## Project Overview

This project, named "Jarvis," is a voice-controlled AI assistant developed in Python. It integrates several powerful libraries to provide a conversational interface:

-   **Speech-to-Text:** Utilizes `openai-whisper` to transcribe spoken audio into text.
-   **Large Language Model (LLM) Integration:** Employs `ollama` to interact with a local `tinyllama:latest` model for natural language processing, understanding user queries, and generating responses.
-   **Audio Recording:** Uses `sounddevice`, `numpy`, and `scipy` to capture audio input from the user.

The core workflow involves:
1.  Recording user's speech.
2.  Transcribing the speech into text.
3.  Sending the transcribed text to the `tinyllama` LLM.
4.  Printing the LLM's generated response.

## Building and Running

This project uses Python for its development and relies on `pyproject.toml` and `uv.lock` for dependency management, suggesting the use of `uv` or `pip`.

### Dependencies Installation

To install the required dependencies, navigate to the project root directory and run:

```bash
uv pip install -e .
# or if you prefer using pip
# pip install -e .
```

### Running the Project

The main entry point for the application is `main.py`. To run the Jarvis assistant, execute the following command from the project root:

```bash
python main.py
```

Upon execution, Jarvis will start listening for audio input, process it, and respond.

## Development Conventions

-   **Language:** Python
-   **Dependency Management:** `pyproject.toml` and `uv.lock` for `uv` (or `pip`).
-   **Code Structure:** `main.py` contains the primary application logic, `record.py` handles audio recording, and `temp_audio.wav` is used for temporary audio storage during processing.

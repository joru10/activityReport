# ActivityReport

## Product Description

ActivityReport is a personal voice-to-text activity logging system that leverages AI to seamlessly capture, transcribe, and analyze your daily activities. Designed for local deployment on your machine, ActivityReport uses the built-in Web Audio API to record your voice, transcribes the recordings with the small model of OpenAI Whisper, and then processes the transcripts through a configurable LLM integration. This processing extracts structured activity data—such as activity group, timestamp, duration, and description—according to YAML-defined prompt profiles.

The system also aggregates your daily activities into insightful periodic reports (daily, weekly, and monthly). These reports provide aggregated analytics such as the total time spent per activity group and a detailed list of activities performed throughout the day. With a React-based frontend for a straightforward user experience and comprehensive backend logging for easy debugging, ActivityReport is built for clarity, modularity, and future expandability. It supports multiple LLM providers and configurable prompt profiles, making it a flexible tool for diverse voice-to-text processing needs.

## Key Features:

- **Audio Capture**: Uses the browser's native Web Audio API with default device selection.
- **Transcription**: Employs OpenAI Whisper (small model) for converting voice recordings into text.
- **LLM Integration**: Supports various LLM providers (both proxy-based and direct) and enforces output structure using Pydantic.
- **Activity Logging**: Extracts and stores structured activity records based on configurable YAML profiles.
- **Periodic Reporting**: Automatically generates daily, weekly, and monthly reports with aggregated data and optional graphical summaries.
- **In-App Notifications**: Reminds you to record at predefined intervals (1, 15, 30, 60, or 120 minutes).
- **Local Data Storage**: Organizes raw audio files, transcripts, and reports in a simple file system hierarchy by date.
- **REST API & React Frontend**: Provides a clean API for recording, settings, logs, and reports, with a user-friendly React-based interface.

## Project Structure

```
activityReport/
├── backend/        # FastAPI application and Python code
├── frontend/       # React app
├── storage/        # Audio files and transcripts (date-based subfolders)
├── reports/        # Generated reports
├── profiles/       # YAML prompt profiles
├── docs/           # Documentation and guides
└── README.md       # Project description and structure
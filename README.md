# Personal AI Email Agent — backend

Read-only Gmail ingestion API built with FastAPI. It stores Gmail OAuth tokens encrypted at rest, classifies incoming messages locally with transparent rules, and exposes summaries without automatically sending, deleting, or modifying email.

## Quick start

1. Create a Google OAuth **Web application** client in Google Cloud, enable the Gmail API, and add `http://localhost:8000/oauth/google/callback` as an authorized redirect URI. Download the client JSON as `credentials.json` (kept out of Git by `.gitignore`). The app requests only `gmail.readonly`.
2. Install Python 3.11+ and configure the app:

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
   pip install -r requirements.txt
   cp .env.example .env

# Travel Guide AI

Travel Guide AI creates written and audio guides for destinations. Choose a summary or detailed guide, select a language and voice, and listen to the generated narration.

## Features

- Destination cards and destination search
- Summary and detailed guide formats
- English, Hindi, Tamil, and Telugu output
- Gemini-generated descriptions and Murf-generated audio

## Requirements

- Python 3
- A Gemini API key
- A Murf API key
- Internet access for the external APIs and frontend assets

## Setup

Install the backend dependencies from the project root:

```powershell
python -m pip install Flask flask-cors google-genai requests
```

Set the API keys in the PowerShell session that will run the backend. Replace the placeholders with your own keys; do not commit real keys to the repository.

```powershell
$env:GEMINI_API_KEY = "your-gemini-api-key"
$env:MURF_API_KEY = "your-murf-api-key"
```

Start the backend from the project root:

```powershell
python .\Backend\app.py
```

The API listens at `http://127.0.0.1:5000`.

In a second terminal, serve the frontend:

```powershell
Set-Location .\Frontend
python -m http.server 8000
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser. Keep both servers running while using the app.

## Project Structure

```text
Backend/app.py       Flask API and AI service integrations
Frontend/index.html  User interface
Frontend/index.js    Frontend interactions and API requests
```

The Flask development server is intended for local development, not production deployment.
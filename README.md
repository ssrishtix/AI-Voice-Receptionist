# AI Voice Receptionist

AI-powered voice receptionist for home service businesses that answers calls 24/7, captures leads conversationally, and automates customer intake.

## Features

- AI-powered call handling
- Real-time speech recognition
- Natural voice responses
- Lead capture & slot extraction
- Owner SMS notifications
- Multi-tenant SaaS architecture
- Calendar & CRM integrations

## Tech Stack

- FastAPI
- Python
- OpenAI GPT-4o
- Deepgram
- Cartesia
- Twilio
- Supabase
- PostgreSQL
- Next.js

## Architecture

(Add architecture diagram image)

## Project Structure

```bash
maya/
├── routes/
├── services/
├── db/
├── config/
├── prompts/
└── main.py

````md
## Quick Start

### Clone the Repository

```bash
git clone https://github.com/yourusername/maya.git
cd maya
````

### Create a Virtual Environment

```bash
python -m venv venv
```

### Activate the Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### macOS / Linux

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Environment Variables

Create a `.env` file in the project root:

```env
TWILIO_ACCOUNT_SID=
TWILIO_AUTH_TOKEN=
TWILIO_PHONE_NUMBER=

DEEPGRAM_API_KEY=

CARTESIA_API_KEY=
CARTESIA_VOICE_ID=

OPENAI_API_KEY=

SUPABASE_URL=
SUPABASE_SERVICE_KEY=

OWNER_PHONE=
```

### Run the Backend Server

```bash
uvicorn main:app --reload --port 3000
```

### Expose Local Server with ngrok

```bash
ngrok http 3000
```

Configure the generated HTTPS URL as your Twilio Voice Webhook:

```text
https://your-ngrok-url/twilio/voice
```

---

# Project Structure

```text
maya/
│
├── routes/
│   ├── twilio.py
│   └── internal.py
│
├── services/
│   ├── stt.py
│   ├── tts.py
│   ├── llm.py
│   ├── notify.py
│   ├── classifier.py
│   ├── calendar.py
│   └── crm/
│       └── jobber.py
│
├── db/
│   └── calls.py
│
├── config/
│   └── verticals.py
│
├── prompts/
│
├── models.py
├── session.py
├── main.py
├── requirements.txt
└── .env
```

---

# Testing

Run the following tests before deployment:

```bash
python test_db.py
python test_llm.py
python test_tts.py
```

---

# Current Status

🚧 Under Development

Current Focus:
- Twilio call handling
- Deepgram speech recognition
- GPT-4o slot extraction
- Cartesia voice responses

Upcoming:
- Google Calendar integration
- CRM integration
- Business dashboard

# License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

# Phone Agent

A voice-first AI agent that can make phone calls, send WhatsApp messages, and manage your daily tasks using natural language.

## Features

- **Voice-First Interface**: Talk to the agent naturally and get spoken responses.
- **Phone Calls**: Make and receive phone calls with AI-powered voice.
- **WhatsApp Integration**: Send and receive WhatsApp messages.
- **Task Management**: Create, update, and query tasks with natural language.
- **Calendar Integration**: Manage your schedule and appointments.
- **Smart Routing**: Intelligent routing of requests to the appropriate tool.
- **Contextual Awareness**: Maintains conversation context for natural interactions.

## Getting Started

### Prerequisites

- Python 3.11+
- [uv](https://github.com/astral-sh/uv) - Fast Python package installer and resolver

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd phone-agent
   ```

2. **Create a virtual environment**
   ```bash
   uv venv .venv
   ```

3. **Activate the virtual environment**
   ```bash
   source .venv/bin/activate
   ```

4. **Install dependencies**
   ```bash
   uv pip install -e .
   ```

## Usage

### Run the Agent

Start the voice-first agent with a single command:

```bash
python -m phone_agent
```

The agent will start in interactive mode, waiting for your voice commands.

### Example Interactions

**Make a phone call:**
```
"Call Mom at home"
```

**Send a WhatsApp message:**
```
"Send a WhatsApp message to John saying I'll be 10 minutes late"
```

**Manage tasks:**
```
"Add a task to buy milk"
"What are my tasks for today?"
"Mark 'buy milk' as completed"
```

**Manage calendar:**
```
"Schedule a meeting with Sarah tomorrow at 2 PM"
"What's on my calendar for Friday?"
```

## Configuration

Create a `.env` file in the project root with the following variables:

```env
# OpenAI API Key
OPENAI_API_KEY=your_openai_api_key

# Twilio Credentials (for phone calls)
TWILIO_ACCOUNT_SID=your_twilio_account_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_PHONE_NUMBER=your_twilio_phone_number

# WhatsApp Credentials (optional)
TWILIO_WHATSAPP_SID=your_whatsapp_sid

# Google Calendar Credentials (optional)
GOOGLE_CALENDAR_CREDENTIALS=path/to/credentials.json
```

## Development

### Testing

Run the test suite:

```bash
pytest
```

### Adding New Tools

To add a new tool to the agent:

1. Create a new Python file in `phone_agent/tools/`
2. Define a class that inherits from `BaseTool`
3. Implement the `run` method
4. Register the tool in `phone_agent/agent.py`

## License

This project is licensed under the terms of the MIT license.

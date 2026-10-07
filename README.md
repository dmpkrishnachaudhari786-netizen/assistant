# Assistant

A dark, voice-enabled assistant web app (PWA): four AI providers, photo attach, image mode,
login, chat history, Google Drive export, and an editable **persona**.

## Features
- **Persona:** the AI talks in a set personality (default: savage-roast / dark-humour / chill /
  philosopher). Edit it in Settings -> Persona. It is sent as the system prompt to the model.
- **Providers:** Gemini (Google), Sarvam AI, DeepSeek, Kimi (Moonshot)
- **Photo attach** and **Image mode** (image generation)
- **Voice** (speaks replies), **Settings**
- **Login / logout** - a LOCAL profile stored on this device only (not real authentication)
- **Chat history** - new, open, delete, export
- **Export** chats to a JSON file, or upload to **Google Drive** (needs your OAuth Client ID)
- Installable PWA; app shell works offline

## Honest limitations
- **Login is a local profile, not real authentication** (real login needs an auth provider).
- **Google Drive upload needs YOUR Google OAuth Client ID.**
- **Screen control is not possible in a web app** (needs a native Android app).
- **Canva cannot be embedded in a web app** - Canva is an agent connector, not an in-app widget.
- **Video editing is not possible in this browser app** (needs a native/desktop toolchain).
- API keys are stored on your device and used from the browser; some providers may block browser
  calls (CORS). For public use, route through a small server.

## Tested
Real-browser checks: persona prefilled, custom persona saved + shown on reopen, persona sent as
system_instruction to the API, plus earlier login/logout, history, providers, attach, image mode.

# Assistant

A dark, voice-enabled assistant web app (PWA): four AI providers, photo attach, image mode,
login, chat history and Google Drive export.

## Features
- **Providers:** Gemini (Google), Sarvam AI, DeepSeek, Kimi (Moonshot)
- **Photo attach** and **Image mode** (image generation)
- **Voice** (speaks replies), **Settings**
- **Login / logout** - a LOCAL profile stored on this device only (see below)
- **Chat history** - saved conversations: new, open, delete, export
- **Export** chats to a JSON file, or upload to **Google Drive** (needs your OAuth Client ID)
- Installable PWA; app shell works offline

## Honest limitations
- **Login is a local profile, not real authentication.** Real login needs an auth provider
  (e.g. Supabase). The app says this on the Account screen.
- **Google Drive upload needs YOUR Google OAuth Client ID** (Google Cloud -> OAuth Client ID,
  enable Drive API, add this site as an allowed origin). Without it, use "Download chats file".
- **Screen control is not possible in a web app** (needs a native Android app).
- API keys are stored on your device and used from the browser; some providers may block browser
  calls (CORS). For public use, route through a small server.

## Tested
Real-browser checks (16/16): loads, account view, honest local-profile warning, login, logout,
honest "add key" reply, chat saved to history with a title, new chat, open a chat, four providers,
per-provider key save, export, service worker, no console errors.

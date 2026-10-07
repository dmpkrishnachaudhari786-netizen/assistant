# Assistant

A dark, voice-enabled assistant web app (PWA) with an optional **Gemini** API key.

## Features
- Dark theme + a new spark logo
- Chat UI; replies spoken aloud when the voice toggle is on (Web Speech API)
- Settings: Gemini API key, model, voice on/off (saved on your device only)
- Installable PWA; app shell works offline

## Add AI
Open Settings and paste your Gemini API key (get one at aistudio.google.com/apikey).
Without a key the app says so honestly and does not fake a reply.

## Honest limitations
- **Screen control is not possible in a web app.** Controlling your phone's screen needs a
  native Android app with an AccessibilityService - a browser/PWA cannot do it.
- The API key is stored on your device and used directly from the browser; for anything public
  or shared, put the call behind a small server so the key stays private.

## Tested
Real-browser checks: loads with logo, honest "add key" message (no fake reply), settings save,
voice toggle, settings persist across refresh, speech capability, service worker, no console errors.

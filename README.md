# Assistant

A dark, voice-enabled assistant web app (PWA) with **four AI providers**, photo attach and image generation.

## Features
- Dark theme + spark logo
- **Providers:** Gemini (Google), Sarvam AI, DeepSeek, Kimi (Moonshot) - pick one, paste its API key
- **Photo attach:** attach an image and ask about it
- **Image mode:** turn it on and your message is generated as an image (needs a model that supports IMAGE responses)
- **Voice:** replies spoken aloud when the toggle is on (Web Speech API)
- Settings saved on your device only; installable PWA; app shell works offline

## Honest limitations
- **Screen control is not possible in a web app.** Controlling your phone's screen needs a native
  Android app with an AccessibilityService - a browser/PWA cannot do it.
- The API key is stored on your device and used directly from the browser. Some providers may block
  browser calls (CORS), and for anything public you should route through a small server.
- Provider base URLs are prefilled best-effort; if a provider's endpoint differs, edit it in Settings.
- Image generation depends on the chosen model supporting image output.

## Tested
Real-browser checks (12/12): loads with logo + provider pill, four providers listed, switching provider
updates model/base URL, per-provider key saved, honest "add key" message (no fake reply), photo attach
thumbnail, image-mode toggle, service worker, and no console errors.

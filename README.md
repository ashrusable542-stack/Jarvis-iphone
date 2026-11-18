# JARVIS iPhone Standalone v1.0

This is a Progressive Web App (PWA) for iPhone 17. It can be added to the Home Screen and launched in a standalone app-like window.

## What works in this free starter

- Blue holographic JARVIS dashboard.
- English, Hindi and Marathi response-language selection.
- Spoken replies using iOS browser speech synthesis where available.
- iPhone keyboard dictation (tap the microphone on the iOS keyboard).
- Local notes stored in this browser on this iPhone, with export and delete.
- Basic built-in commands: time, date, study plan, daily plan, simple arithmetic, and note saving.
- 5-minute and 25-minute timers while the page remains active.
- Offline dashboard shell after the first successful visit.

## Important AI limitation

This standalone package does not contain a full language model. It provides local/basic assistant functions and an **Ask ChatGPT** handoff. That handoff uses the ChatGPT service and requires internet access and whatever account/usage limits apply. A ChatGPT subscription is not the same as API access. Do not paste API keys into this static app.

## Publish it free with GitHub Pages

PWA installation and service workers require HTTPS (or localhost). A local `file://` copy will not install as a PWA.

1. On a computer or iPhone browser, sign in or create a GitHub account at https://github.com/.
2. Create a new public repository named `jarvis-iphone`.
3. Upload the contents of this folder (index.html, manifest.webmanifest, sw.js, and icons folder) to the repository root.
4. In the repository, open **Settings → Pages**.
5. Under Build and deployment, select **Deploy from a branch**, choose `main` and `/ (root)`, then Save.
6. Wait for GitHub Pages to publish. Your URL will look like `https://YOUR-USERNAME.github.io/jarvis-iphone/`.

GitHub's interface may change. Follow its Pages publishing instructions if labels differ.

## Install on iPhone 17

1. Open the published HTTPS URL in **Safari** (not an in-app browser).
2. Tap the Share button.
3. Scroll and choose **Add to Home Screen**.
4. If shown, enable **Open as Web App**.
5. Tap Add. Launch JARVIS from the new Home Screen icon.

## Use voice

- For reliable iPhone dictation, tap the command box, then tap the microphone on the iOS keyboard.
- Tap TRANSMIT to get a local response.
- Spoken output uses the browser's speech synthesis voices. Available Hindi and Marathi voices depend on iOS version and downloaded system voices.
- Safari's web speech recognition support is inconsistent. The app intentionally falls back to iOS keyboard dictation.
- It cannot listen continuously for “Hey JARVIS” in the background.

## Privacy and data

- Notes are stored in local browser storage on this device. Export notes periodically.
- Do not save passwords, payment information, or sensitive personal data.
- No app server is included; the app is static. Ask ChatGPT opens an external service.
- Deleting Safari website data may delete local notes.
- Timers may pause or be suspended if iOS backgrounds or closes the web app. Use the iPhone Clock app for critical alarms.

## iPhone automation limits

A web app cannot freely open arbitrary apps, read messages, create reminders, toggle system settings, or execute actions in the background. For those tasks, create Apple Shortcuts and invoke them with Siri or use supported iOS share/open flows. This app's “Open Shortcuts” button opens the Shortcuts app URL scheme where supported; it does not execute arbitrary shortcuts.

## Files

- `index.html` — app interface and logic
- `manifest.webmanifest` — install metadata
- `sw.js` — offline caching
- `icons/` — app icons

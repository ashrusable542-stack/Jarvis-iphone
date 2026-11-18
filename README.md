# JARVIS Advanced – iPhone 17

A local-first, installable PWA with a blue HUD, browser speech synthesis, optional speech recognition, local notes, and simple offline commands.

## Deploy to GitHub Pages
Upload the contents of this folder to the **root** of your existing `Jarvis-iphone` repository. Keep `assets/` as a folder. Commit to `main`. In Settings → Pages choose Deploy from a branch → `main` → `/(root)`. The site URL should be `https://YOUR-USERNAME.github.io/Jarvis-iphone/`.

## Install on iPhone
Open the published URL in Safari → Share → Add to Home Screen → enable Open as Web App → Add. Apple instructions: https://support.apple.com/guide/iphone/turn-a-website-into-an-app-in-safari-iph8e5236/ios

## Siri activation
Create a Shortcut named **JARVIS**:
1. Add **Dictate Text** (language: choose your preferred language; stop listening: After Pause).
2. Add **URL Encode** and pass the Dictated Text variable.
3. Add **URL** with this base address, then append `?q=` and the encoded text: `https://YOUR-USERNAME.github.io/Jarvis-iphone/`
4. Add **Open URLs**.
5. Name the shortcut exactly `JARVIS`.

Then say **“Hey Siri, JARVIS”**, dictate your request when prompted, and the JARVIS page opens with that request. Siri may ask for permission the first time. If Shortcuts does not expose URL Encode as an action on your iOS version, use the URL action and insert the Dictated Text variable; test with a short phrase.

## What it can and cannot do
- Works locally for time/date, simple planning prompts, local notes, and its interface.
- Uses iOS speech synthesis; speech recognition support varies by browser/device. Siri dictation is the reliable fallback.
- This starter does **not** contain a private LLM or cloud AI key. Use the AI chat tile to open ChatGPT for open-ended answers.
- A PWA cannot run a custom always-listening wake word or freely control iOS settings/other apps. Siri invokes the named Shortcut, and iOS permission prompts remain in place.
- Notes are stored in this browser's local storage. Clearing website data can erase them.
- No API keys, trackers, or remote backend are included.

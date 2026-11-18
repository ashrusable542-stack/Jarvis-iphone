# Siri Shortcut: “JARVIS”

Create this in Apple's Shortcuts app. Apple's supported pattern is to invoke a Shortcut by saying its name to Siri.

1. Tap `+` → New Shortcut → add **Dictate Text**. Set language to English, Hindi or Marathi as desired.
2. Add **URL Encode** (if available) and encode the Dictated Text result.
3. Add a **URL** action containing your deployed site URL followed by `?q=` and insert the encoded text variable.
   Example structure: `https://YOUR-USERNAME.github.io/Jarvis-iphone/?q=[Encoded Text]`
4. Add **Open URLs**.
5. Rename the shortcut `JARVIS`.
6. Say “Hey Siri, JARVIS”. Siri starts dictation, then opens your JARVIS PWA with the query.

If URL Encode isn't available, insert Dictated Text directly after `?q=` and test with a short request. For robust URL encoding, build the URL using Shortcuts' URL action's query parameter support if offered.

This is a Siri-triggered Shortcut, not an always-listening JARVIS wake word. iOS decides when microphone access is available.

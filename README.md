# JARVIS V2

Android personal assistant foundation with phone actions.

## V2 features
- Voice input
- Text-to-speech
- Contact lookup
- Confirm-before-call
- Phone calling
- Confirm-before-SMS
- SMS sending
- Web search
- Open selected apps
- Calendar event screen
- Alarm screen
- Secure-backend-ready architecture
- GitHub Actions APK build

## Commands
- "Call Rahul"
- "Send message to Rahul: I will reach at 7 PM"
- "Search latest IS 2062"
- "Open WhatsApp"
- "Open YouTube"
- "Set alarm tomorrow"
- "Calendar meeting with supplier"

## Build
Upload the project contents to GitHub, then use Actions → Build JARVIS V2 APK → Run workflow. Download the JARVIS-V2-debug-apk artifact.

## Important
Android will request permissions for contacts, phone calls and SMS. Calls and SMS have explicit confirmation dialogs in this version.

The current V2 still uses a local command engine for these actions. A secure AI backend should be connected next for natural-language understanding, live AI answers, PDF/image analysis, web research, memory and advanced assistant automation. Do not embed a production AI API key in the APK.


## JARVIS V2.1 – Hey JARVIS Wake Mode

Added a microphone foreground service using Android `SpeechRecognizer` to listen for the phrase **Hey JARVIS** after the user explicitly enables it from the visible app. After the wake phrase, JARVIS listens for one command and passes it to the main app.

Important Android behavior: the service must be started while the app is visible after microphone permission is granted. Android 14+ restricts starting microphone foreground services from the background. A persistent notification is shown while wake mode is active. This implementation is a practical prototype, not a dedicated low-power hardware hotword engine.

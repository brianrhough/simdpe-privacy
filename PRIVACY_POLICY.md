# Sim DPE — Privacy Policy

**Effective date:** April 23, 2026
**Developer:** Brian Hough
**Contact:** brian@houghmail.com

This Privacy Policy describes how the "Sim DPE — Private Pilot Prep" mobile app ("the App") handles your information.

---

## TL;DR

- We do **not** run servers that collect your data. The App talks to **your** self-hosted backend — you provide the URL and API key.
- The App requests **microphone** and **speech recognition** permission only so you can answer oral-exam questions out loud. Your audio is transcribed on your device and never stored by us.
- The transcripts and your quiz answers are sent to **your backend**, which forwards them to Anthropic (Claude) and ElevenLabs for question generation, grading, and the DPE's voice.
- Your progress is stored **locally on your iPhone** using SwiftData. Nothing is uploaded to a central server we operate.
- The App contains **no third-party analytics, no tracking, and no advertising identifiers**.

---

## 1. Information the App processes

### 1.1 Information you give us
- **Oral-exam speech** — when you tap "Hold to Talk" during an oral practice session, your voice is captured by the iPhone's microphone, transcribed on-device using Apple's Speech framework (or, when offline on-device recognition isn't available, via Apple's servers as permitted by iOS), and the resulting text is sent to your configured backend.
- **Typed answers** — when you answer a multiple-choice or short-answer question, your answer text is sent to your backend for grading.
- **ACS task selections** — which topic you're studying at any moment.

### 1.2 Information stored on your device only
Using Apple's SwiftData framework, the App stores:
- Your quiz attempts (question, your answer, score, feedback, timestamp)
- Your oral-session summaries (final score, date)
- App settings (dark mode, voice speed)

This data lives on your iPhone and is included in your encrypted device backup (iCloud or iTunes) if you enable it. It is not shared with us.

### 1.3 Information the App does **not** collect
- No name, email, phone number, or login credentials
- No location data
- No advertising identifier
- No device contacts, calendars, photos, or files
- No crash reports except the default Apple diagnostics (controlled by your iOS privacy settings)

---

## 2. Third-party services invoked by your backend

Your self-hosted SimDPE backend, when running, passes your questions and answers to:

- **Anthropic** (api.anthropic.com) — generates quiz questions, grades answers, and plays the DPE examiner role. Anthropic's privacy policy: https://www.anthropic.com/legal/privacy
- **ElevenLabs** (api.elevenlabs.io) — synthesizes the DPE's voice (text-to-speech). ElevenLabs' privacy policy: https://elevenlabs.io/privacy

These calls use API keys you register with Anthropic and ElevenLabs yourself. Those vendors process data per their own terms. We have no visibility into their usage of that data.

---

## 3. Permissions the App requests

| Permission | Why |
|---|---|
| **Microphone** (`NSMicrophoneUsageDescription`) | To capture your spoken answers during oral-exam practice. |
| **Speech Recognition** (`NSSpeechRecognitionUsageDescription`) | To convert your speech to text so the AI examiner can evaluate it. |

You can revoke either permission at any time in iOS Settings → Sim DPE. Revoking disables oral practice; typed quizzes continue to work.

---

## 4. Data retention

- **Local data** (quiz history, oral summaries, settings) — stored until you delete the App or reset its data from iOS Settings → General → iPhone Storage → Sim DPE → Delete App.
- **Remote data** — any data your backend logs or caches depends on how you configure it. Review your backend's logs policy.

We (the App developer) retain nothing. We have no account system, no telemetry, and no cloud database.

---

## 5. Children

The App is not directed to children under 13. FAA private-pilot knowledge preparation is a niche study tool for adults (minimum age for a U.S. private-pilot license is 17). We do not knowingly collect any information from children.

---

## 6. Your rights

Because we do not collect or store your data on any server we operate, there is nothing for us to export or delete. To erase all local app data, uninstall the App. To erase data stored by your self-hosted backend or the third-party APIs it invokes, follow their respective procedures.

---

## 7. Security

- All network traffic between the App and your backend uses HTTPS (App Transport Security is enforced).
- Your API key is stored in the App bundle's compiled code; no copy is transmitted to us.
- Local SwiftData storage is protected by iOS file-system encryption when your device is locked.

---

## 8. Accuracy disclaimer

Sim DPE uses AI to generate practice questions and simulate an oral examiner. **The App is a study aid, not official FAA content.** Always verify facts against current FAA publications (PHAK 8083-25, Airplane Flying Handbook 8083-3, the current ACS, AIM, and 14 CFR). Do not rely solely on the App for checkride preparation.

---

## 9. Changes to this policy

Material changes will be posted in the App and at the URL configured as the "Privacy Policy" link in App Store Connect. The effective date above will be updated whenever this policy changes.

---

## 10. Contact

Questions about this policy: brian@houghmail.com

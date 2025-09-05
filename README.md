# Fatigue Bot 🩺🤖

**Fatigue Bot** is a multilingual, privacy-first physiotherapy chatbot for fatigue assessment.  
It implements the **Fatigue Severity Scale (FSS)**, provides instant scoring, and offers **exercise recommendations** aligned with **WHO, APTA, and WCPT guidelines**.  

Built to be lightweight and deployable as a **single-page app** (no backend required).  

---

## 🌟 Features

- **Fatigue Severity Scale (FSS):** 9 validated questions with 1–7 scoring.  
- **Multilingual:** English • हिन्दी (Hindi) • اردو (Urdu).  
- **Voice Interaction:** Speech-to-Text (STT) & Text-to-Speech (TTS) via browser-native Web Speech API.  
- **Personalized Recommendations:** Evidence-based exercise advice based on fatigue levels:
  - Minimal, Moderate, Severe fatigue.  
- **Guidelines Integration:** Inline WHO, APTA, WCPT recommendations.  
- **Avatar & Bot Bubble:** Interactive, empathetic physiotherapy persona.  
- **Privacy-first:** All responses stored locally (browser storage).  
- **Deploy Anywhere:** Works with GitHub Pages, Netlify, or any static hosting.  

---

## 📂 Project Structure

```
fatigue-bot/
├── index.html    # Main app (single file)
├── logo.png      # App logo (place in root)
└── README.md     # This documentation
```

---

## 🚀 Setup & Deployment

### Option 1 — Quick Local Run
1. Clone or download the repo.
2. Place `index.html` and `logo.png` in the same folder.
3. Open `index.html` in Chrome/Edge (recommended for mic/voice support).

### Option 2 — GitHub Pages
1. Push files to a GitHub repo (e.g., `fatigue-bot`).
2. Go to **Settings → Pages**.
3. Select **Deploy from a branch**, choose `main` branch and `/ (root)`.
4. Save → Your app will be live at:
   ```
   https://your-username.github.io/fatigue-bot/
   ```

### Option 3 — GitHub Actions (Auto Deploy)
Add `.github/workflows/deploy.yml`:

```yaml
name: Deploy Fatigue Bot to GitHub Pages

on:
  push:
    branches: [ main ]

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/configure-pages@v5
      - uses: actions/upload-pages-artifact@v3
        with:
          path: .
      - uses: actions/deploy-pages@v4
```

Push → Deployment will auto-update on each commit.

---

## 🎤 Browser Requirements

- **Chrome / Edge:** Full support for Speech-to-Text & Text-to-Speech.  
- **Firefox / Safari:** Limited or no speech recognition support.  
- Ensure microphone permissions are granted.  

---

## 🧪 Usage

1. Select your language (EN/HI/UR).  
2. Accept consent modal.  
3. Answer the 9 FSS questions (1–7).  
   - Click buttons or dictate answers 🎙️.  
4. View results + interpretation.  
5. Read personalized exercise plan & WHO/APTA/WCPT guidelines.  

---

## 👨‍⚕️ Credits

Developed in India 🇮🇳 by **HSS, CSJMU, Kanpur**  
Designed for physiotherapy research and community health awareness.  

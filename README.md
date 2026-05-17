# SIGN**BRIDGE** 🤟
demo url:https://benevolent-bunny-d89e89.netlify.app

> **Real-time ASL sign language recognition — right in your browser.**

SignBridge uses MediaPipe Hands + a trained neural network to detect hand landmarks from your webcam and translate American Sign Language gestures into text, instantly, with no server, no install, and no data ever leaving your device.

---

## ✨ Features

- **Real-time hand tracking** — MediaPipe Hands detects 21 landmarks per hand at up to 60fps
- **AI gesture classification** — Neural network maps hand poses to ASL letters and words
- **100% on-device** — All processing runs in the browser; your camera feed is never uploaded
- **Zero setup** — No installation, no backend, no account — just open and sign
- **Accessible UI** — High-contrast dark interface designed with Deaf and hard-of-hearing users in mind
- **Responsive** — Works on laptop, tablet, and mobile

---

## 🚀 Getting Started

Because SignBridge uses WebAssembly and camera APIs, it **cannot** be opened by double-clicking the HTML file. You must serve it over a local HTTP server.

### Option 1 — Python (recommended, no install needed)

```bash
cd "/path/to/your/project/folder"
python3 -m http.server 8000
```

Then open your browser and go to:

```
http://localhost:8000/signbridge_complete.html
```

### Option 2 — VS Code Live Server

1. Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension
2. Right-click `signbridge_complete.html` → **Open with Live Server**

### Option 3 — Node.js

```bash
npx serve .
```

---

## 📁 Project Structure

```
parent-folder/
├── signbridge_complete.html   # Main app — hand tracking + recognition UI
├── signbridge_landing.html    # Landing page with links to the app
└── README.md
```

---

## 🧠 How It Works

```
Webcam Feed
    │
    ▼
MediaPipe Hands (WASM)
    │  Detects 21 hand landmarks per frame
    ▼
Landmark Normalization
    │  Positions scaled relative to wrist anchor
    ▼
Neural Network Classifier
    │  Maps landmark geometry → ASL gesture
    ▼
Text Output
    │  Letters assembled into words on screen
    ▼
Real-Time Display
```

---


---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Hand Tracking | [MediaPipe Hands](https://mediapipe.dev) |
| Gesture Classification | TensorFlow.js / custom neural network |
| Frontend | Vanilla HTML, CSS, JavaScript |
| Landing Page | HTML/CSS with CSS animations |
| Runtime | Browser (Chrome recommended) |

---

## 🌐 Browser Compatibility

| Browser | Support |
|---|---|
| Chrome / Chromium | ✅ Full support |
| Edge | ✅ Full support |
| Firefox | ⚠️ Partial (WASM may be slower) |
| Safari | ⚠️ Limited (WebAssembly restrictions) |
| Mobile Chrome | ✅ Works with rear/front camera |

---

## 🔒 Privacy

SignBridge is designed with privacy as a core principle:

- **No data collection** — zero analytics, zero tracking
- **No server communication** — the app works entirely offline after the initial page load
- **Camera feed stays local** — video is processed in-memory and never transmitted
- **No accounts or sign-up** required

---

## 📄 License

This project is open source. See [LICENSE](LICENSE) for details.

---

<div align="center">
  <strong>SIGN</strong>BRIDGE — Breaking the silence, one gesture at a time.
</div>

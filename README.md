# ZimaOS App Store (ovi1337)

This repository provides curated 3rd-party apps for **ZimaOS** and **CasaOS**.

## 📦 Included Apps

| App | Description | Category | Port | Image |
| --- | --- | --- | --- | --- |
| **Zima Explorer** | Modern dual-pane file manager for ZimaOS | Utilities | `8088` | `ghcr.io/ovi1337/zima-file-manager:v1.0.0` |
| **DeepSeek Harness** | AI Agent Harness with Playwright Google Search & Model Presets | AI | `3080` | `ghcr.io/src-one/deepseek-harness:latest` |
| **Gemini CLI** | Google Gemini CLI inside a ttyd browser terminal | Developer | `7682` | `ghcr.io/coolcow/gemini:latest` |

---

## How to add this store to ZimaOS

### Option 1: Via CLI (recommended)

Enable the command line in ZimaOS settings (Developer Options) and run:

```bash
casaos-cli app-management register app-store \
  https://github.com/ovi1337/zimaos-appstore/archive/refs/heads/main.zip
```

Replace `ovi1337` with your username if you forked this repo.

### Option 2: Via App Store UI

1. Open the App Store in ZimaOS.
2. Click **Add Source** (or "More Apps" / Settings).
3. Paste the following URL:
   ```
   https://github.com/ovi1337/zimaos-appstore/archive/refs/heads/main.zip
   ```
4. Confirm.

---

## Apps Overview

### 📁 Zima Explorer
A powerful, modern dual-pane file manager built specifically for ZimaOS.
- **Features:** Dual-pane explorer, Drag & Drop, Media preview (images, video, audio, PDF, text), File operations (upload, download, rename, delete, copy, move), Volume browser.
- **Port:** `8088` (maps to container `80`)
- **Image:** `ghcr.io/ovi1337/zima-file-manager:v1.0.0`

### 🤖 DeepSeek Harness (dsh)
An open-source agent framework developed by DeepSeek AI ("Everything is a Plugin") with integrated keyless Google Web Search (Playwright) and Selectable Model Modes.
- **Features:** AI agent harness with Playwright Google Search, selectable model modes, and workspace mounting for documents, downloads, media, and gallery.
- **Port:** `3080`
- **Image:** `ghcr.io/src-one/deepseek-harness:latest`

### 💻 Gemini CLI
Run the Google Gemini CLI directly inside a web browser terminal (powered by ttyd).
- **Features:** Web-based terminal access for Gemini CLI directly on your ZimaOS dashboard.
- **Port:** `7682` (maps to container `7681`)
- **Image:** `ghcr.io/coolcow/gemini:latest`
- **Setup:** Insert your Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikeys) in the app settings before starting.

---

## Repository Structure

```
zimaos-appstore/
└── Apps/
    ├── DeepSeekHarness/
    │   └── docker-compose.yml
    ├── gemini-cli/
    │   └── docker-compose.yml
    └── zima-explorer/
        └── docker-compose.yml
```

---

## License

The app definitions in this repository are provided under the MIT License.

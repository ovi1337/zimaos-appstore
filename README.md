# ZimaOS App Store (ovi1337)

Curated 3rd-party App Store for **ZimaOS** and **CasaOS** supporting both **Protocol V2 (`store.json`)** and **Legacy V1 (`main.zip`)**.

---

## 📦 Included Apps

| App | Description | Category | Port | Image |
| --- | --- | --- | --- | --- |
| **Zima Explorer** | Modern dual-pane file manager for ZimaOS | Utilities | `8088` | `ghcr.io/ovi1337/zima-file-manager:v1.0.0` |
| **DeepSeek Harness** | AI Agent Harness with Playwright Google Search & Model Presets | AI | `3080` | `ghcr.io/src-one/deepseek-harness:latest` |
| **Gemini CLI** | Google Gemini CLI inside a ttyd browser terminal | Developer | `7682` | `ghcr.io/coolcow/gemini:latest` |

---

## 🚀 Adding the Store to ZimaOS / CasaOS

### Option 1: Modern Protocol V2 URL (Recommended)

In modern ZimaOS & CasaOS (v0.4.4+), paste the **`store.json` URL** directly into the App Store source input:

```
https://ovi1337.github.io/zimaos-appstore/store.json
```

*Alternative Raw GitHub URL:*
```
https://raw.githubusercontent.com/ovi1337/zimaos-appstore/main/store.json
```

---

### Option 2: Legacy V1 ZIP Archive

#### Via App Store UI:
1. Open the App Store in ZimaOS / CasaOS.
2. Click **Add Source** (or "More Apps" / Store Settings).
3. Paste the following URL:
   ```
   https://github.com/ovi1337/zimaos-appstore/archive/refs/heads/main.zip
   ```
4. Confirm.

#### Via CLI:
Enable Developer Options / CLI in ZimaOS settings and run:
```bash
casaos-cli app-management register app-store \
  https://github.com/ovi1337/zimaos-appstore/archive/refs/heads/main.zip
```

---

## 📱 Apps Overview

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

## 🏗️ Repository Structure

```
zimaos-appstore/
├── store.json                      # V2 Store Definition
├── store-config.json               # V2 Store Metadata Source
├── supported-languages.json        # Supported Locales
├── category-list.json              # Category taxonomy
├── recommend-list.json             # Featured apps
├── Apps/
│   ├── DeepSeekHarness/
│   │   └── docker-compose.yml
│   ├── gemini-cli/
│   │   └── docker-compose.yml
│   └── zima-explorer/
│       └── docker-compose.yml
└── .github/workflows/
    ├── build-store.yml             # V2 Build & Pages Deployment
    ├── release.yml
    └── validate.yml
```

---

## 📄 License

The app definitions in this repository are provided under the MIT License.

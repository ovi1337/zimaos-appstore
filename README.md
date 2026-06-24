# ZimaOS App Store - Zima Explorer

This repository provides **Zima Explorer** as a 3rd-party app for ZimaOS (and CasaOS).

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
2. Click **Add Source** (or "More Apps").
3. Paste the following URL:
   ```
   https://github.com/ovi1337/zimaos-appstore/archive/refs/heads/main.zip
   ```
4. Confirm.

## About Zima Explorer

Zima Explorer is a modern, dual-pane file manager built specifically for ZimaOS.

**Features:**
- Dual-pane explorer
- Drag & Drop + Multiselect
- Media preview (images, video, audio, PDF, text)
- Full file operations (upload, download, rename, delete, copy, move)
- Volume browser
- Statistics and file details

**Image:** `ghcr.io/ovi1337/zima-file-manager:latest`

**Important:** For the best user experience when installing from this 3rd-party store, make the GHCR package public. No login or token will be required.

Instructions:
1. Go to https://github.com/ovi1337?tab=packages
2. Open **zima-file-manager**
3. Package settings → Change visibility → Public

Once done, the app installs directly without any extra steps.

## Repository Structure

```
zimaos-appstore/
└── Apps/
    └── zima-explorer/
        └── docker-compose.yml     # Contains full x-casaos metadata
```

## For Developers

If you want to host your own version of this store:

1. Fork this repository.
2. Update the image reference in `Apps/zima-explorer/docker-compose.yml` if needed.
3. Update the zip URL when registering the store.
4. (Optional) Improve metadata, add more screenshots, or translate descriptions.

**Recommended:** Make the GHCR package public for a frictionless store experience.

## License

The app definition in this repository is provided under MIT.

The actual Zima Explorer application source code lives in a separate (private) repository.

## Links

- Main project: https://github.com/ovi1337/zima-file-manager
- Docker image: ghcr.io/ovi1337/zima-file-manager

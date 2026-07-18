<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo/logo_horizontal_dark.png">
    <source media="(prefers-color-scheme: light)" srcset="logo/logo_horizontal_transparent.png">
    <img alt="CK Image & PDF Reducer" src="logo/logo_horizontal_transparent.png" width="480">
  </picture>
</p>

<p align="center">
  <b>A free, offline, drag-and-drop tool for shrinking images and PDFs — no uploads, no subscriptions.</b>
</p>

<p align="center">
  <a href="https://github.com/epatels/ck-image-pdf-reducer/releases/latest">
    <img alt="Latest release" src="https://img.shields.io/github/v/release/epatels/ck-image-pdf-reducer?label=download">
  </a>
  <img alt="Platform" src="https://img.shields.io/badge/platform-Windows-blue">
</p>

---

## Download

**[⬇ Download the latest Windows installer](https://github.com/epatels/ck-image-pdf-reducer/releases/latest)**

No installer for your platform yet — the app currently ships for Windows only.

## Installing

### Option A: Winget (recommended)

```
winget install epatels.CKImagePDFReducer
```

### Option B: curl

Running the installer with no arguments opens the interactive setup wizard — the terminal isn't stuck, it's just waiting for you to click through that window (Next → Install → Finish). For a real one-command install, unblock the download and pass the silent switches:

**Command Prompt (cmd.exe):**

```
curl -L -o CKImagePDFReducerSetup.exe https://github.com/epatels/ck-image-pdf-reducer/releases/latest/download/CKImagePDFReducerSetup.exe && powershell -Command "Unblock-File CKImagePDFReducerSetup.exe" && CKImagePDFReducerSetup.exe /VERYSILENT /SUPPRESSMSGBOXES /NORESTART
```

**PowerShell:**

```powershell
curl.exe -L -o CKImagePDFReducerSetup.exe https://github.com/epatels/ck-image-pdf-reducer/releases/latest/download/CKImagePDFReducerSetup.exe; Unblock-File CKImagePDFReducerSetup.exe; .\CKImagePDFReducerSetup.exe /VERYSILENT /SUPPRESSMSGBOXES /NORESTART
```

> **Notes:**
> - Each block above is a single line — paste it as one and press Enter once. (If you instead paste the multi-line version of a command, most terminals won't auto-run the last line; you'll need to press Enter yourself to execute it. That's normal terminal behavior, not a stuck install.)
> - In PowerShell, `curl` is an alias for `Invoke-WebRequest` and doesn't accept `-L`/`-o` the same way, so use `curl.exe` explicitly to run the real curl that ships with Windows 10/11. PowerShell also requires the `.\` prefix to run an exe from the current directory.
> - `Unblock-File` clears the "downloaded from the internet" flag Windows attaches to curl'd files, which can otherwise trigger a SmartScreen prompt that silently blocks the install if its window doesn't have focus.
> - Want to see progress instead of a fully silent install? Drop `/VERYSILENT` down to `/SILENT` — it shows a progress bar but still skips all the click-through prompts.
> - Omit the switches entirely to get the normal interactive wizard.

### Option C: Manual download

1. Download `CKImagePDFReducerSetup.exe` from [Releases](https://github.com/epatels/ck-image-pdf-reducer/releases/latest).
2. Run it — no admin rights needed, it installs per-user.

On first PDF compression, it'll walk you through installing [Ghostscript](https://www.ghostscript.com), a free, separate program the app calls out to. Ghostscript itself is never bundled or copied into this app.

## What it does

CK Image & PDF Reducer compresses images and PDFs right on your PC. Drag a file in, pick how you want it shrunk, and export — nothing is sent anywhere.

- **Resize by percentage** — scale both dimensions down together
- **Fix Width / Fix Height** — set one dimension, the other auto-scales to preserve aspect ratio
- **Compress by Quality** — reduce JPEG quality to hit a smaller file size
- **Target File Size** — tell it a size limit (e.g. "under 200 KB") and it searches for the best quality/resolution that fits
- **PDF compression** — shrinks PDFs by recompressing embedded images (via Ghostscript, installed separately on first use)
- **Batch queue** — load and process multiple files in one pass
- **Drag & drop** — drop files straight onto the window
- **Windows right-click menu** — optional "Reduce with CK Image & PDF Reducer" entry in Explorer's context menu
- **HEIC support** — reads iPhone-style HEIC images

## Source code

This repo ships the compiled installer only — source isn't published here. If you'd like a copy, open a [source request](https://github.com/epatels/ck-image-pdf-reducer/issues/new?labels=source-request&template=source_request.md) issue, or use **Help → Request Source Code** inside the app, and it'll be sent over at no charge.

## Support

Questions, bugs, or feature requests — open an issue on this repo, or use **Help → Contact Developer** inside the app.

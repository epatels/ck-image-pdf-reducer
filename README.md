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

## Installing

1. Download `CKImagePDFReducerSetup.exe` from [Releases](https://github.com/epatels/ck-image-pdf-reducer/releases/latest).
2. Run it — no admin rights needed, it installs per-user.
3. On first PDF compression, it'll walk you through installing [Ghostscript](https://www.ghostscript.com), a free, separate program the app calls out to. Ghostscript itself is never bundled or copied into this app.

## Source code

This repo ships the compiled installer only — source isn't published here. If you'd like a copy, open a [source request](https://github.com/epatels/ck-image-pdf-reducer/issues/new?labels=source-request&template=source_request.md) issue, or use **Help → Request Source Code** inside the app, and it'll be sent over at no charge.

## Support

Questions, bugs, or feature requests — open an issue on this repo, or use **Help → Contact Developer** inside the app.

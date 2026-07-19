<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo/logo_horizontal_dark.png">
    <source media="(prefers-color-scheme: light)" srcset="logo/logo_horizontal_transparent.png">
    <img alt="CK Image & PDF Reducer" src="logo/logo_horizontal_transparent.png" width="480">
  </picture>
</p>

<p align="center">
  <b>Shrink images and PDFs on your own PC — no uploads, no cloud, no subscriptions.</b>
  <br>
  Drag a file in, pick a target, export. That's the whole workflow.
</p>

<p align="center">
  <a href="https://github.com/epatels/ck-image-pdf-reducer/releases/latest"><b>⬇ Latest release</b></a> &nbsp;·&nbsp;
  <b>Windows</b> &nbsp;·&nbsp;
  <b>Free</b> &nbsp;·&nbsp;
  <b>100% Offline</b>
</p>

<p align="center">
  <a href="#download">Download</a> ·
  <a href="#why-people-trust-it">Why trust it</a> ·
  <a href="#what-it-does">Features</a> ·
  <a href="#installing">Install</a> ·
  <a href="#faq">FAQ</a> ·
  <a href="#support">Support</a>
</p>

---

## Download

**[⬇ Download the latest Windows installer](https://github.com/epatels/ck-image-pdf-reducer/releases/latest)**

No installer for your platform yet — the app currently ships for Windows only.

## Why people trust it

- **Your files never leave your machine.** Compression happens locally — there's no upload step to skip, because there's no server to upload to.
- **No account, no email, no subscription.** Download it, run it, use it.
- **No ads, ever.** No banners, no sponsored placements, nothing tracking you across the web to sell you something.
- **Nothing hidden in the install.** Ghostscript, the only external program the app relies on for PDF compression, is installed separately, with your consent, directly from its official source — never bundled or silently dropped in.
- **Source available on request.** The compiled installer is what ships in Releases, but the full source is yours for the asking — see [Source code](#source-code) below.
- **Actively maintained.** Versioned releases, a public issue tracker, and a direct line to the developer through the app itself.

## What it does

CK Image & PDF Reducer compresses images and PDFs right on your PC. Drag a file in, pick how you want it shrunk, and export — nothing is sent anywhere.

| Mode | What it's for |
|---|---|
| **Resize by percentage** | Scale both dimensions down together |
| **Fix Width / Fix Height** | Set one dimension, the other auto-scales to preserve aspect ratio |
| **Compress by Quality** | Reduce JPEG quality to hit a smaller file size |
| **Target File Size** | Tell it a size limit (e.g. "under 200 KB") and it searches for the best quality/resolution that fits |
| **PDF Compression** | Shrinks PDFs by recompressing embedded images, text stays vector (via Ghostscript, installed separately on first use) |
| **PDF Target File Size** | Same idea as image target-size mode, capped by a visual-quality safety floor |

Beyond the core modes:

- **Convert formats** — output as JPEG, PNG, WebP, BMP, or TIFF regardless of the source format (or just keep it the same)
- **Batch queue** — load and process multiple files in one pass
- **Drag & drop** — drop files straight onto the window
- **Windows right-click menu** — optional "Reduce with CK Image & PDF Reducer" entry in Explorer's context menu
- **HEIC support** — reads iPhone-style HEIC images

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

> **Notes**
> - Each block above is a single line — paste it as one and press Enter once. If you paste a multi-line version instead, most terminals won't auto-run the last line; press Enter yourself to execute it. That's normal terminal behavior, not a stuck install.
> - In PowerShell, `curl` is an alias for `Invoke-WebRequest` and doesn't accept `-L`/`-o` the same way, so use `curl.exe` explicitly to run the real curl that ships with Windows 10/11. PowerShell also requires the `.\` prefix to run an exe from the current directory.
> - `Unblock-File` clears the "downloaded from the internet" flag Windows attaches to curl'd files, which can otherwise trigger a SmartScreen prompt that silently blocks the install if its window doesn't have focus.
> - Want to see progress instead of a fully silent install? Drop `/VERYSILENT` down to `/SILENT` — it shows a progress bar but still skips all the click-through prompts.
> - Omit the switches entirely to get the normal interactive wizard.

### Option C: Manual download

1. Download `CKImagePDFReducerSetup.exe` from [Releases](https://github.com/epatels/ck-image-pdf-reducer/releases/latest).
2. Run it — no admin rights needed, it installs per-user.

On first PDF compression, it'll walk you through installing [Ghostscript](https://www.ghostscript.com), a free, separate program the app calls out to. Ghostscript itself is never bundled or copied into this app.

## FAQ

**Does this upload my files anywhere?**
No. Every compression runs locally on your machine. There's no server component and no network step in the compression path itself.

**Why does it need Ghostscript for PDFs?**
Ghostscript handles the actual PDF recompression work. It's a well-established, free, open project — the app just calls it as an external tool, the same way it would call any other program already on your PC, rather than reimplementing that logic itself.

**Is it really free?**
Yes — no trial, no paywalled features, no subscription.

**What if I hit a bug or want a feature?**
Open an issue on this repo, or use **Help → Contact Developer** inside the app — see [Support](#support).

## Source code

This repo ships the compiled installer only — source isn't published here. If you'd like a copy, open a [source request](https://github.com/epatels/ck-image-pdf-reducer/issues/new?labels=source-request&template=source_request.md) issue, or use **Help → Request Source Code** inside the app, and it'll be sent over at no charge.

## Support

Questions, bugs, or feature requests — open an issue on this repo, or use **Help → Contact Developer** inside the app.

---

<p align="center"><sub>Built for people who just want a smaller file, not another account to manage.</sub></p>

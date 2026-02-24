# 🛡 Tactical FieldKit

**100% offline SITREP generator + image sanitizer**
Privacy-first • Zero network • Zero metadata leaks • Works on any phone after one load.

[![Offline](https://img.shields.io/badge/Offline-100%25-brightgreen)](https://github.com/MiMindMendinc/Tactical-FieldKit)
[![Privacy](https://img.shields.io/badge/Privacy-First-blue)](https://github.com/MiMindMendinc/Tactical-FieldKit)
[![PWA](https://img.shields.io/badge/PWA-Ready-purple)](https://github.com/MiMindMendinc/Tactical-FieldKit)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![2026-ready](https://img.shields.io/badge/2026-Ready-orange)](https://github.com/MiMindMendinc/Tactical-FieldKit)

> Built for field operators, LE, journalists & NGOs who need real OPSEC.

---

## Overview

Tactical FieldKit is a single-file progressive web app (PWA) that runs **entirely in the browser** — no server, no cloud, no tracking. Load it once and it works forever offline.

Two tools in one:
- **METHANE-style SITREP generator** — structured incident reports with GPS auto-fill and UTC timestamps.
- **Image sanitizer** — strips ALL EXIF/GPS/camera metadata from photos on-device, with optional manual redaction.

---

## Features

| Feature | Detail |
|---|---|
| 📋 METHANE SITREP | Structured format: Major, Exact location, Type/Hazards, How many casualties, Access, Number of services |
| 📍 GPS auto-fill | One-tap coordinates (±accuracy) inserted into location field |
| 🕐 UTC timestamps | Every report stamped in UTC/ISO format |
| 📋 Copy & Share | Copy to clipboard or native OS share sheet |
| 🖼 EXIF stripper | All metadata removed via canvas round-trip — no EXIF survives |
| ✏️ Redaction | Draw black boxes over sensitive areas before export |
| 💾 JPEG / PNG export | Choose format, download sanitized file |
| 📲 Install as PWA | Add to Home Screen on iOS or Android (feels like a native app) |
| 🔒 100% on-device | Zero network requests after first load, zero analytics |

---

## How to Use

### Desktop
1. Open the [live site](https://mimindmendinc.github.io/Tactical-FieldKit/)
2. Fill in the SITREP fields → **Generate SITREP** → Copy or Share
3. For images: upload a photo → toggle **Redact: ON** → draw boxes → **Export JPEG/PNG**

### Phone (iOS / Android)
1. Open the live link in your mobile browser
2. For SITREP: tap **📍 Auto-fill GPS** to insert coordinates automatically
3. For images: tap the upload area, pick a photo from your gallery or camera

---

## Install as PWA

### Android (Chrome)
1. Open the site in Chrome
2. Tap the **📲 Install on Home Screen** button that appears at the top
3. Or tap the browser menu (⋮) → **Add to Home screen**

### iOS (Safari)
1. Open the site in Safari
2. Tap the **Share** icon (□↑)
3. Scroll down → tap **Add to Home Screen**
4. Tap **Add** — the app icon appears on your home screen

Once installed, the app works fully offline — no internet needed.

---

## Screenshots

| SITREP screen | Image with redaction | Sanitized export |
|---|---|---|
| GPS auto-filled, UTC timestamp, Copy/Share buttons | Black redaction boxes drawn over sensitive areas | Clean JPEG/PNG downloaded with zero EXIF metadata |

---

## Tech Stack

| Component | Detail |
|---|---|
| **Single HTML file** | All UI, logic, and styles in `index.html` — no build step |
| **Service Worker** | `sw.js` caches assets for 100% offline use |
| **Web App Manifest** | `manifest.json` enables PWA install on mobile |
| **Canvas API** | Used for EXIF stripping and redaction drawing |
| **Clipboard API** | One-click copy with fallback for older browsers |
| **Web Share API** | Native OS share sheet on mobile |
| **Geolocation API** | GPS auto-fill for SITREP location field |
| No frameworks | Vanilla HTML/CSS/JS — fast, auditable, no supply chain risk |

---

## Deployment (GitHub Pages)

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set Source → **Deploy from branch** → `main` → `/ (root)` → **Save**
4. Wait 30–60 seconds → your live URL appears at the top of the Pages settings

Your URL: `https://YOURUSERNAME.github.io/Tactical-FieldKit/`

---

## License

MIT — free to use, modify, and share.

**Ethical use only. Keep OPSEC. Verify your agency policies before sharing.**

---

*Built with ❤️ for field operators who need real OPSEC.*

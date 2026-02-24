# 🛡️ Tactical FieldKit

> **100% offline SITREP generator + image sanitizer.**
> Privacy-first · Zero network · Zero metadata leaks.
> Built for field teams, law enforcement, journalists &amp; NGOs.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-58a6ff?style=flat-square&logo=github)](https://mimindmendinc.github.io/Tactical-FieldKit/)
[![Offline Ready](https://img.shields.io/badge/Offline-100%25-3fb950?style=flat-square&logo=pwa)](https://mimindmendinc.github.io/Tactical-FieldKit/)
[![Privacy First](https://img.shields.io/badge/Privacy-First-8957e5?style=flat-square&logo=shield)](https://github.com/MiMindMendinc/Tactical-FieldKit)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/MiMindMendinc/Tactical-FieldKit?style=flat-square&color=f0e68c)](https://github.com/MiMindMendinc/Tactical-FieldKit/stargazers)

---

## 📋 Table of Contents

- [Features](#-features)
- [Screenshots](#-screenshots)
- [How to Install &amp; Use](#-how-to-install--use)
- [Why This Exists](#-why-this-exists--opsec-rationale)
- [FAQ](#-faq)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

| # | Feature | Description |
|---|---------|-------------|
| 🗂️ | **Structured SITREP Generator** | Fill in a guided form — callsign, DTG, location, situation, mission, execution, logistics, command &amp; signal — and export a properly formatted report in seconds. |
| 🖼️ | **Image Metadata Sanitizer** | Drag-and-drop images to strip all EXIF data (GPS coordinates, device model, timestamps) via HTML5 Canvas re-render. Nothing leaves your device. |
| ✏️ | **Redaction Mode** | Toggle on-the-fly redaction of IP addresses, email addresses, frequencies, and numeric identifiers before copying or exporting. |
| 📲 | **Installable PWA** | Install directly from the browser — no app store, no account. Works fully offline after first load. |
| 🔒 | **Zero Network** | No CDN, no fonts, no analytics, no beacon. Single-file HTML. Verified with DevTools Network panel. |
| ⌨️ | **Keyboard Shortcuts** | `Ctrl / ⌘ + Enter` generates SITREP. Designed for speed in high-tempo environments. |
| ♿ | **Accessible** | ARIA labels, roles, live regions, and proper tab semantics throughout. |
| 💾 | **Export** | Download SITREP as a timestamped `.txt` file or copy to clipboard with one click. |
| 🎨 | **Dark UI** | GitHub-style dark theme — easy on the eyes in low-light field conditions. |

---

## 📸 Screenshots

### SITREP Generator
![SITREP Generator screenshot](https://picsum.photos/800/600?random=1)

### Image Sanitizer
![Image Sanitizer screenshot](https://picsum.photos/800/600?random=42)

### Mobile View
![Mobile view screenshot](https://picsum.photos/800/600?random=77)

---

## 🚀 How to Install &amp; Use

### Option A — Browser (Desktop or Mobile)

1. **Open the live demo:**
   ```
   https://mimindmendinc.github.io/Tactical-FieldKit/
   ```

2. **Or clone and open locally:**
   ```bash
   git clone https://github.com/MiMindMendinc/Tactical-FieldKit.git
   cd Tactical-FieldKit
   # Open index.html in any modern browser — no server required
   open index.html        # macOS
   start index.html       # Windows
   xdg-open index.html    # Linux
   ```

3. **Select your module** using the tabs at the top:
   - 📋 **SITREP** — fill in the form fields and press `Generate SITREP` (or `Ctrl+Enter`)
   - 🖼️ **Image Sanitizer** — drag images onto the drop zone or click to browse
   - ℹ️ **About** — OPSEC notes and tool information

4. **Export or copy** your report using the buttons that appear after generation.

---

### Option B — Add to Home Screen (iPhone / Android)

**iPhone (Safari):**

1. Open the link in **Safari** (not Chrome or Firefox)
2. Tap the **Share icon** (square with arrow) at the bottom of the screen
3. Scroll down and tap **"Add to Home Screen"**
4. Name it `FieldKit` → tap **Add**
5. The app icon will appear on your home screen — it works **fully offline**

**Android (Chrome):**

1. Open the link in **Chrome**
2. Tap the **⋮ menu** (three dots, top-right)
3. Tap **"Add to Home Screen"** or **"Install App"**
4. Confirm by tapping **Add** / **Install**
5. The app is now installed and works offline

---

### Option C — Self-Host (Air-Gapped / Secure Network)

1. Copy `index.html` to any web server, USB drive, or internal file share
2. No build step, no dependencies — it is a single file
3. For maximum OPSEC: copy to a USB drive and open directly on an air-gapped device

---

## 🔐 Why This Exists — OPSEC Rationale

Modern smartphones and laptops **leak identifying metadata** in ways most operators never consider:

- 📍 **Photos contain GPS coordinates** accurate to within meters — embedded silently by every camera app
- 🕐 **EXIF timestamps** reveal when and where you were — even if the filename is scrubbed
- 📱 **Device model and OS version** are embedded in image files and can be used to fingerprint your kit
- ☁️ **Online SITREP tools** send your operational data to third-party servers — creating an exploitable record

**Tactical FieldKit removes these risks:**

- Images are re-rendered through a Canvas element, which does not copy EXIF data
- SITREP data never leaves the device — all processing is in-browser JavaScript
- The tool can be used in **Airplane Mode** for absolute network isolation
- The single-file design means you can verify every line of code before use

> *"Trust, but verify. Then verify again."*
> If you are operating in a hostile signals environment, turn off Wi-Fi and cellular before use.

---

## ❓ FAQ

**Q: Does this tool send any data to a server?**
A: No. Zero network requests are made after the page loads. You can verify this yourself by opening DevTools → Network tab and watching for requests while using the tool.

**Q: How does the image sanitizer work?**
A: Each image is drawn onto an HTML5 `<canvas>` element and then exported as a new JPEG. The canvas API does not copy EXIF metadata, so the output image contains only raw pixel data with no embedded location, device, or timestamp information.

**Q: Can I use this on a phone with no internet connection?**
A: Yes. Install it as a PWA (Add to Home Screen) and it will work completely offline from that point forward. The entire app is contained in one HTML file with no external resources.

**Q: Is the redaction feature legally sufficient for classified documents?**
A: No. The redaction mode is a convenience tool for masking common sensitive patterns (IPs, emails, frequencies). It is not a certified redaction solution. For classified material, follow your organization's approved redaction procedures.

**Q: Can I trust this code?**
A: The entire application is a single `index.html` file with no minification and no external dependencies. You can read every line of it. It is MIT-licensed and open source. If you need absolute assurance, audit the code yourself before use.

---

## 🤝 Contributing

Contributions that keep the tool **simple, offline, and dependency-free** are welcome.

1. Fork the repository
2. Make your changes to `index.html`
3. Test in at least two browsers
4. Open a pull request with a clear description of what changed and why

Please do **not** add external CDN resources, analytics, or anything that would cause network requests.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for full text.

---

<div align="center">

⭐ **Star the repo** · 📤 **Share with your team** · 🛡️ **Built for operators who need real privacy**

*If this tool has helped you work more securely, consider starring the repository so others in the community can find it.*

</div>

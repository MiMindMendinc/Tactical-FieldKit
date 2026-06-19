# Tactical-FieldKit

Browser-based SITREP drafting and image re-encoding prototype with GPS and manual redaction tools.

## Technical Summary
- **Architecture**: Single-file PWA, no server dependency
- **Features**: METHANE SITREP format, GPS auto-fill, UTC timestamps
- **Privacy feature**: Canvas-based image re-encoding, plus manual redaction tools
- **Performance**: Works offline after initial load, installable on mobile
- **Integration**: Clipboard/Web Share APIs, geolocation

## Impact
Demonstrates a local-first field-workflow UI. It is not an audited OPSEC product, and exported files should be independently inspected before sensitive use.

## Quick Start
Visit [live site](https://mimindmendinc.github.io/Tactical-FieldKit/) or:
```bash
git clone https://github.com/MiMindMendinc/Tactical-FieldKit.git
cd Tactical-FieldKit
# Open index.html in browser
```

## Features
- Offline SITREP generation
- GPS coordinate integration
- Canvas-based image re-encoding intended to omit source EXIF metadata
- PWA deployment

## License
MIT - Supporting field operations with reliable tools.

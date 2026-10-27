# Developer Toolkit (English README)

> 
> Zero-deployment, backend-free, fully client-side developer utility collection. Open and use directly, **all data stays locally in your browser and never uploads to any server**.

---

## ✨ Features

| Item | Description |
| --- | --- |
| **Pure static site** | Built with plain HTML + CSS + JS. No build tools or backend required. Just open the HTML file locally. |
| **Privacy-first** | All encoding, hashing, encryption and image processing run locally inside your browser. No data is sent externally. |
| **Dual theme support** | Light / dark mode, your preference is saved automatically. Consistent UI across all pages. |
| **Responsive layout** | Works on PC, tablet and mobile. Collapsible navigation for small screens. |
| **Easy extension** | Central menu config array. Add new tools by simply inserting one configuration entry. Supports homepage recommended cards. |
| **Free static hosting** | Deploy on Nginx, GitHub Pages, Cloudflare Pages or any static host without extra configuration. |

---

## 🛠️ Tool List

### 🔧 Developer Tools

| Tool Name | File Path | Description |
| --- | --- | --- |
| JSON Tool | `./dev/code/json.html` | JSON format / minify / validate / tree view / JSONPath query |
| Base64 Encode & Decode | `./dev/code/base64.html` | Text & image Base64, Base64Url conversion |
| MD5 Hash | `./dev/code/md5.html` | Calculate MD5 digest for plain text |
| SHA Hash | `./dev/code/sha.html` | SHA-1 / SHA-256 / SHA-512 multi-algorithm hash generator |
| JWT Parser | `./dev/code/jwt.html` | Parse, generate and verify JWT tokens |
| URL Encode & Decode | `./dev/code/url.html` | URL escape / unescape, handle Chinese characters |
| Timestamp Converter | `./time/timestamp.html` | Convert between Unix timestamp and readable date time, support seconds / milliseconds |
| WebSocket Debugger | `./network/ws.html` | Online WebSocket test client, send & receive messages |

### 📝 Text Utilities

| Tool Name | File Path | Description |
| --- | --- | --- |
| Text Case Converter | `./text/case.html` | Uppercase / lowercase / capitalize / camelCase / snake_case |
| Random Password Generator | `./text/pwd.html` | Custom length & character set, password strength indicator |
| Text Compressor | `./text/compress.html` | Gzip / deflate compress & decompress text, output Base64 |
| Line Deduplication | `./text/unique.html` | Remove duplicate lines, optional ignore-case and trim whitespace |
| Regex Tester | `./text/regex.html` | Test regular expression match & replace, support g / i / m flags |

### 🖼️ Image & Media Tools

| Tool Name | File Path | Description |
| --- | --- | --- |
| Bulk Image Compressor | `./media/image/compress.html` | Drag & drop multiple images, adjustable quality, format selection, before/after preview, ZIP batch download |
| Color Converter | `./media/image/color.html` | HEX / RGB / HSL conversion, color picker, live preview |

### 📦 Other Utilities

| Tool Name | File Path | Description |
| --- | --- | --- |
| QR Code Tool | `./other/qrcode.html` | Generate QR codes with custom size, margin, color, logo; also scan & decode QR from image |

### 🎮 Mini Games

| Game Name | File Path | Description |
| --- | --- | --- |
| Minesweeper | `./game/mine.html` | Preset easy / medium / hard difficulty, custom rows, columns and mine count, timer, flag marking |

---

## 🚀 Quick Start

### Local usage

Double-click `index.html` in root folder to open it in your browser.

### Online deployment

Upload the whole folder to any static file host. No runtime environment needed.

```
# Simple local static server (optional)
npx serve .
# Or python built-in server
python3 -m http.server 8080
```

---

## 📂 Project Structure

```
├── index.html                 # Homepage & navigation config
├── dev/
│   └── code/                  # Encode & hash tools
│       ├── base64.html
│       ├── md5.html
│       ├── sha.html
│       ├── jwt.html
│       └── url.html
├── time/
│   └── timestamp.html         # Timestamp converter
├── network/
│   └── ws.html                # WebSocket debugger
├── text/
│   ├── case.html              # Text case convert
│   ├── pwd.html               # Password generator
│   ├── compress.html          # Text gzip
│   ├── unique.html            # Line deduplicate
│   └── regex.html             # Regex tester
├── media/
│   └── image/
│       ├── compress.html      # Image compressor
│       └── color.html         # Color convert
├── other/
│   └── qrcode.html            # QR code generator & scanner
└── game/
    └── mine.html              # Minesweeper
```

---

## 🎨 Add New Tools

All navigation items are defined inside the `appList` array in `index.html`.
Add a new tool by inserting an item like this:

```
{
  name: 'Tool Name',
  url: './path/to.html',
  icon: 'fa-code',
  desc: 'Brief description of this tool',
  homeRecommend: true
}
```

Group styles (group name, icon, accent color) are configured on parent nodes.

---

## 🧰 Tech Stack

- Core: HTML5 / CSS3 / Vanilla JavaScript ES6+
- Styling: Tailwind CSS 3 (CDN)
- Icons: Font Awesome 6.4
- External libraries (loaded via CDN only):
  - `pako`: gzip / deflate compression
  - `qrcode.js` / `jsQR`: QR generate & decode
  - `jszip`: ZIP archive download

---

## ⚠️ Notes

1. All calculations run locally in your browser. Sensitive data will not be uploaded.
2. Internet connection is required for first load to fetch CDN CSS and JS assets.
3. When bulk downloading files, your browser may prompt for permission to download multiple files. Allow it.
4. In Minesweeper, **right-click is used to place flags**. Default browser right-click menu is disabled.

---

© 2026 Developer Toolkit
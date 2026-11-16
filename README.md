[readme.md](https://github.com/user-attachments/files/34929740/readme.md)
# Random Aesthetic Generator 🎨✒️

**Color and type, in one click.**

Random Aesthetic Generator is a zero-dependency, single-file web application designed to help designers and developers quickly discover, customize, test, and export harmonious 6-color palettes paired with curated Google Fonts typography.

---

## ✨ Features

### 🎨 Color Palette Generation & Tuning
- **One-Click Shuffling:** Instantly generate harmonious 6-color palettes alongside curated font pairings with mood descriptions.
- **15 Curated Palettes:** Browse and apply built-in presets (*Minimal, Playful, Bold, Coastal Glass, Citrus Club, Night Market*, and more).
- **Image-to-Palette Extraction:** Drag and drop or upload any JPEG or PNG (up to 15 MB) to extract 6 representative colors locally in your browser using a median-cut color quantization algorithm.
- **Individual Swatch Tuning:** Select any of the 6 swatches to fine-tune its exact HEX value via a color picker or adjust its saturation via a slider.
- **One-Click Copy:** Click any swatch HEX code to copy it directly to your clipboard.

### ♿ Built-in Accessibility (WCAG AA)
- **Live Contrast Checker:** Automatically evaluates all 6 palette colors against pure white (`#FFFFFF`) and pure black (`#000000`).
- **Actionable Contrast Fixes:** Expand any `AA pass · why?` or `AA fail · why?` badge to inspect exact contrast ratios against the `4.5:1` standard. If a color fails, the tool suggests a passing alternative from your current palette (or black/white) and lets you swap it in with one click.

### ✒️ Typography & Live Preview
- **18 Curated Font Pairings:** Explore modern Google Fonts combinations (e.g., *Playfair Display + Source Sans 3*, *Space Grotesk + Work Sans*, *Fraunces + DM Sans*).
- **Lock & Iterate:** Like the heading font but want a different body font? Click **Keep** on one font and **Discard** on the other to cycle through alternatives independently.
- **Neutral Live Preview:** Test how your selected heading and body fonts look together in real time without color bias.

### ⭐ Favorites & Multi-Format Export
- **Browser Storage:** Save up to **5 color palettes** (with custom renaming) and **5 font pairings** locally via `localStorage`.
- **Developer Exports:**
  - **Copy CSS:** Copies ready-to-use `:root` CSS custom properties (`--color-1` through `--color-6`, `--font-heading`, `--font-body`).
  - **Export JSON:** Downloads the active palette and font pairing as `aesthetic-combination.json`.
- **Visual Favorites Export:** Opens a dedicated export window allowing you to select specific saved favorites and download them as a **PDF** (`aesthetic-favorites.pdf`) or high-resolution **JPEG** (`aesthetic-favorites.jpg`) mood board.

### 🌗 Theme & Responsiveness
- **Light & Dark Mode:** Switch seamlessly between a soft daylight aesthetic and a deep slate dark mode.
- **Mobile-Friendly:** Collapsible cards and responsive grids adapt smoothly to smaller screens, respecting `prefers-reduced-motion`.

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| **`Space`** | Shuffle palette and font pairing |
| **`S`** | Save current palette and font pairing to Favorites |
| **`C`** | Copy current palette and fonts as CSS variables |

*(Shortcuts are automatically disabled when typing in inputs or interacting with buttons/modals.)*

---

## 🚀 Getting Started

Because the entire application—HTML, CSS, SVG favicon, PDF generator, and canvas image extractor—is self-contained in `index.html`, no build tools, package managers, or backend servers are required.

1. **Clone or download** this repository.
2. **Open `index.html`** directly in any modern web browser (Chrome, Firefox, Safari, Edge).

> **Note:** An active internet connection is required to load font stylesheets from `fonts.googleapis.com`. All image processing, contrast calculations, and exports run 100% client-side.

---

## 🛠️ Technical Highlights

- **Zero External JS/CSS Dependencies:** Built purely with vanilla ES6+ JavaScript, modern CSS (`color-mix()`, CSS Grid, custom properties, native `<dialog>`), and semantic HTML5.
- **Client-Side Image Quantization:** Uses an HTML5 `<canvas>` downsampler and a custom median-cut algorithm to extract dominant colors without uploading user images to a server.
- **Dependency-Free PDF & JPEG Generation:** Generates valid PDF 1.4 documents (`Blob` byte streams) and renders high-DPI mood boards via `<canvas>` directly in the browser.

---

## 📄 License & Attribution

- **Fonts:** Loaded dynamically via [Google Fonts](https://fonts.google.com/) and subject to their respective open-source licenses.
- **Application Code:** Free to use, modify, and distribute.

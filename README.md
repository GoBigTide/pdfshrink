# PDF Shrinker

A privacy-first PDF tool that runs **entirely in your browser**.

- Reorder individual pages (drag & drop)
- Rotate pages (90° / 180° / 270°)
- Normalize every page to **US Letter** size
- Merge multiple PDFs
- Compress (optional)

Your files never leave the device. No server, no account, no tracking.

## Live use

Open `index.html` in a modern browser, or host on GitHub Pages / Netlify / any static host.

## Features

### Page editing
- Drop one or more PDFs
- See a thumbnail for every page
- Drag pages to put them in any order
- Rotate any page with the ↺ / ↻ buttons
- Remove individual pages
- Everything is forced to **US Letter** (8.5 × 11 in) and centered

### Export options
| Button | What it does |
|--------|----------------|
| **Merge only** | Lossless. Keeps original quality and selectable text. Pages are scaled & centered onto Letter. |
| **Compress** | Rasterizes each page (with your rotation + Letter size) as JPEG. Much smaller for scans and image-heavy PDFs. Text becomes non-selectable. |

### Compression presets
| Preset       | DPI | Notes                      |
|--------------|-----|----------------------------|
| High         | 300 | Print-quality / sharp text |
| Balanced     | 150 | Good screen + light print  |
| Small        | 100 | Solid size reduction       |
| Super Small  | 70  | Maximum shrink             |

## Deploy to GitHub Pages

1. Create a new repository
2. Upload the three files (`index.html`, `README.md`, `LICENSE`)
3. Go to **Settings → Pages**
4. Source → branch `main` + folder `/ (root)`
5. Live at `https://<username>.github.io/<repo>/`

## Tech

- Vanilla HTML / CSS / JS (no build step)
- [pdf.js](https://mozilla.github.io/pdf.js/) — rendering & thumbnails
- [pdf-lib](https://pdf-lib.js.org/) — merging, rotating, building the final PDF

## Limitations

- Very large documents (hundreds of pages or tens of MB) can be slow or memory-heavy
- Pure text/vector PDFs often don’t shrink much with the Compress path
- Compression turns text into images (no longer selectable/searchable)
- “Merge only” keeps text selectable

## Privacy

Everything runs locally in the browser tab. The only network requests are for the two open-source libraries from a public CDN. Your PDF data is never uploaded.

## License

MIT

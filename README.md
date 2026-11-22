# PDF Shrinker

A tiny, privacy-first PDF tool that runs **entirely in your browser**.

- Compress PDFs
- Merge multiple PDFs
- Reorder documents before merging (drag & drop)
- Merge + compress in one step

Your files never leave the device. No server, no account, no tracking.

## Live use

Just open `index.html` in a modern browser, or host it on GitHub Pages / Netlify / any static host.

## Features

### Compress
Renders each page to a canvas, encodes as JPEG at a chosen quality, and rebuilds the PDF.  
Works especially well on scans, photo-heavy documents, and large decks.

**Presets**

| Preset    | Approx. DPI | Best for               |
|-----------|-------------|------------------------|
| High      | ~150        | Readable text + images |
| Balanced  | ~120        | Good all-rounder       |
| Small     | ~96         | Maximum size reduction |

### Merge & Reorder
- Drop multiple PDFs
- Drag to reorder the documents
- **Merge only** → keeps original quality, text stays selectable
- **Merge & Compress** → combines then shrinks

## Deploy to GitHub Pages

1. Create a new repo (e.g. `pdf-shrinker`)
2. Upload / push the three files in this folder
3. Go to **Settings → Pages**
4. Set source to the branch containing `index.html` (usually `main`, folder `/`)
5. After a minute it will be live at  
   `https://<your-username>.github.io/<repo-name>/`

## Tech

- Vanilla HTML / CSS / JS (no build step)
- [pdf.js](https://mozilla.github.io/pdf.js/) — rendering pages
- [pdf-lib](https://pdf-lib.js.org/) — merging & building PDFs

## Limitations

- Very large files (>50–80 MB total) can be slow or run out of memory on low-end devices
- Pure text/vector PDFs may not shrink much (they’re already efficient) — sometimes they even get slightly bigger
- Compression mode makes text non-selectable (it becomes part of the page image)
- Merge-only mode keeps text selectable and original quality

## Privacy

Everything runs locally in the browser tab. The only network requests are for the two open-source libraries from a public CDN. Your PDF data is never sent anywhere.

## License

MIT

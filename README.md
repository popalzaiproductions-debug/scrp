# Scrp.

> Priced in minutes. Paid in full.

Landing page for Scrp — we buy fine watches, loose links and parts, old gold,
designer bags and luxury pens, in any condition, across the UAE.

**Live:** https://popalzaiproductions-debug.github.io/scrp/

## Structure

Single page, no build step, no dependencies beyond one Google font.

- `index.html` — the entire site. CSS is inline in the `<head>`.
- `images/` — the four section photographs.

Open `index.html` in a browser to work on it, or serve the folder:

```
python -m http.server
```

## Photography

All four slots are filled.

| Path | Subject | Size |
| --- | --- | --- |
| `images/hero.jpg` | Rolex Daytona dial on stone, grey ground | 990×1485 |
| `images/links.jpg` | Loose steel links and screw pins, overhead | 1200×1200 |
| `images/gold.jpg` | Rose gold AP bracelet on black leather | 798×1200 |
| `images/bags-pens.jpg` | Rolex ballpoint pen on its box | 1080×1080 |

Each `<img>` carries `onerror="this.remove()"`, so a missing or renamed file
falls back to a grey placeholder with its caption rather than a broken-image
icon. To swap a photo, replace the file at the same path — no HTML change.

All four are `object-fit: cover`, so the subject wants to sit near the centre;
edges crop away at narrow widths and the hero crops hard on mobile. Aim for
~1600–2400px on the long edge and keep each file under about 400KB.

> **Licensing:** the current photographs are dealer and listing images sourced
> from the web, and they carry other companies' trademarks. They work for
> previewing the design, but replace them with your own shoot or properly
> licensed images before this is promoted as a live business site.

## Before going live

- [ ] Replace the placeholder WhatsApp number `971500000000` (7 occurrences).
- [ ] Point the Instagram link at the real profile.
- [ ] Confirm `hello@scrp.ae` is receiving mail.
- [ ] Replace the photographs with owned or licensed images.

## Palette

| Token | Value | Use |
| --- | --- | --- |
| `--linen` | `#F5F1E8` | Main ground |
| `--shell` | `#EBE6D9` | Alternate sections |
| `--sage` | `#DCDCD0` | Empty photo slots |
| `--dark` | `#2B2A24` | Footer, "how it works" |
| `--ink` | `#1E1D18` | Text |
| `--grey` | `#6E6A5E` | Secondary text |
| `--gold` | `#A8842C` | Accent, focus rings |

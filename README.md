# Scrp.

> Priced in minutes. Paid in full.

Landing page for Scrp — we buy fine watches, loose links and parts, old gold,
designer bags and luxury pens, in any condition, across the UAE.

**Live:** https://popalzaiproductions-debug.github.io/scrp/

## Structure

Single page, no build step, no dependencies beyond one Google font.

- `index.html` — the entire site. CSS is inline in the `<head>`.
- `images/` — the four photographs the page calls for.

Open `index.html` in a browser to work on it, or serve the folder:

```
python -m http.server
```

## Photography

The page expects four images at these exact paths. Each `<img>` carries
`onerror="this.remove()"`, so a missing file falls back to a grey placeholder
with its caption rather than a broken-image icon — the page stays presentable
while slots are empty.

| Path | Subject | Orientation |
| --- | --- | --- |
| `images/hero.jpg` | Watch dial and bracelet macro, warm light | Portrait / tall |
| `images/links.jpg` | Loose bracelet links arranged on linen, overhead | Square-ish |
| `images/gold.jpg` | Coiled gold chains on dark stone, soft side light | Square-ish |
| `images/bags-pens.jpg` | Bag hardware and pen nib still life, muted tones | Square-ish |

All four are `object-fit: cover`, so the subject wants to sit near the centre —
edges get cropped at narrow widths. Aim for ~1600–2400px on the long edge and
keep each file under about 400KB.

## Before going live

- [ ] Replace the placeholder WhatsApp number `971500000000` (7 occurrences).
- [ ] Point the Instagram link at the real profile.
- [ ] Confirm `hello@scrp.ae` is receiving mail.
- [ ] Add the four photographs to `images/`.

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

# TDF Usage

Package guide for OpenDesign agents building Taiwan Digital Fest artifacts.

## Read Order

1. Read this file for the package contract.
2. Read `DESIGN.md` for the CIS rules, the 12-swatch palette, type pairing, grid language and hard prohibitions.
3. Paste the whole `:root` block from `tokens.css` into the first `<style>` of the artifact before writing any component CSS.
4. Load fonts: `Jersey 10`, `Space Grotesk`, `Noto Sans TC` from Google Fonts; `Cubic 11` from `fonts/Cubic_11.woff2` (package-local) — fall back to `Noto Sans TC 700` if the file cannot be embedded.
5. Reuse the recipes in `components.html` (nav short mark, Mondrian hero, buttons, place cards, event card, form, table, footer endorsement) before inventing new controls.
6. Open `preview/` pages for a visual sanity check of colors, type scale, grid rhythm and logo lockups.

## Design Highlights

- Visual style: Mondrian grid + pixel headings, carnival color blocks separated by black rules.
- Color stance: white / light-gray reading base, black structure, one dominant brand color per screen (yellow by default), pink / green / magenta / purple for rhythm.
- Type: English headings in Jersey 10 (pixel), 繁中 headings in Cubic 11 (pixel bold, line-height 1.45), body in Space Grotesk / Noto Sans TC.
- Three places are equal: `HUALIEN · TAITUNG · GREEN ISLAND` — same size, same weight, no ranking language.

## Do

- Keep every schema token name intact; add brand values only through the `--tdf-*` extensions.
- Separate color blocks with `--tdf-line` (5px) black rules on desktop and `--tdf-line-mobile` (3px) on phones.
- Use `--accent` (yellow) for the single primary action; secondary actions are white with a black border.
- Keep all visible text at 14px or larger; body 16–18px.
- Pair foreground and background per the AA table in `DESIGN.md` (black on yellow / cyan / pink / orange / green / gray / white; white on magenta / blue / ink / black).
- Use the official mark `assets/favicon.svg` unchanged; keep ¼-width clear space.

## Avoid

- No gradients, blur shadows, glass, rounded corners, glow or 3D effects — the radius tokens are 0 and `--elev-raised` is a ring on purpose.
- No new colors or tints beyond the 12 swatches (the derived `--muted` and `--border-soft` are the only functional exceptions).
- No pixel fonts for body copy, tables, QR codes, or wayfinding; no low-resolution "8-bit" filters.
- No Act I / II / III or 第一站 / 壓軸 hierarchy between Hualien, Taitung and Green Island.
- No hype copy ("world's biggest", "全球頂尖"); state dates, places, cost and limits plainly, English first.

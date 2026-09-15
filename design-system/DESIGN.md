---
name: "TDF 2027 — Taiwan Digital Fest"
category: Brands
surface: web
colors:
  background: "#FFFFFF"
  surface: "#F6F6F6"
  foreground: "#1E1F1C"
  muted: "#5B5C59"
  border: "#000000"
  accent: "#FFD028"
  accent-secondary: "#10B8D9"
  accent-tertiary: "#E74310"
  pink: "#F9D2E5"
  green: "#00993E"
  magenta: "#E4003D"
  purple: "#C54090"
  blue: "#004E9D"
---

# TDF 2027 — Taiwan Digital Fest Design System

> Category: Themed & Unique
> Surface: web, social, deck, print
> Owner: Taiwan Digital Nomad Association (TDNA) · CIS 1.0 (2026-09-01)
> A Mondrian-grid, pixel-headline festival system: white reading base, black structural rules, 12 fixed carnival swatches, hard edges, no gradients or shadows. Hosted by TDNA; Hualien · Taitung · Green Island are equal.

## Brand architecture and voice

- **TDNA** endorses; **Taiwan Digital Fest 2027 / TDF 2027** is the event brand every participant touches. The endorsement line is fixed: `HOSTED BY TAIWAN DIGITAL NOMAD ASSOCIATION · TDNA`, placed under the headline or in the footer at ≤25% of the headline height.
- Three places are **equal and parallel**: `HUALIEN · TAITUNG · GREEN ISLAND` / `花蓮 · 台東 · 綠島`. Never use Act I/II/III, 第一站/壓軸 or any ranking language; never bind one place permanently to one color.
- Fixed tagline, never rewritten: `Where digital nomads meet nature & innovation.` / `數位遊牧者，相遇於山海與創新。` Dates: `Apr 19 — May 31, 2027` / `2027 年 4 月 19 日至 5 月 31 日` (43 days).
- Voice: open, direct, culturally grounded, lively but ordered. English first for international material, Chinese second (≥75% of English body size). Say dates, places, cost and limits plainly. Use `community`, `live together`, `workation`, `local connection`; avoid `networking opportunity`, `exclusive lifestyle`, "world's biggest", "全球頂尖", stacked exclamation marks. CTAs are verbs: `Explore`, `Join`, `Apply`, `Buy tickets`.

## Color

Twelve official swatches. Print uses CMYK, screen uses HEX. Do not add tints, near-colors or gradients.

| Role | Name | HEX | Token | Text on it |
| --- | --- | --- | --- | --- |
| Primary | Yellow 亮黃 | `#FFD028` | `--tdf-yellow` / `--accent` | black |
| Primary | Cyan 青藍 | `#10B8D9` | `--tdf-cyan` | black |
| Primary | Orange 橘紅 | `#E74310` | `--tdf-orange` / `--warn` | black (white only for display sizes) |
| Accent | Pink 淺粉 | `#F9D2E5` | `--tdf-pink` / `--surface-warm` | black |
| Accent | Green 綠 | `#00993E` | `--tdf-green` / `--success` | black (white only for display sizes) |
| Accent | Magenta 桃紅 | `#E4003D` | `--tdf-magenta` / `--danger` | white |
| Accent | Purple 紫紅 | `#C54090` | `--tdf-purple` | black or white, one per component |
| Support | Blue 深藍 | `#004E9D` | `--tdf-blue` | white |
| Base | Gray 50 淺灰 | `#F6F6F6` | `--tdf-gray-50` / `--surface` | black |
| Base | Ink 深灰黑 | `#1E1F1C` | `--tdf-ink` / `--fg` | white |
| Base | White | `#FFFFFF` | `--tdf-white` / `--bg` | black |
| Structure | Black | `#000000` | `--tdf-black` / `--border` / `--fg-2` | white |

- White and light gray are the reading bases; black draws the grid; ink sets long copy.
- Yellow, cyan and orange carry the key visual and actions — **one dominant color per screen**. `--accent` is yellow by default; swap to cyan or orange for a whole screen, never mix three.
- Pink, green, magenta and purple create rhythm and sectioning; different colors must never imply a ranking of the three places.
- Blue is for calm information, headings on dark ground, or a dark block.
- One information component gets at most one solid fill and one text color.
- Contrast (WCAG AA, measured): black on yellow 14.3, cyan 8.9, pink 15.4, orange 5.2, green 5.6, gray 19.4; white on magenta 4.8, purple 4.7, blue 8.2, ink 16.6. Orange-white (4.0) and green-white (3.7) are display-size only. Ink must not sit as small text on orange, green, magenta, purple or blue.
- Derived functional exceptions: `--muted` (ink mixed 28% toward white, ≈7:1 on white) for captions and `--border-soft` (black at 15%) for inner row separators. Do not use them as fills.

## Typography

| Use | Face | Weight | Token |
| --- | --- | --- | --- |
| All English headings, year, short numbers | Jersey 10 (pixel) | 400 | `--font-display` |
| English UI and body | Space Grotesk | 400 / 500 / 700 | `--font-body` |
| All 繁中 headings | Cubic 11 (pixel) | 700 | `--tdf-font-display-zh` |
| 繁中 UI and body | Noto Sans TC | 400 / 500 / 700 | `--font-body` (fallback chain) |
| Code, kbd, tabular metrics | system monospace | — | `--font-mono` |

- Scale: `--text-4xl` 120px display (64–164 allowed, leading .82–.9) · `--text-3xl` 64px H1 · `--text-2xl` 44px section · `--text-xl` 28px H2–H6 · `--text-lg` 18px · `--text-base` 16px · `--text-sm` / `--text-xs` 14px. **Nothing visible below 14px** — labels, buttons, captions included.
- Headings: uppercase Jersey 10, `--leading-tight` .9, `--tracking-display` .02em. Chinese headings: Cubic 11 bold, line-height `--tdf-leading-display-zh` 1.45, letter-spacing `--tdf-tracking-display-zh` .08em; never let wrapped pixel lines overlap.
- Eyebrows: Space Grotesk 700, 14–16px, uppercase, tracking `--tdf-tracking-eyebrow` .2em.
- Body 16–18px, `--leading-body` 1.55–1.7, sentence case, normal punctuation.
- Bilingual hierarchy: English-first material makes Chinese the second line at ≥75% of English body size; Chinese-first material swaps the levels. The two languages never compete for the headline.
- Never set body copy, tables, QR codes or wayfinding in a pixel face; pixel character comes from the display faces and the integer grid, not from low-resolution rendering.

## Layout and grid language

- Base module `--tdf-module` 8px; align positions and sizes to whole modules.
- Structural rules are black: `--tdf-line` 5px on desktop and large output, `--tdf-line-mobile` 3px on phones and small sizes. Color blocks are separated by these rules — never by shadows, glass, gradients or rounded corners.
- Grids are **asymmetric Mondrian compositions** with a clear reading order: a dominant block, a supporting column, and small accent cells. Empty white is a legitimate block; do not decorate to fill space.
- Container `--container-max` 1440px; gutters 32 / 24 / 20px; section rhythm 96 / 64 / 48px.
- Three-place modules use equal cell size, type size and position weight; colors may differ per cell but rotate between materials.
- Mobile is a redesign, not a squeeze: stack blocks, keep the 3px rules, never scroll horizontally.

## Shape, elevation and imagery

- **Radius is 0 everywhere** (`--radius-*` = 0). Pills, avatars and badges are squares or rectangles with a black rule.
- **No blur shadows.** `--elev-ring` is a 1px black ring; `--elev-raised` is a 3px black ring for emphasized cards. `--elev-flat` is the default.
- Photography: real participants, co-working, local culture, nature and night-community documentary. Natural light, real skin tones, visible context, people interacting. No staged "laptop by the sea", no stock business shots, no HDR, no fake crowds. Crops keep hands, faces and key local elements; portraits require release.
- Pixel sheep (`assets/sheep-desk.webp`) is a community character for event moods, empty states and light motion — never a substitute for the mark, never in formal documents or dense tables. Pixel art renders with `image-rendering: pixelated` on a 1× grid.
- Icons: single-color linear SVG, uniform stroke, square terminals, placed in square cells with official swatches; always paired with a text label.
- Photos, QR codes and text stay high resolution; only illustrations are pixelated.

## Logo and lockups

- Official mark: `assets/favicon.svg`, an asymmetric pinwheel of black rules around yellow, cyan, magenta, blue and a white center — the smallest Mondrian/pixel module. Use the vector file only; never redraw, retrace or AI-regenerate it.
- Clear space: ¼ of the mark width on every side. Minimum size: 16px digital, 24px preferred in UI, 8mm print; wordmark ≥32mm; below 32px show the mark alone.
- Lockups: full wordmark `TAIWAN DIGITAL FEST` in Jersey 10 uppercase with `2027` at the same level or as its own color block; navigation short mark `TDF 2027` in Space Grotesk 700 with `TDF` optionally inside a yellow box with a black rule; endorsement `Hosted by TDNA` at ≤25% of headline height.
- Backgrounds: full color on white, light gray or a clean solid brand color; on photos add a full white or black plate first; monochrome processes use pure black or pure white versions only.
- Never stretch, rotate, skew, round, re-color, add gradients, shadows, outlines, glow, transparency or partner marks inside the mark.

## Components

- **Primary button:** `--accent` yellow fill, black text, 3px black border, 48px min height, Space Grotesk 700 16px. Hover inverts to black fill / white text (both change together); active shifts 2px down-right. One primary button per viewport.
- **Secondary button:** white fill, black text, 3px black border; hover moves the fill to `--surface`. **Text link:** black, underlined 2px, hover to `--accent` underline.
- **Nav bar:** white, bottom rule 5px, short mark left, uppercase 14px links; active link gets a yellow fill with black text.
- **Mondrian hero:** black-background grid with `--tdf-line` gaps; dominant yellow block holds the Jersey 10 headline, side cells hold mark, year and endorsement; a three-cell equal row lists the places.
- **Place card:** equal-size cells, Jersey 10 place name 28–34px, Space Grotesk 700 14px date line, one swatch per cell, bottom-aligned content.
- **Event card:** white cell, date block in `--tdf-blue` with white Jersey 10 day number, black rule separators, 14px meta row, one CTA.
- **Form field:** 14px bold label, 46px input with 3px black border, focus shows `--focus-ring` and a yellow underline; error uses `--danger` text and border, never color alone.
- **Badge / tag:** square-cornered, 14px uppercase, one swatch fill with correct text color, no pill.
- **Table:** 15–16px, header row black text on `--surface`, rows separated by `--border-soft`, tabular numbers in `--font-mono` where alignment matters.
- **Footer:** `--fg` ink background, white text, Jersey 10 title, endorsement line, partner logos separated by black rules or full white space in an independent logo wall.

## Motion and interaction states

- Durations: `--motion-fast` 180ms for hover and micro-states, `--motion-base` 220ms for state changes, 400ms max for large blocks; easing `--ease-standard` ease-out.
- Vocabulary: whole-cell slides, color-block flips, hard cuts. No bounce, float, particles, parallax or long loops.
- Hover is never the only feedback; every focusable element shows `--focus-ring` (3px white gap + 3px black ring). Text never turns gray on hover; hover moves the background or border instead.
- Respect `prefers-reduced-motion`: remove movement, parallax and autoplay.

## Applications and output specs

- OG image 1200×630 with ≥40px safe area (`assets/og-image.png` is the current master).
- Instagram portrait 1080×1350, headline in the central safe area; Story / Reels 1080×1920 with 250px UI safe zones top and bottom.
- Decks 16:9, one message per slide, 5px rules scaled proportionally; titles ≥36px, body ≥24px on 1920×1080.
- Print: CMYK, 300dpi, 3mm bleed, outlined text. Badges and tickets keep 4 QR modules of quiet zone and never tint the dark QR modules.
- Wayfinding: bilingual, high contrast, no Jersey 10 for critical direction text.
- Co-branding: TDF and partner marks separated by a black rule or full white space; TDF area ≥ largest partner mark when TDF hosts; partner logos used as supplied, never re-colored.

## Do's and don'ts

- **Do** pick one dominant brand color per screen and let black rules and white space do the rest.
- **Do** keep all text ≥14px and every fg/bg pair inside the AA table.
- **Do** show the three places at equal weight in every material.
- **Do** use real event photography and the official vector mark.
- **Don't** add gradients, blur shadows, glass, rounded corners, glow, transparency or 3D.
- **Don't** invent colors, tints, pixel filters, neon/cyberpunk or retro-game UI vocabulary.
- **Don't** set body copy, tables, QR codes or signage in pixel type.
- **Don't** put more than one solid primary button in a viewport, or make text lighter on hover.

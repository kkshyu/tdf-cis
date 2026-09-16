# TDF CIS

Taiwan Digital Fest brand identity site (evergreen; the year only marks the current edition) — https://cis.taiwandigitalfest.com

- `index.html` — CIS handbook, built on the OpenDesign token contract.
- `spec.html` / `spec/品牌色彩計畫.md` — canonical written specification.
- `design-system/` — OpenDesign package (`tokens.css`, `design-tokens.json`, `tailwind-v4.css`, `DESIGN.md`, `USAGE.md`, `components.html`, previews, fonts).

Static site served by nginx (`Dockerfile`), deployed on Railway from the `main` branch.
Source of truth for the package lives in `tdf/brand/design-system/tdf-2027`; copy it here when it changes.

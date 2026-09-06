# CLAUDE.md — KanoWorks

Guidance for Claude Code when working in this repository.

## What this is
A single-page marketing site for **KanoWorks** (kanoworks.io). The entire site is one
self-contained `index.html` — markup plus an inline `<style>` block, no separate
stylesheet, no build step, no framework, no bundler. Deployed via **GitHub Pages** on
push to `main` (repo: public `kanomelvin-prog/kanoworks`); the custom domain is set by
the root `CNAME` file.

## File structure
- `index.html` — the whole site, markup and CSS together (edit directly; there is no
  separate dev copy, and no separate `styles.css`)
- `CNAME` — custom domain for GitHub Pages; contains exactly `kanoworks.io`
- `docs/` — planning notes only; **not** linked from or served as site content
- No external JS libraries. System fonts or Google Fonts only.

## Visual Feedback Protocol
Follow this for every working session:
1. **Confirm a local preview URL at session start** before making changes
   (`python3 -m http.server` from the repo root).
2. **Plan before non-trivial changes** — state the approach, then build.
3. **Small commits, each producing a visible change** to the rendered page.
4. **Surface the rendered result after each commit** so changes can be eyeballed.

## Code standards
- Mobile-first, responsive.
- Accessible: semantic HTML, landmark elements, AA contrast (4.5:1), alt text on images.
- CSS custom properties for color/spacing — no scattered hardcoded values.
- Keep CSS in the single inline `<style>` block; do not reintroduce an external stylesheet.
- No `!important` unless truly unavoidable.
- Keep it fast: minimal fonts, no tracking scripts, no third-party embeds without approval.

## Brand basics
- Wordmark: **KanoWorks** — one word, camel case, no ™.
- Naming ruling 2026-09-06: KanoWorks one word everywhere — wordmark, domain, handles.
  'Kano Works' two-word form and 'Kano Studios' are retired. No second-tier parent brand
  (EM Studios rejected on collision check).
- Positioning: AI products, designed and built for the built world — by a civil-engineering
  insider (transportation, Civil 3D) who designs and ships real products.
- Voice: confident, plainspoken, maker/foundry. No hype, no invented clients or results.
- Contact address: `kano@kanoworks.io` (the only address shown on the site).

## Git
- Commit message format: a plain sentence-case subject describing what changed —
  no prefix or tag (e.g. `Fix LinkedIn link`).
- Push to `main` triggers the GitHub Pages deploy.

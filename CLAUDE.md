# CLAUDE.md — Kano Works

Guidance for Claude Code when working in this repository.

## What this is
A single-page marketing site for **Kano Works** (kanoworks.io). Static HTML/CSS/JS,
no build step, no framework, no bundler. Deployed via **Cloudflare Pages** on push to
`main` (repo: private `kanomelvin-prog/kanoworks`).

## File structure
- `index.html` — the site (edit directly; there is no separate dev copy)
- `styles.css` — stylesheet
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
- No `!important` unless truly unavoidable.
- Keep it fast: minimal fonts, no tracking scripts, no third-party embeds without approval.

## Brand basics
- Wordmark: **Kano Works™** (the ™ appears on the wordmark only, nowhere else).
- Positioning: AI products, designed and built for the built world — by a civil-engineering
  insider (transportation, Civil 3D) who designs and ships real products.
- Voice: confident, plainspoken, maker/foundry. No hype, no invented clients or results.

## Git
- Commit message format: `chat: [what changed]`
- Push to `main` triggers the Cloudflare Pages deploy.

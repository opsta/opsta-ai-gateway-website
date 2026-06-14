# Opsta AI Gateway — marketing website

Public landing page for **Opsta AI Gateway**, live at **https://ai-gateway.opsta.co.th**.

## Stack
- Plain **HTML + CSS + vanilla JS** — no build step, no dependencies.
- Single page: [`public/index.html`](public/index.html).
- Fonts: Montserrat (EN) + IBM Plex Sans Thai (TH) via Google Fonts.
- Brand: navy `#111F35`, blue `#008BEA` (Opsta brand palette + the Opsta mark).
- Bilingual **EN / ไทย** via a vanilla-JS toggle (`data-en` / `data-th` attributes; choice persisted in `localStorage`).

## Deployment
- **GitHub Pages** via [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) — publishes `public/` on every push to `main`.
- Custom domain: `public/CNAME` → `ai-gateway.opsta.co.th`. DNS is a `CNAME` record `ai-gateway` → `opsta.github.io` on the `opsta.co.th` Cloudflare zone (DNS-only so GitHub Pages can provision HTTPS).

## Editing
- All copy lives inline in `public/index.html` as `data-en` / `data-th` attribute pairs on each element.
- To change a string, edit both the visible text and its `data-en` (and `data-th`) attribute.

## Done
- Thai copy — native, English-loanword wording (per the approved Opsta dictionary).
- Social card — on-brand 1200×630 OG image at `public/assets/og-image.png`, wired into `og:image` / `twitter:image`.
- Nav anchor links wired to section IDs (`#why`, `#capabilities`, `#how`, `#security`) with smooth scroll.

## Possible future tweaks
- Regenerate the OG card if the headline/brand changes (source: a standalone 1200×630 HTML rendered via headless Chrome).
- Add more sections (pricing, customer logos, case studies) as the story grows.

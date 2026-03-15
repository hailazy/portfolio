# Architecture

## System Overview

Single-page static site. Zero JS shipped to browser. All content hardcoded in Astro components — no CMS, no database, no API calls. Deployed to Cloudflare Pages CDN.

**Architecture Style**: Static Site (pure SSG, no Astro Islands used)

## Project Structure

```
portfolio/
├── src/
│   ├── components/        — Section components (Hero, Services, Work, About, Contact, Nav, Footer)
│   ├── layouts/           — BaseLayout.astro (wraps all pages)
│   ├── pages/             — index.astro (single page)
│   └── styles/            — global.css (design tokens, reset, typography)
├── public/                — Static assets
├── dist/                  — Build output (gitignored)
├── wrangler.jsonc         — Cloudflare Pages config
└── astro.config.mjs       — Astro config (output: static, CF adapter)
```

## Component Map

```
index.astro
  └── BaseLayout
        ├── Nav
        ├── Hero
        ├── Services
        ├── Work
        ├── About
        ├── Contact
        └── Footer
```

## Data Flow

```
pnpm build
    ↓
Astro compiler (SSG)
    ↓
dist/ (HTML + CSS + assets)
    ↓
git push master
    ↓
Cloudflare Pages CDN
    ↓
Browser (zero JS)
```

## Content Strategy

- **Current**: All content hardcoded in components (intentional — simple, fast)
- **Future**: Astro content collections for blog/devlog (deferred to Phase 0 Week 2+)
- **Content pipeline**: `digital-identity/derived/public-bio.md` → `src/content/` (deferred)

## Design Decisions

- **No JS framework** — pure `.astro` components, no React/Vue/Svelte
- **No CMS** — avoids complexity for a simple profile site
- **No build-time data fetching** — content is static text, no API at build time
- **Single page** — all sections on `index.astro`, smooth scroll navigation

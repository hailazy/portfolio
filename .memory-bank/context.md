# Current Context

> **Last Updated**: 2026-03-15
> **Updated By**: Claude (deploy setup session)

## Recent Changes (Last 30 Days)

- **2026-03-15** `feat`: Init Astro portfolio (Cloudflare Pages)
  - Files: `astro.config.mjs`, `wrangler.jsonc`, `src/` scaffold
  - Impact: Project bootstrapped with Cloudflare adapter, `output: static`

- **2026-03-15** `feat`: Add portfolio content (hero, services, work, about, contact)
  - Files: `src/components/Hero.astro`, `Services.astro`, `Work.astro`, `About.astro`, `Contact.astro`, `src/styles/global.css`
  - Impact: Full single-page site live — dark theme, Inter + JetBrains Mono, all five sections

- **2026-03-15** `refactor`: Trim About bio to professional minimum
  - Files: `src/components/About.astro`
  - Impact: Removed personal backstory, kept positioning only

- **2026-03-15** `feat`: Add canonical site URL for haingt.dev
  - Files: `astro.config.mjs` — added `site: 'https://haingt.dev'`
  - Impact: Canonical `<link>` tags, future sitemap, OG URLs now use correct domain

## Context Carry-Forward

**In Progress**:
- CF Pages project not yet created — user needs to do dashboard steps (Workers & Pages → Create → Pages → connect GitHub repo, build: `pnpm build` / `dist`, env: `NODE_VERSION=22`)
- After CF Pages created: add `git remote add origin <url>` then `git push -u origin master`
- Custom domain: add `haingt.dev` in Pages Settings → Custom Domains (CF auto-creates CNAME, ~1-2min SSL)

**Immediate blocker**:
- `Contact.astro` has a placeholder Upwork URL — needs real URL once Upwork profile is created

**For Next Session**:
- Create Upwork profile → update URL in `Contact.astro`
- Create CF Pages project (dashboard) + push code to GitHub remote
- Consider blog/devlog section (Astro content collections, Phase 0 Week 2+)

## Known Issues & Workarounds

- **Issue**: Upwork URL in `Contact.astro` is a placeholder
  - **Workaround**: None — URL goes nowhere until profile exists
  - **Fix**: Create Upwork profile, paste real URL

## Key Files

- `src/components/Contact.astro` — Contains placeholder Upwork URL (needs update)
- `src/components/Services.astro` — Pricing / service descriptions
- `src/components/Work.astro` — Case studies / past work
- `src/styles/global.css` — Design tokens (colors, fonts, spacing)
- `astro.config.mjs` — Framework config (adapter, output mode)
- `wrangler.jsonc` — Cloudflare Pages config (project name, compat date)

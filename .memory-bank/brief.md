# Project Brief

## Goal
Public portfolio site for Upwork/client discovery — showcasing Hải's backend dev + AI automation expertise.

## Scope
**In Scope:**
- Public-facing profile: skills, projects, contact
- Deployed via Cloudflare Pages (public repo, auto-deploy on push)
- Content source: manual sync from `digital-identity/derived/public-bio.md` (public tier only)

**Out of Scope:**
- Private profile data — digital-identity is the data source, portfolio only consumes public tier
- CMS or dynamic content — static site only for now
- Blog (deferred — possible future addition)

## Stack
- **Framework**: Astro (minimal template, strict TypeScript)
- **Adapter**: @astrojs/cloudflare — `output: 'static'`
- **Deploy**: Cloudflare Pages (public repo required)
- **Package manager**: pnpm

## Content Pipeline (deferred)
- `digital-identity/scripts/derive.sh` → `derived/public-bio.md` (public tier only)
- Future: copy script syncs into `portfolio/src/content/`

## Status
- **Created**: 2026-03-15
- **Status**: Bootstrapped — skeleton Astro site, Cloudflare adapter configured

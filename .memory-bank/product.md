# Product Context

## Problem Statement

**The Problem**: Independent freelancers need credibility signals before clients trust them. Without a portfolio, Upwork profiles look thin; without a live site, website service pitches feel hollow.

**Current State**: No public portfolio existed. Upwork profile not yet created. Both gaps block Phase 0 income.

**Desired State**: Portfolio live + Upwork profile linked → credibility loop closes → first client inquiry possible.

## Two Jobs (Dual Purpose)

This site does two jobs simultaneously:

### Job 1 — Upwork Credibility
- **Audience**: English-speaking Upwork clients evaluating AI Integration / Automation freelancers
- **Evaluation criteria**: Positioning clarity, past work relevance, contact accessibility
- **Success**: Client clicks "Contact" or reaches out via Upwork

### Job 2 — Website Service Demo
- **Audience**: Local VN businesses evaluating website services
- **Evaluation criteria**: The site itself — speed, design, mobile, professionalism
- **Success**: Client says "I want something like this"
- **The pitch**: "This site is built with the same stack I'd build yours on"

## Known Issues

| Issue | Location | Status |
|-------|----------|--------|
| Upwork URL is placeholder | `src/components/Contact.astro` | Blocked — Upwork profile not created yet |

## Roadmap

1. **Now**: Replace Upwork URL placeholder once profile is created
2. **Phase 0 Week 2+**: Blog/devlog section (Astro content collections)
3. **Later**: Content pipeline — `digital-identity/derived/public-bio.md` → `src/content/`

## Constraints

- **Static only** — no server runtime, no database (by design)
- **Public repo** — required for Cloudflare Pages free tier auto-deploy
- **No secrets** — nothing sensitive can live in this repo

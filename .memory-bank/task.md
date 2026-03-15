# Active Tasks

> **Last Updated**: 2026-03-15
> **Updated By**: Claude (deploy setup session)

## Current Sprint/Focus

**Goal**: Portfolio live + Upwork profile ready for first client inquiry
**Deadline**: Before Sa arrives (April 2026)
**Progress**: ~70% — code ready to ship, CF Pages project not yet created

## Active Workstreams

1. **Cloudflare Pages Deploy**
   - **Status**: In Progress (code done, dashboard pending)
   - **Priority**: High
   - **Next Action**: Create CF Pages project in dashboard → connect GitHub repo → push code
   - **Steps remaining**: Dashboard setup + `git remote add` + push + custom domain `haingt.dev`

2. **Upwork Profile Setup**
   - **Status**: Blocked
   - **Priority**: High
   - **Blockers**: Not started — need to create profile, write bio, select skills, set rate
   - **Next Action**: Create Upwork account, write profile, get profile approved
   - **Dependency**: Unblocks Contact.astro URL fix

2. **Contact.astro URL Fix**
   - **Status**: Blocked (waiting on Upwork)
   - **Priority**: High
   - **Blockers**: Upwork profile doesn't exist yet
   - **Next Action**: Once Upwork profile URL known, update `src/components/Contact.astro`

3. **Blog / Devlog Section**
   - **Status**: Deferred
   - **Priority**: Low
   - **Next Action**: Phase 0 Week 2+ — implement Astro content collections
   - **Notes**: Will use `digital-identity/derived/public-bio.md` pipeline eventually

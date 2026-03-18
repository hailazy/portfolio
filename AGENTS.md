# Portfolio — haingt.dev

## Project Overview

Single-page portfolio for Nguyen Thanh Hai — backend developer + indie game dev ecosystem builder.
Deployed via Cloudflare Pages (static site, auto-deploy on push to master).

**Stack:** Astro 6 (static output), TypeScript strict, vanilla CSS, no JS framework.

## File Structure

```
src/
├── components/
│   ├── Nav.astro          # Sticky nav, glass-morphism backdrop
│   ├── Hero.astro         # Full viewport hero, entrance animations
│   ├── Work.astro         # Current projects + past work with metrics
│   ├── Services.astro     # Service offerings with SVG icons
│   ├── About.astro        # Bio + skills grid
│   ├── Contact.astro      # CTA + social links
│   └── Footer.astro       # Simple footer (do not modify)
├── layouts/
│   └── BaseLayout.astro   # HTML shell, fonts, global styles, scripts
├── pages/
│   └── index.astro        # Page composition (all sections)
└── styles/
    └── global.css         # Design tokens, reset, utilities, components
```

## Design System

### Color Tokens (Electric Blue accent)

```css
--color-bg:              #0d0d0f;
--color-surface:         #16161a;
--color-border:          #2a2a35;
--color-text:            #e8e8ec;
--color-muted:           #8888a0;
--color-accent:          #3b82f6;
--color-accent-dim:      #2563eb;
--color-accent-glow:     rgba(59, 130, 246, 0.15);
--color-accent-gradient: linear-gradient(135deg, #2563eb 0%, #3b82f6 50%, #60a5fa 100%);
--color-surface-hover:   #1c1c22;
--shadow-glow:           0 0 20px rgba(59, 130, 246, 0.08);
--shadow-card:           0 2px 8px rgba(0, 0, 0, 0.3);
```

### Typography

- **Sans:** Inter (400, 500, 600, 700)
- **Mono:** JetBrains Mono (400, 500)
- Loaded from Google Fonts in BaseLayout.astro

### Spacing & Layout

- `--radius: 8px`
- `--max-w: 1100px`
- `--gap: clamp(1rem, 4vw, 2.5rem)`
- All sections use `.container` for max-width centering

### Component Patterns

- **Cards**: `.card` — surface bg, border, radius, flex column. Hover: border-color + glow + lift.
- **Tags**: `.tag` — mono font, uppercase, surface bg, border pill.
- **Buttons**: `.btn` + `.btn-primary` or `.btn-ghost`.
- **Section dividers**: `<hr class="section-divider">` — gradient fade center.
- **Scroll reveal**: `.reveal` class on elements — fades up on scroll via IntersectionObserver.

### Gradient Usage

- **Gradient text** (background-clip): hero h1 accent, metric numbers
- **Flat accent** (#3b82f6): buttons, links, overlines, tag hover, nav active indicator
- **Glow** (accent-glow): card hover backgrounds
- **Section divider**: gradient at center, transparent at edges

## Hard Constraints

- **No Tailwind** — vanilla CSS only, scoped `<style>` per component
- **No JS frameworks** — vanilla JS only, IntersectionObserver + scroll listeners
- **No SSR** — static output only (`output: 'static'` in astro.config.mjs)
- **Dark theme stays** — no light mode toggle
- **Content stays** — do not change text, project data, or descriptions
- **`prefers-reduced-motion`** — all animations must be disabled when user prefers reduced motion
- **Mobile-first** — test at 375px, 768px, 1024px, 1440px

## Quality Gates

1. `npm run build` must pass with no errors
2. Lighthouse Performance > 95
3. Lighthouse Accessibility > 90
4. No horizontal overflow at 375px
5. All interactive elements have focus-visible states
6. `prefers-reduced-motion: reduce` disables all animations and transitions

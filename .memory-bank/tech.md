# Tech Stack

## Core Technologies

### Language & Runtime
- **Primary Language**: TypeScript (strict mode)
- **Runtime**: Node.js >=22.12.0
- **Package Manager**: pnpm

### Framework
- **Main Framework**: Astro 6.0.4
- **Output Mode**: `static` (zero server runtime)
- **Why**: Sub-second loads, zero JS to browser by default, free Cloudflare Pages tier

## Key Dependencies

### Production
| Dependency | Version | Purpose |
|------------|---------|---------|
| astro | 6.0.4 | Static site framework |
| @astrojs/cloudflare | 13.1.1 | Cloudflare Pages adapter |

### Development
| Dependency | Version | Purpose |
|------------|---------|---------|
| wrangler | 4.73.0 | Cloudflare CLI (local preview + deploy) |
| typescript | bundled | Type checking |

## Development Commands

```bash
pnpm dev        # Local dev server
pnpm build      # Production build → dist/
pnpm preview    # Preview built site via wrangler
```

## Design System

- **Fonts**: Inter (body), JetBrains Mono (code/accent)
- **Theme**: Dark, CSS custom properties
- **Tokens defined in**: `src/styles/global.css`
- **No CSS framework** — hand-rolled, minimal

## Deploy

- **Platform**: Cloudflare Pages
- **Trigger**: Push to `master` branch → auto-deploy
- **Config**: `wrangler.jsonc` (project name, compatibility date)
- **Build output**: `dist/`

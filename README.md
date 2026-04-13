# STIM Canada

Landing page for STIM Canada — Tier-1 electronics manufacturing: PCBA, Box-Build, NPI/Prototyping, and Supply Chain Solutions.

**Live site:** [stimcanada.com](https://stimcanada.com)

## Quick Start

```bash
bun install
bun run dev       # http://localhost:4321
bun run build     # production build → dist/
bun run preview   # preview production build
```

Requires [Bun](https://bun.sh).

## Project Structure

```
src/
├── components/Nav.astro              # Glassmorphism navigation bar
├── components/sections/              # Landing page sections
│   ├── Hero.astro                    #   Hero with background image + CTA
│   ├── Services.astro                #   Three-column service cards
│   ├── ValueAdded.astro              #   Icon grid of value-added services
│   ├── Testimonial.astro             #   Parallax quote section
│   ├── Markets.astro                 #   Four-column market images
│   ├── Quality.astro                 #   ISO certifications + partner logos
│   ├── CTA.astro                     #   Contact call-to-action banner
│   ├── Values.astro                  #   Brand values strip
│   ├── STIMSense.astro               #   STIM Sense feature section
│   ├── News.astro                    #   Latest news cards
│   └── Footer.astro                  #   Site footer
├── layouts/BaseLayout.astro          # HTML shell, meta, fonts
├── pages/index.astro                 # Assembles all sections
├── scripts/animations.ts             # GSAP parallax & scroll reveals
└── styles/global.css                 # Design tokens + Tailwind import

public/
├── icons/favicon.svg
├── images/
│   ├── hero/                          # Hero backgrounds
│   ├── markets/                        # Market section images
│   ├── news/                           # News card images
│   └── sections/                       # CTA, testimonial, feature images
├── logos/                              # Brand + partner logos
└── robots.txt
```

## Design System

See [DESIGN.md](./DESIGN.md) for the full design system. Key tokens:

| Token | Value | Usage |
|---|---|---|
| Primary | `#006a63` | Brand teal, CTAs |
| Primary Container | `#35bdb2` | Accent, gradients |
| On Surface | `#191c1d` | Body text (no `#000`) |
| Surface | `#f8f9fa` | Page background |
| Surface Container Low | `#f3f4f5` | Alternate sections |

- Fonts: **Manrope** (headlines) + **Inter** (body)
- Headline letter-spacing: `-0.02em`
- Max border-radius: `8px`
- Gradient CTAs: `#006a63 → #35bdb2` at 135deg
- Glassmorphism nav: `white/80` + `20px backdrop-blur`

## Agent Pointers

- **Design tokens** → `src/styles/global.css` (`@theme` block)
- **All sections** → `src/components/sections/`
- **Animations** → `src/scripts/animations.ts` (GSAP)
- **Page assembly** → `src/pages/index.astro`
- **Layout** → `src/layouts/BaseLayout.astro`
- **Assets** → `public/images/` (WebP), `public/logos/` (SVG/WebP)
- **Design spec** → `DESIGN.md` at project root

## Deploy

Push to `master` — GitHub Actions builds and deploys to GitHub Pages automatically via `.github/workflows/deploy.yml`.
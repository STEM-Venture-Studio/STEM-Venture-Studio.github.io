# STIM Canada Landing Page

## Project
Landing page for STIM Canada (stimcanada.com) — Tier-1 electronics manufacturing: PCBA, Box-Build, NPI/Prototyping, Supply Chain Solutions.

## Tech Stack
- **Runtime/PM**: Bun (source ~/.bashrc or set PATH=$HOME/.bun/bin:$PATH)
- **Framework**: Astro 6
- **CSS**: Tailwind CSS 4 via @tailwindcss/vite
- **Interactive**: Svelte 5 via @astrojs/svelte (use ONLY for client-side interactivity)
- **Animations**: GSAP + ScrollTrigger (src/scripts/animations.ts)
- **Deploy**: GitHub Pages via withastro/action@v5

## Commands (use bun, not npm)
- `bun run dev` — Start dev server (localhost:4321)
- `bun run build` — Production build to dist/
- `bun run preview` — Preview production build
- `bun add <pkg>` — Add dependency

## Architecture
- `src/pages/` — File-based routing (index.astro = landing page)
- `src/layouts/BaseLayout.astro` — HTML shell with meta tags, view transitions, font loading
- `src/components/sections/` — Landing page sections (Hero, Services, ValueAdded, Markets, Quality, CTA, News, Footer)
- `src/components/` — Reusable UI components (Nav.astro)
- `src/styles/global.css` — Design tokens (@theme block) + Tailwind import
- `src/scripts/animations.ts` — GSAP parallax/scroll utilities
- `public/` — Static assets (favicon, images, SVGs)
- `public/content/` — Optimized WebP images and SVG logos

## Design System
See design/DESIGN.md for complete design guidelines.
Key rules:
- Manrope (headlines) + Inter (body/labels), tight letter-spacing on headlines (-0.02em)
- Primary teal #006a63, Primary container #35bdb2
- Surface hierarchy: white cards on #f3f4f5 on #f8f9fa
- No 1px borders for sectioning — use background shifts only
- Max border-radius 8px (industrial feel)
- No #000000 — use #191c1d for text
- Gradient CTAs: primary to primary-container at 135deg
- Glassmorphism nav: white/80 with 20px backdrop-blur
- Material Symbols Outlined icons for value-added services

## Assets
- Logo: `/svg/logo.svg` (square, original), `/svg/logo-rectangle.svg` (cropped, for nav/header)
- Content images: `/content/*.webp` — optimized WebP, max 2400px, max 2MB
- NSO logos: `/content/Logo_IPCMember.svg`, `/content/Logo_SMTA.svg`
- ISO logos: `/content/Logo_ISO_9001_2015_black_TM.webp`, `/content/Logo_ISO_13485_2016_black_TM.webp`

## Svelte Usage Rules
- Only use .svelte for components needing CLIENT-SIDE interactivity
- Use client:visible for below-fold interactive components
- Use client:load only for above-fold critical interactivity
- Most components should be .astro (zero JS shipped)
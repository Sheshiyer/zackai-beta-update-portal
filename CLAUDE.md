# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

ZackAI Beta Update Portal — an Astro 4 static site serving as a brand launch portal and documentation wiki for ZackAI (screen-free AI plush companion for children ages 3-8). Bilingual (English + French). Deployed on Vercel.

Live site: https://zackai-beta-update-portal.vercel.app

## Commands

All commands run from `wiki-site/` directory using Bun:

```bash
cd wiki-site
bun install          # Install dependencies
bun run dev          # Dev server with hot reload
bun run build        # Static production build (outputs to wiki-site/dist/)
bun run preview      # Preview production build locally
```

No test or lint commands are configured.

## Architecture

**Framework:** Astro 4 with MDX integration, TypeScript strict mode, pure CSS (no framework). Zero client-side JS frameworks — only inline scripts for theme toggle and TOC observer.

**Key directories:**
- `wiki-site/src/` — Main application source
- `wiki-site/src/pages/` — File-based routing with `[locale]` dynamic segments
- `wiki-site/src/content/docs/` — English markdown docs (Content Collections)
- `wiki-site/src/content/frDocs/` — French markdown docs
- `wiki-site/src/components/` — Astro components (no React/Vue/Svelte)
- `wiki-site/src/styles/global.css` — Single monolithic CSS file with design token system
- `wiki-site/src/i18n/index.ts` — Type-safe i18n utilities and translation strings
- `wiki-site/src/data/site-data.json` — Centralized brand metadata, nav config, featured content
- `wiki-site/public/` — Static assets (images, NotebookLM research artifacts)
- `src/components/Icon.astro` — 25+ inline SVG icon system (root level, not wiki-site)
- `brand-config.yaml` — Brand DNA reference (not used at runtime)
- `wiki-output/` / `wiki-output-fr/` — Generated markdown source (provenance)

**Routing pattern:**
- `/` redirects to `/en/`
- `/[locale]/` — Localized homepage
- `/[locale]/docs/[...slug]` — Doc pages
- `/docs/[...slug]` — Legacy redirect to `/en/docs/`

**Content Collections:** Two collections (`docs` and `frDocs`) defined in `src/content/config.ts` with Zod schema: `title` (required), `description`, `category`, `order`, `icon`. French docs fall back to English when missing.

**i18n strategy:** Route-based locale (`/en/`, `/fr/`). Translation strings live in `src/i18n/index.ts` as a typed nested object. Key functions: `localizedPath()`, `switchLocalePath()`, `t()`, `localizedDocTitle()`.

## Design System

All design tokens in `wiki-site/src/styles/global.css` via CSS custom properties:

- **Brand colors:** `--brand-primary` (#AA98D6 Lilac), `--brand-accent` (#E67A2E Orange), `--brand-signal` (#4CC8B2 Teal), `--brand-secondary` (#F8F6F2 Cloud White)
- **Typography:** Figtree (display), Inter (body), JetBrains Mono (code) — loaded via Google Fonts in BaseLayout
- **Theme:** Light (default) / Dark via `data-theme` attribute on `<html>`, persisted to localStorage
- **Glass morphism:** `backdrop-filter: blur(24px)` + semi-transparent backgrounds using `color-mix()`
- **Spacing:** 8-step modular scale (`--space-1` through `--space-9`)
- **Radius:** 6-step scale (`--radius-xs` 10px through `--radius-pill` 999px)
- **Responsive breakpoints:** 1180px (sidebar collapses) and 820px (single column)

## Important Conventions

- **Bun only** — package manager is Bun, lockfile is `bun.lock`
- **Git LFS** — Binary assets (mp3, pdf, png, jpg, webp, mp4, wav) tracked via LFS
- **Static-only** — No SSR, everything pre-rendered at build time
- **No external JS deps** — Theme toggle and TOC use inline `<script>` tags
- **Component naming:** PascalCase `.astro` files, BEM-like CSS classes (`.glass-card--interactive`)
- **Doc categories ordered:** general → product → brand → audience → marketing
- **Icon additions:** Add new SVG paths to `src/components/Icon.astro` icon map
- **Adding docs:** Create `.md` file in `wiki-site/src/content/docs/[category]/` with proper frontmatter. For French, mirror in `frDocs/` and add translation entries in `i18n/index.ts`

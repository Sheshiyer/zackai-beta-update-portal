# ZackAI Beta Update Portal

A bilingual (EN/FR) brand launch wiki for **ZackAI** — a screen-free AI plush companion for children aged 3–8.

Built with [Astro 4](https://astro.build) and deployed on [Vercel](https://vercel.com).

## Live Site

**https://zackai-beta-update-portal.vercel.app**

## Stack

| Layer | Technology |
|-------|-----------|
| Framework | Astro 4.16 (static output) |
| Content | Markdown + Content Collections |
| Styling | Custom CSS with design tokens |
| Icons | Custom SVG icon system (`Icon.astro`) |
| Media | HTML5 audio players, iframe PDF embeds, inline data tables |
| i18n | English + French with locale routing |
| Hosting | Vercel (static) |

## Project Structure

```
├── public/
│   ├── images/          # Brand visuals, product shots
│   └── notebooklm/     # Audio briefings, PDF decks, CSVs, infographics
├── src/
│   ├── components/      # Astro components (Icon, Navigation, PortalHome, etc.)
│   ├── content/
│   │   ├── docs/        # English content (20 pages)
│   │   └── frDocs/      # French content (10 pages)
│   ├── data/            # site-data.json (navigation, featured docs)
│   ├── i18n/            # Translation strings
│   ├── layouts/         # BaseLayout, DocLayout
│   ├── pages/           # Route definitions with [locale] param
│   └── styles/          # global.css with design token system
├── astro.config.mjs
└── package.json
```

## Content Sections

- **Getting Started** — Quick-start guide
- **Product** — Overview, features, technical specifications
- **Brand** — Visual guidelines, voice & tone, asset library
- **Audience** — Primary persona (parents), secondary personas
- **Marketing** — Campaign copy, email templates, social content, ad creative, video scripts
- **Market** — Competitive landscape analysis
- **Research** — NotebookLM artifacts (audio briefings, presentation decks, data tables, infographics, reports)

## Development

```bash
npm install
npm run dev       # Start dev server
npm run build     # Build for production
npm run preview   # Preview production build
```

## Design System

- **Fonts**: Figtree (display), Inter (body), JetBrains Mono (code)
- **Brand colors**: Lilac `#AA98D6`, Orange `#E67A2E`, Teal `#4CC8B2`
- **Themes**: Light and dark mode via `[data-theme]` toggle
- **Icons**: 22 custom SVG stroke icons via `Icon.astro` component

## License

Proprietary — HeyZack / ZackAI. All rights reserved.

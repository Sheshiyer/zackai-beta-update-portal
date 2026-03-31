---
name: "competitor-alternatives"
description: "ZackAI project wrapper for competitor-alternatives. Use it for comparison pages and battle-card style content, but always ground the work in the current competitive and product markdown first."
metadata:
  version: "1.1.0-zackai.1"
  basedOn: "global/competitor-alternatives@1.1.0"
---

# competitor-alternatives — ZackAI Wrapper

This project-level skill keeps the original `competitor-alternatives` purpose, but adds ZackAI-specific reuse-first behavior.

## Core Goal

Create competitor comparison, alternative-page, or battle-card style content that is honest, useful, and grounded in current ZackAI product and market docs before any new page is drafted.

## Required Read-First Workflow

Before drafting or asking broad discovery questions, read:
- .agents/product-marketing-context.md
- src/content/docs/market/competitive-landscape.md
- src/content/docs/product/features.md
- src/content/docs/product/overview.md
- src/content/docs/product/specifications.md
- src/content/docs/marketing/campaign-copy.md

## ZackAI Source-of-Truth Rules

Canonical inputs, in order:
1. `.agents/product-marketing-context.md`
2. `README.md`
3. `src/content/docs/**`
4. `src/content/frDocs/**` for French or bilingual work

Never use `wiki-output/**`, `wiki-output-fr/**`, or `wiki-site/**` as the primary source for regeneration, rewriting, or claim harvesting.

## Reuse-First Rules

- Treat `src/content/docs/market/competitive-landscape.md` as the base comparison source and extend it before spinning up separate competitor notes elsewhere.
- Keep comparisons tied to documented ZackAI claims, differentiators, objections, and limits already present in repo markdown.
- If a new comparison page is needed, place it under the canonical root docs tree and explicitly link it back to the competitive-landscape source rather than creating detached notes.
- Never invent competitor pricing, features, support claims, or ZackAI proof that has not been verified.
- Be explicit about research gaps instead of filling them with marketing language.

## ZackAI-Specific Guidance

- Be honest about who ZackAI is best for and where an alternative may still be a better fit.
- Explain why differences matter for parents and households, not just as a feature checklist.
- Prioritize screen-free interaction, multilingual capability, emotional warmth, trust/safety, and no-subscription value because those are the strongest documented axes in this repo.
- If the request is SEO-driven, recommend the minimal new comparison pages needed and avoid redundant variants that restate the same narrative.
- If localized output is requested, review matching French market/product docs before translating.

## Output Expectations

When responding:
1. Name the repo files you used.
2. Separate what can be extended inside `src/content/docs/market/competitive-landscape.md` from what genuinely requires a new comparison asset.
3. Clearly distinguish documented facts from fresh research needs.

---
name: "sales-enablement"
description: "ZackAI project wrapper for sales-enablement. Use it to create sales collateral and objection handling, but always build from ZackAI\u2019s canonical messaging and adapt the motion to the actual business context instead of default SaaS assumptions."
metadata:
  version: "1.1.0-zackai.1"
  basedOn: "global/sales-enablement@1.1.0"
---

# sales-enablement — ZackAI Wrapper

This project-level skill keeps the original `sales-enablement` purpose, but adds ZackAI-specific reuse-first behavior.

## Core Goal

Create sales collateral, objection handling, demos, one-pagers, or decks that reuse ZackAI’s current value props, proof, and competitor framing while adapting the sales motion to the actual audience requested.

## Required Read-First Workflow

Before drafting or asking broad discovery questions, read:
- .agents/product-marketing-context.md
- src/content/docs/marketing/campaign-copy.md
- src/content/docs/market/competitive-landscape.md
- src/content/docs/product/features.md
- src/content/docs/product/overview.md
- src/content/docs/product/specifications.md
- src/content/docs/brand/voice-tone.md

## ZackAI Source-of-Truth Rules

Canonical inputs, in order:
1. `.agents/product-marketing-context.md`
2. `README.md`
3. `src/content/docs/**`
4. `src/content/frDocs/**` for French or bilingual work

Never use `wiki-output/**`, `wiki-output-fr/**`, or `wiki-site/**` as the primary source for regeneration, rewriting, or claim harvesting.

## Reuse-First Rules

- Reuse current value props, proof points, objections, and competitive framing from canonical root docs before drafting new collateral.
- Create a new deck, one-pager, objection doc, or pitch artifact only when that deliverable is explicitly needed; otherwise extend the existing source docs.
- Do not force generic B2B SaaS sales language onto ZackAI. Adapt the motion to the real request, such as Kickstarter backers, retail buyers, distributors, schools, gifting partnerships, creators, or press.
- Keep ROI or proof sections honest about the current repo state, which is primarily launch-stage marketing rather than a mature SaaS funnel with abundant customer metrics.
- When French or bilingual collateral is needed, review the matching localized docs before rephrasing.

## ZackAI-Specific Guidance

- Tie every claim to a concrete family, buyer, or business outcome.
- Keep collateral scannable and usable in real conversations.
- Re-use the objections already documented in the product context, including safety, boredom risk, price, and screen concerns.
- Stay consistent with `competitive-landscape.md` when describing alternatives or objections.
- If the requested sales motion is unclear, ask a narrow follow-up instead of assuming an enterprise SaaS funnel.

## Output Expectations

When responding:
1. Name the repo files you used.
2. State the target audience and stage for the collateral.
3. Explain whether the work should extend an existing ZackAI doc or live as a new deliverable, and flag any unsupported proof or motion assumptions.

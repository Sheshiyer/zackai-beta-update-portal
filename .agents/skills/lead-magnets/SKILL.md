---
name: "lead-magnets"
description: "ZackAI project wrapper for lead-magnets. Use it to plan lead capture offers, but always start from ZackAI\u2019s existing marketing assets and nurture docs before proposing new gated content."
metadata:
  version: "1.0.0-zackai.1"
  basedOn: "global/lead-magnets@1.0.0"
---

# lead-magnets — ZackAI Wrapper

This project-level skill keeps the original `lead-magnets` purpose, but adds ZackAI-specific reuse-first behavior.

## Core Goal

Plan lead magnets and lead-capture offers that solve a specific problem and naturally connect to ZackAI, while reusing existing repo messaging and assets before recommending new standalone offers.

## Required Read-First Workflow

Before drafting or asking broad discovery questions, read:
- .agents/product-marketing-context.md
- src/content/docs/marketing/email-templates.md
- src/content/docs/marketing/social-content.md
- src/content/docs/marketing/campaign-copy.md
- src/content/docs/product/features.md
- src/content/docs/marketing/whatsapp-templates.md
- src/content/docs/audience/primary-persona.md

## ZackAI Source-of-Truth Rules

Canonical inputs, in order:
1. `.agents/product-marketing-context.md`
2. `README.md`
3. `src/content/docs/**`
4. `src/content/frDocs/**` for French or bilingual work

Never use `wiki-output/**`, `wiki-output-fr/**`, or `wiki-site/**` as the primary source for regeneration, rewriting, or claim harvesting.

## Reuse-First Rules

- Start from the offers, hooks, objections, and nurture patterns already present in the current marketing docs.
- Prefer adding a lead-magnet appendix, offer matrix, or CTA block to an existing marketing doc before drafting a standalone ebook or resource spec.
- Match the proposed lead magnet to buyer stage and to the follow-up assets that already exist in email, social, and messaging docs.
- Do not recommend gated content when a high-value ungated root doc could be upgraded more efficiently.
- For bilingual work, note which matching French docs need to be updated alongside the English source.

## ZackAI-Specific Guidance

- Solve one specific parent or buyer problem at a time.
- Keep time-to-value low and the path to ZackAI purchase or signup obvious.
- Use current ZackAI themes such as screen-free play, multilingual growth, bedtime, emotional reassurance, independent play, gifting, privacy trust, and no-subscription value when relevant.
- Prefer lead magnets that can be assembled from existing docs over net-new large-format content.
- Do not invent download counts, performance benchmarks, or customer proof not present in canonical files.

## Output Expectations

When responding:
1. Name the repo files you used.
2. Specify the buyer stage, format, promise, CTA, and follow-up path.
3. State which existing ZackAI docs should be updated and what truly new work, if any, is still required.

---
name: "cold-email"
description: "ZackAI project wrapper for cold-email. Use it for cold outreach emails and follow-up sequences, but always ground the work in ZackAI canonical markdown before drafting new copy."
metadata:
  version: "1.1.0-zackai.1"
  basedOn: "global/cold-email@1.1.0"
---

# cold-email — ZackAI Wrapper

This project-level skill keeps the original `cold-email` purpose, but adds ZackAI-specific reuse-first behavior.

## Core Goal

Write cold outreach emails and follow-up sequences that sound human, relevant, and low-friction. Preserve the original cold-email intent, but make the output clearly grounded in ZackAI messaging, proof, and audience context.

## Required Read-First Workflow

Before drafting or asking broad discovery questions, read:
- .agents/product-marketing-context.md
- src/content/docs/marketing/email-templates.md
- src/content/docs/marketing/campaign-copy.md
- src/content/docs/brand/voice-tone.md
- src/content/docs/audience/primary-persona.md
- src/content/frDocs/marketing/email-templates.md (for French or bilingual output)

## ZackAI Source-of-Truth Rules

Canonical inputs, in order:
1. `.agents/product-marketing-context.md`
2. `README.md`
3. `src/content/docs/**`
4. `src/content/frDocs/**` for French or bilingual work

Never use `wiki-output/**`, `wiki-output-fr/**`, or `wiki-site/**` as the primary source for regeneration, rewriting, or claim harvesting.

## Reuse-First Rules

- Reuse current hooks, proof points, objections, and CTA patterns from the existing email and campaign docs before inventing new copy.
- If the request is for reusable outbound collateral, extend `src/content/docs/marketing/email-templates.md` instead of creating a parallel email brief.
- Ask only for truly missing prospect-specific information such as company trigger, role, desired outcome, or social proof not already in the repo.
- If age range matters, follow the exact source file being extended; if synthesizing across docs, flag the current 3–8 vs 3–12 inconsistency instead of silently normalizing it.
- Check matching French docs before translating or rephrasing localized copy.

## ZackAI-Specific Guidance

- Sound like a thoughtful human peer, not a sales template or generic SDR.
- Keep one clear, low-friction ask per email.
- For ZackAI, outbound use cases may include partnerships, retail, education, press, creators, or gifting programs; use strict B2B/SDR conventions only when they actually fit the ask.
- Use screen-free play, multilingual learning, safety/privacy, emotional warmth, and no-subscription value when relevant, but do not force every point into every email.
- Do not invent customer quotes, results, or competitive claims that are not present in the canonical docs.

## Output Expectations

When responding:
1. Name the repo files you used.
2. State whether the draft is a one-off outreach asset or an update that should be folded back into `src/content/docs/marketing/email-templates.md`.
3. Call out any claims, proof, or audience facts that still need confirmation.

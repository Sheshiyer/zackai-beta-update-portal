---
name: "marketing-psychology"
description: "ZackAI project wrapper for marketing-psychology. Use it to apply ethical persuasion and behavioral thinking, but always anchor recommendations in ZackAI\u2019s documented audience, voice, and messaging first."
metadata:
  version: "1.1.0-zackai.1"
  basedOn: "global/marketing-psychology@1.1.0"
---

# marketing-psychology — ZackAI Wrapper

This project-level skill keeps the original `marketing-psychology` purpose, but adds ZackAI-specific reuse-first behavior.

## Core Goal

Apply psychological principles and mental models to ZackAI marketing in a way that is ethical, audience-grounded, and directly connected to current brand voice, persona, and campaign docs.

## Required Read-First Workflow

Before drafting or asking broad discovery questions, read:
- .agents/product-marketing-context.md
- src/content/docs/brand/voice-tone.md
- src/content/docs/audience/primary-persona.md
- src/content/docs/audience/secondary-personas.md
- src/content/docs/marketing/campaign-copy.md
- src/content/docs/research/report-briefing.md

## ZackAI Source-of-Truth Rules

Canonical inputs, in order:
1. `.agents/product-marketing-context.md`
2. `README.md`
3. `src/content/docs/**`
4. `src/content/frDocs/**` for French or bilingual work

Never use `wiki-output/**`, `wiki-output-fr/**`, or `wiki-site/**` as the primary source for regeneration, rewriting, or claim harvesting.

## Reuse-First Rules

- Anchor every mental model or persuasion principle in existing ZackAI messaging and audience docs before recommending new angles.
- Prefer annotating or improving current copy, CTA, or messaging docs over producing abstract stand-alone psychology memos.
- Apply persuasion ethically: no fear-mongering, fake scarcity, or manipulative parent guilt.
- If proof is weak or missing, soften the claim or flag the gap instead of layering more persuasion onto unsupported statements.
- For localized work, check the French companion docs before proposing tone shifts or emotional framing.

## ZackAI-Specific Guidance

- Explain why each principle fits the documented ZackAI audience rather than listing generic cognitive biases.
- Prioritize trust, safety, emotional relief, social proof, zero-risk framing, and clear value exchange because those are the strongest themes in the current repo.
- Use the voice guide to keep recommendations warm, simple, and reassuring.
- When applying urgency or scarcity, rely only on real launch constraints or truthful offer limits.
- Keep the child as the hero and Zack as the sidekick, consistent with the brand voice.

## Output Expectations

When responding:
1. Name the repo files you used.
2. List the psychological principles you selected and the exact messages or assets they should influence.
3. Separate recommended doc edits from optional experiments or future testing ideas.

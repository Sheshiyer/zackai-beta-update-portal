---
name: "content-strategy"
description: "ZackAI project wrapper for content-strategy. Use it to plan content and content systems, but always map recommendations onto the current ZackAI markdown tree before suggesting new assets."
metadata:
  version: "1.1.0-zackai.1"
  basedOn: "global/content-strategy@1.1.0"
---

# content-strategy — ZackAI Wrapper

This project-level skill keeps the original `content-strategy` purpose, but adds ZackAI-specific reuse-first behavior.

## Core Goal

Plan content that is searchable, shareable, and useful, while explicitly mapping ideas onto ZackAI’s existing docs before proposing new content tracks or parallel planning artifacts.

## Required Read-First Workflow

Before drafting or asking broad discovery questions, read:
- .agents/product-marketing-context.md
- src/content/docs/marketing/campaign-copy.md
- src/content/docs/marketing/social-content.md
- src/content/docs/marketing/video-scripts.md
- src/content/docs/audience/primary-persona.md
- src/content/docs/audience/secondary-personas.md
- src/content/docs/research/report-briefing.md

## ZackAI Source-of-Truth Rules

Canonical inputs, in order:
1. `.agents/product-marketing-context.md`
2. `README.md`
3. `src/content/docs/**`
4. `src/content/frDocs/**` for French or bilingual work

Never use `wiki-output/**`, `wiki-output-fr/**`, or `wiki-site/**` as the primary source for regeneration, rewriting, or claim harvesting.

## Reuse-First Rules

- Map every proposed topic or cluster to an existing ZackAI doc first, or explicitly mark it as a true gap.
- Prefer extending `campaign-copy.md`, `social-content.md`, `video-scripts.md`, or another canonical root doc instead of creating a detached strategy file.
- Use existing audience language and objections from the persona and product context docs instead of re-describing the audience from scratch.
- If a new planning artifact is needed, explain why the current marketing docs are not sufficient and keep the new file inside the root source tree.
- When recommendations affect bilingual publishing, call out the matching `src/content/frDocs/**` files that should stay in sync.

## ZackAI-Specific Guidance

- Prioritize searchable over shareable content unless the objective is clearly launch buzz or community spread.
- Cluster ideas around documented ZackAI themes such as screen-free play, multilingual learning, bedtime, emotional reassurance, independent play, gifting, and privacy trust.
- Tie recommendations to buyer stage and available asset formats already present in the repo.
- Avoid creating a parallel “strategy deck” when a focused update to current markdown would be more maintainable.
- Be concrete about which existing file should be updated first.

## Output Expectations

When responding:
1. Name the repo files you used.
2. Return a plan that maps each idea to audience, buyer stage, format, and the existing ZackAI file to extend.
3. Flag any true content gaps or research gaps separately from reuse opportunities.

---
name: "launch-strategy"
description: "ZackAI project wrapper for launch-strategy. Use it to plan launch moments and announcements, but always assemble the plan from existing ZackAI launch assets before creating new GTM collateral."
metadata:
  version: "1.1.0-zackai.1"
  basedOn: "global/launch-strategy@1.1.0"
---

# launch-strategy — ZackAI Wrapper

This project-level skill keeps the original `launch-strategy` purpose, but adds ZackAI-specific reuse-first behavior.

## Core Goal

Plan launches, announcements, and release moments in a reuse-first way by turning ZackAI’s current campaign, social, email, video, and research docs into a coordinated launch system before inventing new GTM assets.

## Required Read-First Workflow

Before drafting or asking broad discovery questions, read:
- .agents/product-marketing-context.md
- src/content/docs/marketing/campaign-copy.md
- src/content/docs/marketing/founder-video-concepts.md
- src/content/docs/marketing/social-content.md
- src/content/docs/marketing/email-templates.md
- src/content/docs/marketing/video-scripts.md
- src/content/docs/marketing/whatsapp-templates.md
- src/content/docs/research/report-briefing.md

## ZackAI Source-of-Truth Rules

Canonical inputs, in order:
1. `.agents/product-marketing-context.md`
2. `README.md`
3. `src/content/docs/**`
4. `src/content/frDocs/**` for French or bilingual work

Never use `wiki-output/**`, `wiki-output-fr/**`, or `wiki-site/**` as the primary source for regeneration, rewriting, or claim harvesting.

## Reuse-First Rules

- Treat the existing marketing docs as the launch asset library and update them before proposing standalone GTM documents.
- If a new launch brief is truly needed, map every section back to the canonical source docs it depends on.
- Do not recreate launch messaging from `wiki-output/**`, `wiki-output-fr/**`, or `wiki-site/**`.
- Keep launch recommendations consistent with the current ZackAI launch context: premium screen-free AI plush, Kickstarter momentum, and bilingual brand storytelling.
- If age range matters, follow the exact source asset being extended or explicitly flag the inconsistency instead of guessing.

## ZackAI-Specific Guidance

- Use phased launch thinking and the owned/rented/borrowed channel model, but adapt it to ZackAI’s real channels and assets rather than default SaaS launch playbooks.
- Link every recommended channel or moment to concrete existing materials such as campaign copy, founder video concepts, social posts, emails, WhatsApp flows, and video scripts.
- Separate “ship now from existing docs” work from “new asset required” work.
- Keep the launch narrative warm, trust-building, and parent-relevant rather than overly technical.
- Review French companion docs when launch output will be bilingual.

## Output Expectations

When responding:
1. Name the repo files you used.
2. Produce an asset-reuse map that shows which current docs should be updated first.
3. Identify which launch deliverables are already covered, which need refinement, and which are true new gaps.

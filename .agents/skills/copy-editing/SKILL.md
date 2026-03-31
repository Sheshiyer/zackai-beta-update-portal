---
name: "copy-editing"
description: "ZackAI project wrapper for copy-editing. Use it to improve existing marketing copy, but always edit against ZackAI source-of-truth voice, claims, and product context rather than producing parallel rewrites."
metadata:
  version: "1.1.0-zackai.1"
  basedOn: "global/copy-editing@1.1.0"
---

# copy-editing — ZackAI Wrapper

This project-level skill keeps the original `copy-editing` purpose, but adds ZackAI-specific reuse-first behavior.

## Core Goal

Improve existing copy through focused editing passes while preserving the original message and aligning the result with current ZackAI voice, claims, and canonical markdown.

## Required Read-First Workflow

Before drafting or asking broad discovery questions, read:
- The exact file or snippet being edited
- .agents/product-marketing-context.md
- src/content/docs/brand/voice-tone.md
- The closest canonical source file that supports the claims in the copy being edited
- The matching `src/content/frDocs/**` file when the request is French or bilingual

## ZackAI Source-of-Truth Rules

Canonical inputs, in order:
1. `.agents/product-marketing-context.md`
2. `README.md`
3. `src/content/docs/**`
4. `src/content/frDocs/**` for French or bilingual work

Never use `wiki-output/**`, `wiki-output-fr/**`, or `wiki-site/**` as the primary source for regeneration, rewriting, or claim harvesting.

## Reuse-First Rules

- Edit in place whenever possible; do not create “v2” or parallel rewrite docs unless the user explicitly asks for alternatives.
- Preserve the core message and only strengthen claims that are actually supported by canonical ZackAI docs.
- Keep terminology consistent with `.agents/product-marketing-context.md` and `src/content/docs/brand/voice-tone.md`.
- If a proof point or product claim is unsupported, flag it instead of polishing it into something stronger but less accurate.
- For French or bilingual work, check the localized source file before making tone or terminology decisions.

## ZackAI-Specific Guidance

- Use multi-pass editing: clarity, voice, so-what, proof, specificity, emotion, and risk.
- Preserve the author’s voice where it is working; prefer surgical edits over wholesale rewrites.
- Make the child/parent benefit clearer when the copy drifts into internal product language.
- When useful, show before/after snippets or grouped edits so the reasoning is easy to follow.
- Do not introduce cold technical language that conflicts with ZackAI’s warm, trust-building tone.

## Output Expectations

When responding:
1. Name the file(s) or snippets you edited.
2. Summarize the main editing passes you applied.
3. Call out any factual, proof, or tone issues that still need source confirmation.

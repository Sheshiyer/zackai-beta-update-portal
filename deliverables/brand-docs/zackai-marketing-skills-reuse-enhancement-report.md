# ZackAI Marketing Skills Reuse & Enhancement Report

## 1. Executive Summary

I reviewed the imported **33 marketing skills** against the current ZackAI markdown source tree.

### Current status at a glance
- **7 skills are ready now** — the repo already contains strong markdown support for them.
- **8 skills should be enhanced for reuse-first behavior** — they are relevant, but should be explicitly wired to existing markdown before generating new outputs.
- **18 skills have low current evidence** — they may still be useful, but the repo does not yet contain enough dedicated markdown to support them cleanly without creating duplication.

### Main conclusion
The ZackAI repo already has a strong reusable markdown base for:
- product positioning
- personas and audience
- brand voice
- campaign copy
- ad creative
- email templates
- social content
- video scripts
- WhatsApp templates
- product overview / features / specifications
- competitive landscape
- research reports

The biggest opportunity is **not creating more parallel content**.

Instead, the imported skills should follow a simple rule:
> **Read and extend the existing root markdown first. Only create new docs when the current source tree truly has a gap.**

## 2. Source of Truth to Reuse

Treat these as primary source of truth:

- [`.agents/product-marketing-context.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/product-marketing-context.md)
- [`README.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/README.md)
- [`src/content/docs/`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs)
- [`src/content/frDocs/`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/frDocs)

### High-value markdown already present

#### Foundational context
- [`.agents/product-marketing-context.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/product-marketing-context.md)
- [`src/content/docs/index.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/index.md)
- [`src/content/docs/getting-started/quickstart.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/getting-started/quickstart.md)

#### Product
- [`src/content/docs/product/overview.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/product/overview.md)
- [`src/content/docs/product/features.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/product/features.md)
- [`src/content/docs/product/specifications.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/product/specifications.md)

#### Audience / positioning
- [`src/content/docs/audience/primary-persona.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/audience/primary-persona.md)
- [`src/content/docs/audience/secondary-personas.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/audience/secondary-personas.md)
- [`src/content/docs/market/competitive-landscape.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/market/competitive-landscape.md)

#### Brand
- [`src/content/docs/brand/voice-tone.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/brand/voice-tone.md)
- [`src/content/docs/brand/visual-guidelines.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/brand/visual-guidelines.md)
- [`src/content/docs/brand/visual-assets.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/brand/visual-assets.md)

#### Marketing execution
- [`src/content/docs/marketing/campaign-copy.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/campaign-copy.md)
- [`src/content/docs/marketing/ad-creative.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/ad-creative.md)
- [`src/content/docs/marketing/email-templates.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/email-templates.md)
- [`src/content/docs/marketing/social-content.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/social-content.md)
- [`src/content/docs/marketing/video-scripts.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/video-scripts.md)
- [`src/content/docs/marketing/founder-video-concepts.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/founder-video-concepts.md)
- [`src/content/docs/marketing/whatsapp-templates.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/whatsapp-templates.md)

#### Research
- [`src/content/docs/research/report-blog.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/research/report-blog.md)
- [`src/content/docs/research/report-briefing.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/research/report-briefing.md)
- [`src/content/docs/research/report-study-guide.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/research/report-study-guide.md)
- [`src/content/docs/research/notebooklm-artifacts.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/research/notebooklm-artifacts.md)

> The French tree under [`src/content/frDocs/`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/frDocs) should be treated as the bilingual companion to the English source tree.

## 3. Do Not Reload / Do Not Regenerate

Do **not** treat these as primary input for future regeneration:
- [`wiki-output/`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/wiki-output)
- [`wiki-output-fr/`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/wiki-output-fr)
- [`wiki-site/`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/wiki-site)

### Why
These look like duplicate, generated, or secondary trees. If skills read those first, they will:
- recreate content that already exists in root docs
- drift English and French content out of sync
- create conflicting versions of product/marketing truth
- make future updates harder because no one knows which tree is canonical

### Practical anti-duplication rule
If the content already exists in `src/content/docs/**` or `src/content/frDocs/**`, the skill should:
1. **read it**
2. **extend or revise it**
3. **avoid creating a parallel version elsewhere**

## 4. Skills Ready Now

These skills already have strong markdown support and can be used immediately in this repo.

### 1) `ad-creative`
**Why:** There is already a dedicated ad-creative markdown source.
**Read first:**
- [`src/content/docs/marketing/ad-creative.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/ad-creative.md)
- [`src/content/frDocs/marketing/ad-creative.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/frDocs/marketing/ad-creative.md)
**Rule:** Add variants to the existing creative system instead of creating a new ad brief.

### 2) `copywriting`
**Why:** Campaign and product copy foundations already exist.
**Read first:**
- [`src/content/docs/marketing/campaign-copy.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/campaign-copy.md)
- [`src/content/docs/product/overview.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/product/overview.md)
- [`src/content/docs/brand/voice-tone.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/brand/voice-tone.md)
**Rule:** Extend the current campaign/product narrative instead of inventing a second homepage story.

### 3) `email-sequence`
**Why:** The repo already contains email templates.
**Read first:**
- [`src/content/docs/marketing/email-templates.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/email-templates.md)
- [`src/content/frDocs/marketing/email-templates.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/frDocs/marketing/email-templates.md)
**Rule:** Modify and extend the current email library instead of writing a disconnected new sequence set.

### 4) `marketing-ideas`
**Why:** The current marketing markdown already contains many idea seeds across social, campaign, video, and messaging docs.
**Read first:**
- [`src/content/docs/marketing/social-content.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/social-content.md)
- [`src/content/docs/marketing/campaign-copy.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/campaign-copy.md)
- [`src/content/docs/marketing/video-scripts.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/video-scripts.md)
**Rule:** Brainstorm from the current docs, not from zero.

### 5) `paid-ads`
**Why:** Paid-message ingredients already exist in ad creative + campaign copy.
**Read first:**
- [`src/content/docs/marketing/ad-creative.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/ad-creative.md)
- [`src/content/docs/marketing/campaign-copy.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/campaign-copy.md)
**Rule:** Reuse current hooks and angles before creating new audience/message systems.

### 6) `product-marketing-context`
**Why:** The repo-local context file now exists.
**Read first:**
- [`.agents/product-marketing-context.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/product-marketing-context.md)
**Rule:** Treat this as the single source for core product, audience, positioning, and messaging context.

### 7) `social-content`
**Why:** The repo already contains social content docs in both languages.
**Read first:**
- [`src/content/docs/marketing/social-content.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/social-content.md)
- [`src/content/frDocs/marketing/social-content.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/frDocs/marketing/social-content.md)
**Rule:** Extend the existing social calendar / post bank instead of creating a parallel one.

## 5. Skills to Enhance for Reuse-First Behavior

These skills are relevant, but should be made more reuse-aware before heavy use.

### 1) `cold-email`
**Read first:** [`src/content/docs/marketing/email-templates.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/email-templates.md)
**Enhancement:** Add a clear repo-specific rule: reuse tone, CTA structure, and objections from current email templates before drafting outbound copy.

### 2) `competitor-alternatives`
**Read first:**
- [`src/content/docs/market/competitive-landscape.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/market/competitive-landscape.md)
- [`src/content/docs/product/features.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/product/features.md)
**Enhancement:** Force the skill to build comparisons from the current competitor landscape instead of recreating battle cards each time.

### 3) `content-strategy`
**Read first:**
- [`.agents/product-marketing-context.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/product-marketing-context.md)
- [`src/content/docs/marketing/campaign-copy.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/campaign-copy.md)
- [`src/content/docs/audience/primary-persona.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/audience/primary-persona.md)
**Enhancement:** Have the skill map new content ideas onto existing persona + campaign docs before creating a fresh editorial map.

### 4) `copy-editing`
**Read first:**
- [`src/content/docs/marketing/campaign-copy.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/campaign-copy.md)
- [`src/content/docs/brand/voice-tone.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/brand/voice-tone.md)
**Enhancement:** Bias the skill toward revising current markdown rather than re-drafting sections wholesale.

### 5) `launch-strategy`
**Read first:**
- [`src/content/docs/marketing/campaign-copy.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/campaign-copy.md)
- [`src/content/docs/research/report-briefing.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/research/report-briefing.md)
- [`src/content/docs/index.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/index.md)
**Enhancement:** The skill should append tactical launch structure onto the existing campaign plan instead of producing a disconnected GTM document.

### 6) `lead-magnets`
**Read first:**
- [`src/content/docs/marketing/email-templates.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/email-templates.md)
- [`src/content/docs/marketing/social-content.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/social-content.md)
- [`src/content/docs/product/features.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/product/features.md)
**Enhancement:** Introduce a lead-magnet appendix inside existing marketing docs before creating a standalone asset library.

### 7) `marketing-psychology`
**Read first:**
- [`src/content/docs/brand/voice-tone.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/brand/voice-tone.md)
- [`src/content/docs/research/report-briefing.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/research/report-briefing.md)
**Enhancement:** Add explicit persuasion / behavioral hooks to the voice system rather than creating a new disconnected psychology framework.

### 8) `sales-enablement`
**Read first:**
- [`src/content/docs/marketing/campaign-copy.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/campaign-copy.md)
- [`src/content/docs/market/competitive-landscape.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/market/competitive-landscape.md)
- [`src/content/docs/product/features.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/product/features.md)
**Enhancement:** Build decks / talk tracks from current campaign + competitor + feature docs rather than recreating value props in a separate sales narrative.

## 6. Skills With Low Current Evidence

These skills may still be useful, but the current markdown tree does not contain enough dedicated material to support them cleanly yet.

### Measurement / experimentation
- `ab-test-setup`
- `analytics-tracking`
- `schema-markup`
- `seo-audit`
- `ai-seo`

### CRO / lifecycle
- `form-cro`
- `onboarding-cro`
- `page-cro`
- `paywall-upgrade-cro`
- `popup-cro`
- `signup-flow-cro`
- `churn-prevention`

### Growth / ops / SEO scale
- `free-tool-strategy`
- `programmatic-seo`
- `referral-program`
- `revops`
- `site-architecture`
- `pricing-strategy`

### What “low evidence” means here
It does **not** mean these skills are bad.
It means the repo does not yet contain strong, dedicated markdown that would let those skills operate in a reuse-first, no-duplication way.

For these skills, the best first move is often:
1. read [`.agents/product-marketing-context.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/product-marketing-context.md)
2. read the most relevant product / marketing doc
3. capture the missing framework into root markdown
4. only then generate broader assets

## 7. Recommended Enhancement Backlog (Top 10)

1. **Create a reusable idea bank inside** [`src/content/docs/marketing/campaign-copy.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/campaign-copy.md)
   - So `marketing-ideas` and `content-strategy` expand existing themes instead of recreating them.

2. **Add a launch playbook section inside campaign markdown**
   - So `launch-strategy` stops generating parallel GTM docs.

3. **Expand** [`.agents/product-marketing-context.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/product-marketing-context.md) **every sprint**
   - So all future skills start from the latest positioning and audience truth.

4. **Add persuasion / psychology notes into** [`src/content/docs/brand/voice-tone.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/brand/voice-tone.md)
   - So `marketing-psychology` is grounded in existing brand voice.

5. **Formalize reuse notes inside** [`src/content/docs/marketing/email-templates.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/email-templates.md)
   - So `email-sequence`, `cold-email`, and `lead-magnets` share one base.

6. **Turn** [`src/content/docs/market/competitive-landscape.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/market/competitive-landscape.md) **into a battle-card source**
   - So `competitor-alternatives` and `sales-enablement` reuse one comparison system.

7. **Add a social cadence / content architecture section to** [`src/content/docs/marketing/social-content.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/social-content.md)
   - So `marketing-ideas` and `social-content` extend an existing rhythm.

8. **Add a WhatsApp reuse playbook to** [`src/content/docs/marketing/whatsapp-templates.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/src/content/docs/marketing/whatsapp-templates.md)
   - So the team reuses current message structures instead of generating more message banks elsewhere.

9. **Create a lightweight experimentation / measurement section in root docs**
   - This would unlock better support for `ab-test-setup` and `analytics-tracking`.

10. **Create a lightweight SEO / structured-data section in root docs**
   - This would unlock cleaner use of `ai-seo`, `seo-audit`, `schema-markup`, and `programmatic-seo`.

## 8. Practical Operating Rules

- **Always read root source docs first.**
  Start with `.agents/product-marketing-context.md`, then the most relevant file under `src/content/docs/**` / `src/content/frDocs/**`.

- **Never regenerate from `wiki-output`, `wiki-output-fr`, or `wiki-site`.**
  Those trees should not drive new content creation.

- **Extend before creating.**
  If a relevant markdown file already exists, update it or append to it before creating a new document.

- **Keep bilingual parity in mind.**
  If you update a high-value English marketing doc, check whether the matching French doc should also be updated.

- **Cite the files you reused.**
  When a skill is used, explicitly note which markdown files it read first.

- **Preserve one narrative spine.**
  Product story, campaign messaging, brand tone, and competitive positioning should continue to flow from the same root markdown system.

- **Use low-evidence skills carefully.**
  For those skills, first capture missing knowledge into root docs so future runs don’t repeat the same discovery work.

## 9. Skill Matrix

| Skill | Status | Read First | Reuse / Enhancement Note |
| --- | --- | --- | --- |
| ab-test-setup | Low evidence | `.agents/product-marketing-context.md`<br>`README.md` | Layer new experiment planning on the existing context docs before drafting standalone A/B test briefs. |
| ad-creative | Ready now | `src/content/docs/marketing/ad-creative.md` | Build on the established ad concepts to avoid recreating paid creatives. |
| ai-seo | Low evidence | `.agents/product-marketing-context.md`<br>`src/content/docs/research/report-study-guide.md` | Start from the research brief and avoid parallel AI SEO write-ups until the repo has dedicated SEO docs. |
| analytics-tracking | Low evidence | `README.md` | Capture tracking needs in root docs before drafting separate analytics plans. |
| churn-prevention | Low evidence | `src/content/docs/marketing/campaign-copy.md`<br>`src/content/docs/research/report-study-guide.md` | Reference the current campaign messaging when proposing retention tactics to prevent redundant positioning docs. |
| cold-email | Enhance for reuse | `src/content/docs/marketing/email-templates.md` | Augment the existing email templates instead of writing new cold sequences from scratch. |
| competitor-alternatives | Enhance for reuse | `src/content/docs/market/competitive-landscape.md`<br>`src/content/docs/product/features.md` | Frame comparison pages around the documented landscape so the team avoids redundant battle cards. |
| content-strategy | Enhance for reuse | `.agents/product-marketing-context.md`<br>`src/content/docs/marketing/campaign-copy.md` | Use the current campaign copy plan as the starting list of topics rather than reinventing the content map. |
| copy-editing | Enhance for reuse | `src/content/docs/marketing/campaign-copy.md`<br>`src/content/docs/brand/voice-tone.md` | Edit within the existing campaign copy and voice docs instead of publishing parallel revisions. |
| copywriting | Ready now | `src/content/docs/marketing/campaign-copy.md` | Expand on the documented campaign copy structure instead of duplicating hero narratives. |
| email-sequence | Ready now | `src/content/docs/marketing/email-templates.md` | Iterate on the established email templates rather than spinning up a new sequence repository. |
| form-cro | Low evidence | `README.md` | Document form optimization needs in root docs before splitting into dedicated CRO briefs. |
| free-tool-strategy | Low evidence | `README.md` | Reference the launch dossier before drafting a new free-tool strategy. |
| launch-strategy | Enhance for reuse | `src/content/docs/marketing/campaign-copy.md`<br>`src/content/docs/research/report-briefing.md` | Tie launch checklists to the existing campaign plan to avoid creating redundant go-to-market decks. |
| lead-magnets | Enhance for reuse | `src/content/docs/marketing/email-templates.md`<br>`src/content/docs/marketing/social-content.md` | Link opt-in content proposals to current templates instead of adding duplicate lead-magnet specs. |
| marketing-ideas | Ready now | `src/content/docs/marketing/social-content.md` | Use the social-content rhythms as the idea bank so the team does not duplicate brainstorm docs. |
| marketing-psychology | Enhance for reuse | `src/content/docs/brand/voice-tone.md`<br>`src/content/docs/research/report-briefing.md` | Anchor psychological hooks in the established voice guide to prevent parallel persuasion frameworks. |
| onboarding-cro | Low evidence | `.agents/product-marketing-context.md` | Capture onboarding needs within the product context doc before crafting a separate CRO narrative. |
| page-cro | Low evidence | `.agents/product-marketing-context.md`<br>`README.md` | Audit conversions using the existing context docs rather than drafting new page-CRO summaries. |
| paid-ads | Ready now | `src/content/docs/marketing/ad-creative.md` | Build paid-channel strategy around the documented ad creative to avoid duplicated audience guidance. |
| paywall-upgrade-cro | Low evidence | `.agents/product-marketing-context.md` | Document upgrade moments inside the product context before specing a standalone paywall-CRO guide. |
| popup-cro | Low evidence | `README.md` | Map popup intents in root docs to keep new CRO notes from overlapping. |
| pricing-strategy | Low evidence | `src/content/docs/product/specifications.md`<br>`src/content/docs/product/overview.md` | Reference the product specs/overview before creating new pricing narratives. |
| product-marketing-context | Ready now | `.agents/product-marketing-context.md` | Treat this file as the single source to avoid duplicating foundational context. |
| programmatic-seo | Low evidence | `.agents/product-marketing-context.md` | Detail templated SEO plans only after the product context is synced to avoid redundant outlines. |
| referral-program | Low evidence | `src/content/docs/marketing/social-content.md` | Fit referral concepts into the existing social plan rather than inventing a separate community doc. |
| revops | Low evidence | `README.md` | Document RevOps needs in root docs to prevent duplicative ops playbooks. |
| sales-enablement | Enhance for reuse | `src/content/docs/marketing/campaign-copy.md`<br>`src/content/docs/market/competitive-landscape.md` | Lean on campaign messaging and competitor landscape when drafting sales assets to avoid conflicting decks. |
| schema-markup | Low evidence | `.agents/product-marketing-context.md` | Outline structured-data needs in root docs before designing new schema docs. |
| seo-audit | Low evidence | `README.md` | Capture ranking issues in root docs to avoid duplicating audits without new evidence. |
| signup-flow-cro | Low evidence | `.agents/product-marketing-context.md` | Ensure signup-friction notes stay in the context doc to prevent redundant CRO briefs. |
| site-architecture | Low evidence | `src/content/docs/product/overview.md`<br>`src/content/docs/market/competitive-landscape.md` | Base site planning on the existing overview and landscape pages so the team does not produce competing sitemaps. |
| social-content | Ready now | `src/content/docs/marketing/social-content.md` | Expand the documented social plan rather than writing a parallel calendar. |

## 10. Bottom Line

The repo already has enough markdown to make several imported marketing skills immediately useful.

The highest-value behavior change is simple:
- **stop regenerating what already exists**
- **reuse root markdown first**
- **enhance a few key skills to be file-aware**
- **only create new docs for true gaps**

That will keep ZackAI's product and marketing knowledge compact, reusable, and much easier to maintain.

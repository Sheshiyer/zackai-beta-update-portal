# TODO

## Plan

- [x] Confirm the deployed source of truth and capture root-cause notes for the root-vs-`wiki-site` drift.
- [x] Sync the root content schema with the newer markdown frontmatter used by the founder and WhatsApp docs.
- [x] Add the missing English and French marketing docs to the root content tree.
- [x] Update root i18n and docs index content so the new docs and research wording show up correctly in the menu and landing pages.
- [x] Port the search UI from `wiki-site` into the root app and wire it into the root layout/styles.
- [x] Verify with a production build and record the outcome plus any residual risk.

## Notes

- User-reported main issues: search, founder script tags/docs, menu updates, and French content not matching the main Vercel site.
- Investigation found that the root Astro app is the deployed app, while newer search/menu/content changes exist only under `wiki-site/`.

## Review

- Root-cause confirmed: Vercel-targeted root app had drifted from the newer `wiki-site/` subtree, so search, founder docs, and some FR/menu updates were never reaching the deployed source tree.
- Added root-side search UI, synced i18n/menu wording, and copied the missing founder/WhatsApp docs into both locales under `src/content/`.
- Verification passed with `npm run build` after temporarily exposing the existing `wiki-site/node_modules` install to the root app for local validation.
- Build evidence: generated routes now include `/docs/marketing/founder-video-concepts`, `/docs/marketing/whatsapp-templates`, `/fr/docs/marketing/founder-video-concepts`, and `/fr/docs/marketing/whatsapp-templates`.
- Rendered output evidence: built HTML contains the search trigger/button, French “Recherche” quicklink, and the new FR menu/index entries for founder video concepts and WhatsApp templates.
- Residual risk: the repo still contains duplicated root and `wiki-site/` app trees, so future content drift will recur unless one becomes the explicit source of truth.

## Product Marketing Context Draft

- [x] Confirm whether `.agents/product-marketing-context.md` already exists in the repo
- [x] Draft a v1 from the current wiki source files in `src/content/`, `src/data/site-data.json`, and `brand-config.yaml`
- [x] Save the repo-local product marketing context for use by the imported global marketing skills
- [x] Review gaps or contradictions that still need user confirmation

### Context Review

- Created [`.agents/product-marketing-context.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/product-marketing-context.md)
- Grounded the draft in the current repo's wiki sources, especially `src/content/docs/`, `src/data/site-data.json`, and `brand-config.yaml`
- Captured ZackAI positioning, personas, pain points, competitors, differentiators, objections, customer language, brand voice, proof points, and launch goals
- Preserved the main open inconsistency found in the repo: high-level docs say **3–8**, while detailed product/positioning docs mostly say **3–12**

## Skills Enhancement Report

- [x] Extract imported marketing skill metadata from global skills
- [x] Inventory repo markdown source-of-truth files and frontmatter
- [x] Map existing markdown assets to relevant skills
- [x] Identify which skills are already supported vs should be enhanced
- [x] Write a report explaining what to reuse and what not to regenerate

### Report Review

- Created [`deliverables/brand-docs/zackai-marketing-skills-reuse-enhancement-report.md`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/deliverables/brand-docs/zackai-marketing-skills-reuse-enhancement-report.md)
- Classified the imported 33 marketing skills into three buckets: ready now, enhance for reuse, and low evidence
- Documented the canonical source-of-truth files and explicitly warned against using `wiki-output/**`, `wiki-output-fr/**`, and `wiki-site/**` as primary regeneration sources
- Added a full skill matrix with read-first paths and anti-duplication notes so future work extends existing markdown rather than recreating it

## Repo-Local Skill Wrappers

- [x] Read the current global `SKILL.md` files for the 8 target skills
- [x] Create `.agents/skills/{slug}/SKILL.md` wrappers in the repo with ZackAI-specific reuse rules
- [x] Validate the new files structurally with a local frontmatter check
- [x] Validate the project-level skill files with `skill_validate`
- [x] Update task tracking with implementation and review notes

### Wrapper Review

- Created project-level wrapper skills for:
  - [`cold-email`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/skills/cold-email/SKILL.md)
  - [`competitor-alternatives`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/skills/competitor-alternatives/SKILL.md)
  - [`content-strategy`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/skills/content-strategy/SKILL.md)
  - [`copy-editing`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/skills/copy-editing/SKILL.md)
  - [`launch-strategy`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/skills/launch-strategy/SKILL.md)
  - [`lead-magnets`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/skills/lead-magnets/SKILL.md)
  - [`marketing-psychology`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/skills/marketing-psychology/SKILL.md)
  - [`sales-enablement`](file:///Volumes/madara/2026/twc-vault/01-Projects/HeyZack/zackai-launch/beta-update-github/.agents/skills/sales-enablement/SKILL.md)
- Each wrapper preserves the original skill purpose while forcing ZackAI read-first behavior against `.agents/product-marketing-context.md`, `README.md`, `src/content/docs/**`, and `src/content/frDocs/**`
- Each wrapper explicitly blocks `wiki-output/**`, `wiki-output-fr/**`, and `wiki-site/**` from being used as primary regeneration inputs
- Local structural validation passed for all 8 files, and `skill_validate` confirmed all 8 wrappers from the **project tier**

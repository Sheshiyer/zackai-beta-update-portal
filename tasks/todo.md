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

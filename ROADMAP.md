# v1 Hardening Roadmap

Status tracking for moving from prototype to release-ready v1.

---

## Priority 1 — Must Fix (Bugs that will break the pipeline)

- [x] **1. Normalize asset paths across all skills**
  Standardized: vanilla = `website/assets/`, React = `website/public/assets/`. Curator reads `design_brief.stack_recommendation` to decide. Updated Curator, Site Builder pipeline position, pre-flight gate, and favicon section.

- [x] **2. Add `website/` directory creation to the Curator skill's pre-flight**
  Added to Curator's Non-Destructive Workflow section — creates `website/` if it doesn't exist before copying assets.

- [x] **3. Add local preview server instructions to the Site Builder skill**
  Added new Section 16 (Local Preview) with `python3 -m http.server 8000` for vanilla, `npm run dev` for React/Vite, and a warning against `file://`.

- [x] **4. Fix the Interviewer to save profile to an explicit, unambiguous path**
  Changed from "project root" to "the toolkit's root directory (the same directory that contains `CLAUDE.md`, `docs/`, and `schemas/`)."

- [x] **5. Add Formspree/Netlify Forms setup as a concrete step in the Site Builder skill**
  Expanded Section 9 (Form & Booking Strategy) with specific setup instructions for both backends, including HTML attributes and account creation steps.

- [x] **6. Add `netlify.toml` copy step to the Site Builder**
  Added new Section 14 (Deploy Preparation) — copies `templates/netlify.toml` into `website/` and adjusts for React builds. Added QA checklist item.

---

## Priority 2 — Must Add (Gaps that will cause user abandonment)

- [x] **7. Add image optimization guidance to the Curator skill**
  Added new Section 8 (Image Optimization) with target sizes (hero <400KB, gallery <200KB, portrait <150KB), `sips` resize commands, and squoosh.app fallback.

- [x] **8. Add HEIC-to-JPEG conversion handling**
  Added new Section 7 (HEIC Detection & Conversion) with macOS `sips` conversion and cross-platform guidance. Updated what-to-prepare.md to reassure about HEIC.

- [x] **9. Add project state tracking**
  Created `templates/pipeline-status.template.json`. Added Pipeline Status update instructions to all 5 skills. Added reference in CLAUDE.md project structure and a new Pipeline Status Tracking section.

- [x] **10. Add post-deploy verification checklist**
  Added to the Local Footprint Optimizer skill — 8-item checklist covering images, fonts, forms, mobile, HTTPS, speed, social previews, and GBP.

- [x] **11. Add error recovery guidance to docs**
  Created `docs/troubleshooting.md` covering: lost progress, JSON errors, deploy discrepancies, form failures, deleted website folder, starting over, slow images, design changes. Added to CLAUDE.md project structure and README guides list.

- [x] **12. Inline the `design_brief` structure into `profile-schema.md`**
  Replaced the "see VVT skill" pointer with full field definitions for `design_brief`, `color_system`, `typography`, `signature_interactions`, and `section_patterns`. Also clarified `design_tokens` as derived from `design_brief`.

---

## Priority 3 — Should Fix (Inconsistencies and friction)

- [x] **13. Reconcile README "no monthly fees" with FAQ's Claude Pro requirement**
  Removed misleading "No monthly fees" from README headline. Added explicit "Cost" section to README listing Claude Pro, hosting, and domain costs. Updated "What You Need" to mention Claude Pro pricing and cancel-anytime.

- [x] **14. Remove "backward compatibility" language from VVT**
  Changed to: "a convenience reference for quick CSS custom property mapping — the `design_brief` is the canonical source."

- [x] **15. Align Quick Start step count across README and docs**
  Reviewed: README has 8 steps (including photo drop + deploy), your-first-site has 7 steps. Mapping is clear — different formats serving different purposes (quick reference vs walkthrough). No change needed.

- [x] **16. Add Node.js installation guidance for the React path**
  Added Step 6 to getting-started.md with nodejs.org link, LTS download, install steps, and verification command. Noted Claude will tell you if it's needed.

- [x] **17. Improve what-to-prepare with a "quick start" option**
  Added "Quick Start (Minimum Viable Package)" section at top: 5 photos + services + contact info. Reframed full checklist as optional for best results.

---

## Priority 4 — Should Add (Polish for release)

- [x] **18. Add a `.gitignore` template**
  Created `templates/.gitignore` with OS files, node_modules, editor files, and .env exclusions.

- [x] **19. Add a "troubleshooting" section to the FAQ**
  Added Troubleshooting section to faq.md with quick answers for: broken deploys, form issues, lost progress, photo problems. Points to full troubleshooting.md.

- [x] **20. Add explicit photo count/size expectations to the Curator skill's quality audit**
  Added Image size check to Quality Audit section: total count, directory size target (<5MB), 500KB flag, HEIC conversion count.

- [x] **21. Add a "what to check after deploy" doc or section**
  Covered by #10 (post-deploy verification checklist in the SEO skill). The skill walks the luthier through checks on the live URL.

---

## Panel Notes

### Key Tensions Resolved

**Complexity vs. Audience Capability:** Build guardrails INTO the skills (Claude checks before proceeding) rather than adding external tooling. The luthier should never need to run a script.

**Image Optimization:** Use OS-native tools (macOS `sips`) rather than requiring Node.js. Known compromise — full optimization may require a future dedicated skill.

**`design_tokens` vs. `design_brief` duplication:** Keep both for v1. `design_brief.color_system` is canonical; `design_tokens` is derived convenience. Removed "backward compatibility" framing.

### Standing Rules (from verification)
_(Errors discovered during implementation get added here as permanent instructions)_

---

## Files Modified

| File | Changes |
|---|---|
| `.claude/skills/luthier-interviewer.md` | Explicit save path, pipeline status tracking |
| `.claude/skills/visual-vibe-translator.md` | Removed backward compat language, pipeline status tracking |
| `.claude/skills/workbench-curator.md` | Asset path normalization, directory creation, HEIC conversion, image optimization, quality audit expansion, pipeline status tracking |
| `.claude/skills/luthier-site-builder.md` | Asset path normalization, form backend setup, deploy prep (netlify.toml), QA checklist expansion, local preview instructions, pipeline status tracking |
| `.claude/skills/local-footprint-optimizer.md` | Post-deploy verification checklist, pipeline status tracking |
| `schemas/profile-schema.md` | Full design_brief structure inlined, design_tokens clarified |
| `CLAUDE.md` | Pipeline status section, project structure updates |
| `README.md` | Cost section, honest Claude Pro pricing, troubleshooting link |
| `docs/getting-started.md` | Node.js installation guidance |
| `docs/what-to-prepare.md` | Quick start minimum package, HEIC reassurance |
| `docs/faq.md` | Troubleshooting section |
| `docs/troubleshooting.md` | **NEW** — Full error recovery guide |
| `templates/pipeline-status.template.json` | **NEW** — Pipeline state tracking template |
| `templates/.gitignore` | **NEW** — Git ignore template |

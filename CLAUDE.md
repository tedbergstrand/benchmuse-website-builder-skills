# Luthier Web Toolkit

A set of AI skills that builds bespoke websites for luthiers, guitar repair techs, and instrument builders. Every site is one-of-a-kind — never a template.

## Who This Is For

You're a luthier, guitar repair professional, or instrument builder who wants a professional website without paying monthly fees to Squarespace or Wix, and without being locked into a static page you can't update. You're using Claude Code to build and maintain your own site.

## How It Works

You chat with Claude through five skills, run in order. Each skill handles one phase of building your site.

| Step | Skill | What It Does |
|---|---|---|
| 1 | `/luthier-interviewer` | Claude asks you about your business, services, and story |
| 2 | `/visual-vibe-translator` | Claude analyzes your photos and style preferences to design your site's look |
| 3 | `/workbench-curator` | Claude organizes your photos and assigns them to pages |
| 4 | `/luthier-site-builder` | Claude builds your actual website |
| 5 | `/local-footprint-optimizer` | Claude adds SEO so customers can find you on Google |

## Project Structure

```
.
├── CLAUDE.md                      # This file
├── .claude/skills/                # The 5 skills (invoke with /skill-name)
├── docs/                          # Guides and help
│   ├── getting-started.md         # Install and setup
│   ├── your-first-site.md         # Step-by-step walkthrough
│   ├── updating-your-site.md      # How to make changes later
│   ├── what-to-prepare.md         # Photo and content checklist
│   ├── faq.md                     # Common questions
│   └── troubleshooting.md         # Error recovery and common fixes
├── schemas/
│   └── profile-schema.md          # Technical spec for luthier-profile.json
├── templates/
│   ├── netlify.toml               # Hosting config (copied into website/ by Site Builder)
│   ├── luthier-profile.template.json
│   ├── pipeline-status.template.json
│   └── .gitignore                 # Git ignore template (optional)
├── luthier-profile.json           # YOUR profile (created by Step 1)
├── pipeline-status.json           # Pipeline progress tracker (auto-updated by skills)
├── handoffs/                      # Per-step handoff files (written once per skill, never overwritten)
│   ├── 01-interview.md            # Written after Step 1
│   ├── 02-design.md               # Written after Step 2
│   ├── 03-curation.md             # Written after Step 3
│   ├── 04-build.md                # Written after Step 4
│   └── 05-seo.md                  # Written after Step 5
└── website/                       # YOUR site (created by Step 4)
```

## Key Rules for Claude

- **Anti-Template Mandate**: Every site must feel one-of-a-kind. No WordPress/Squarespace/Wix vibes.
- **No Hallucination**: Never invent instrument repair procedures, materials, or measurements. Only use what the luthier has stated.
- **Privacy First**: Never expose residential addresses. Respect the luthier's preferences about what's public.
- **Accessibility**: WCAG 2.1 AA compliance mandatory (skip-to-content, semantic HTML, ARIA, keyboard nav, color contrast, reduced motion).
- **Vanilla Default**: Default to Vanilla HTML/CSS/JS + GSAP via CDN. Only use React/Vite/Tailwind if the luthier confirms they have Node.js and the design demands it.
- **Asset Paths**: Vanilla sites use `website/assets/`. React/Vite sites use `website/public/assets/`. Check `design_brief.stack_recommendation` in the profile to determine which.
- **Quality Bar**: Every site must feel like it was designed by a high-end web agency. The design brief (from VVT) defines the specific standard for each project. There is no template — every site starts from the luthier's own photos, references, and story.

## Session Start

**When a user opens this project without invoking a specific skill** — whether they say "how do I use this?", "what do I do?", "hi", or anything else — your first move is always to check whether `pipeline-status.json` and the `handoffs/` folder exist. That tells you which case you're in.

---

### Case 1: First-Time User (no `pipeline-status.json`, no `handoffs/` folder)

This person is brand new. Assume they have very little experience with computers or software. Do NOT use any of these words: "skill", "invoke", "run", "execute", "command". Instead say "type" or "type this in the chat box."

Walk them through orientation in plain, warm, conversational language. Do it in stages — don't dump everything at once:

**Stage 1 — Welcome and explain what's about to happen:**
Tell them in 2–3 plain sentences what this toolkit does (builds them a professional website through conversation, no coding required, they'll own everything). Ask if they're primarily a guitar builder, repair tech, or both — this helps you understand their business before the interview starts.

**Stage 2 — Check if they're ready to begin:**
Tell them the interview takes about 15–20 minutes and all they need is: their services and prices, their contact info, and a quick sense of their story. They don't need photos yet — those come later. Ask: "Do you have that handy, or do you want a few minutes to gather it first?"

**Stage 3 — Send them in:**
Once they're ready, tell them to type exactly this in the chat box — nothing else, just these characters:

```
/luthier-interviewer
```

Explain that this will start a conversation where you ask them questions about their business. They just answer naturally, like talking to someone.

**Tone:** Warm, encouraging, never condescending. These are skilled craftspeople who are just unfamiliar with this kind of software. Treat them the way you'd treat an expert in their field who's new to yours.

---

### Case 2: Returning User (`pipeline-status.json` or `handoffs/` files exist)

Read `pipeline-status.json` and the highest-numbered file in `handoffs/`, then **confirm with the user before doing anything**. Do not assume they want to continue from that point — they may want to go back, start over, or do something different.

Present what you found in plain language, then ask:

> "It looks like you've completed [steps done so far] and the next step is [step name]. Does that sound right — want to pick up from there?"

If they confirm, give them the exact text to type to continue (e.g., "Great — type `/visual-vibe-translator` in the chat box and we'll get going").

If all 5 steps are done, summarize that the site is built and ask what they'd like to change or update.

**Do this regardless of what the user said to open the conversation** — whether they said "hi", "where was I?", "I'm back", or anything else. Don't wait for them to remember a specific phrase. Just check the files and ask.

## Pipeline Status Tracking

Each skill writes two things on completion:
- **`pipeline-status.json`** — machine-readable progress tracker (overwritten each time)
- **`handoffs/0N-stepname.md`** — a permanent, never-overwritten handoff file capturing what was decided at that step, and what to do next

Before starting any skill, read `pipeline-status.json` and the latest file in `handoffs/` to understand where the luthier left off. If `pipeline-status.json` doesn't exist, copy from `templates/pipeline-status.template.json`.

## Blocking Conditions

Before starting any skill, read `pipeline-status.json` to check the current state. If it doesn't exist, copy from `templates/pipeline-status.template.json`.

| Step | Cannot start until... |
|---|---|
| Visual Vibe Translator | `luthier-profile.json` exists with identity + services |
| Workbench Curator | Design brief populated in profile |
| Site Builder | Curator has populated assets AND design brief exists |
| SEO Optimizer | Site builds and previews without errors |

## Updating Your Site Later

Open this folder in Claude Code and tell Claude what you want to change. Examples:
- "Add a new service: Plek machine leveling at $200"
- "Swap out the hero photo with this new one"
- "Update my hours to appointment-only on weekends"

Claude will update your profile and rebuild the affected pages. Re-run `/local-footprint-optimizer` if you changed services, pricing, hours, or contact info. Then drag the updated `website/` folder to Netlify to redeploy.

If something goes wrong, see `docs/troubleshooting.md` for common fixes and error recovery.

# Luthier Web Toolkit

Build a professional, one-of-a-kind website for your instrument repair shop or custom building business. No templates. You own everything.

## What This Is

This toolkit uses Claude Code (an AI assistant) to build you a bespoke website through conversation. You answer questions about your business, drop in your best photos, and Claude designs and builds a site that looks like you hired a high-end web agency.

Your site gets hosted for free on Netlify. You own 100% of the code, design, and content. No lock-in.

## What You Need

1. **Claude Code** — The AI that builds your site. Requires a Claude Pro subscription ($20/month — you only need it while building or updating, cancel anytime between). Get it at [claude.ai/code](https://claude.ai/code)
2. **A Netlify account** — Free hosting for your site. Sign up at [netlify.com](https://app.netlify.com/signup)
3. **Your photos and info** — See `docs/what-to-prepare.md` for exactly what to gather

No programming experience required.

## Quick Start

1. Get the toolkit onto your computer — see [Getting the toolkit](#getting-the-toolkit) below, or `docs/getting-started.md` for more detail. Then open the folder in Claude Code.
2. Gather your materials — at minimum 5 photos, your services/prices, and contact info (see `docs/what-to-prepare.md`)
3. Type `/luthier-interviewer` — answer Claude's questions about your business (~15 min)
4. Drop your photos into the project folder
5. Type `/visual-vibe-translator` — Claude designs your site's look and feel
6. Type `/workbench-curator` — Claude curates and optimizes your photos
7. Type `/luthier-site-builder` — Claude builds your site and starts a preview server
8. Type `/local-footprint-optimizer` — Claude adds SEO
9. Drag your `website/` folder onto Netlify to go live

**Need to stop and come back later?** No problem — Claude tracks your progress and picks up where you left off.

For detailed instructions, see `docs/your-first-site.md`.

## Updating Your Site

Open this folder in Claude Code any time and tell Claude what you want to change:

> "Change my setup price to $95"
> "Add a before/after photo of that Martin restoration"  
> "I got my Taylor Gold certification, add that to the site"

Claude updates your site. You drag the folder to Netlify again. Done.

## What's Inside

| Folder | What It Is |
|---|---|
| `.claude/skills/` | The 5 AI skills that build your site |
| `docs/` | Setup guides, FAQ, troubleshooting, and help |
| `templates/` | Starter files (profile template, hosting config, pipeline tracker) |
| `benchmuse/` | BenchMuse brand assets (logo variants used in the "Built with BenchMuse" footer attribution) |
| `schemas/` | Technical spec for your profile data |

## Getting the toolkit

Three ways to get the files onto your computer. Pick the one you're most comfortable with — they all end up in the same place.

### Option A — Download as a ZIP (easiest, no account needed)

1. On this GitHub page, click the green **`< > Code`** button near the top of the file list.
2. Click **`Download ZIP`** at the bottom of the menu that appears.
3. Open the ZIP from your Downloads folder — it will unzip into a folder named `benchmuse-website-builder-skills-main`.
4. Drag that folder somewhere findable like your **Documents** or **Desktop**. You can rename it to something shorter if you want (e.g., `luthier-web-toolkit`).

**Getting updates later:** You'll need to re-download the ZIP and copy your personal files (`luthier-profile.json`, `pipeline-status.json`, the `handoffs/` folder, and your `website/` folder) from the old copy into the new one. Not elegant but it works. If you want painless updates, use Option B instead.

### Option B — GitHub Desktop (friendly GUI, easy updates)

If you want the one-click "check for updates" experience without learning the command line:

1. Install **GitHub Desktop** from [desktop.github.com](https://desktop.github.com).
2. Sign in with a free GitHub account (create one if you don't have one).
3. In GitHub Desktop: **File → Clone Repository → URL tab**, and paste:
   ```
   https://github.com/tedbergstrand/benchmuse-website-builder-skills
   ```
4. Choose where to save it (Documents is fine), click **Clone**.

**Getting updates later:** Open GitHub Desktop, click **`Fetch origin`** then **`Pull`**. Your personal files stay untouched because they're listed in `.gitignore`.

### Option C — Git on the command line (for the technical)

```bash
git clone https://github.com/tedbergstrand/benchmuse-website-builder-skills.git
cd benchmuse-website-builder-skills
```

Updates: `git pull` from inside the folder.

## Guides

- **[Getting Started](docs/getting-started.md)** — Install Claude Code and create your Netlify account
- **[Your First Site](docs/your-first-site.md)** — Step-by-step from zero to live website
- **[Updating Your Site](docs/updating-your-site.md)** — Making changes after launch
- **[What to Prepare](docs/what-to-prepare.md)** — Photos, text, and style references to gather
- **[Site Recommendations](docs/site-recommendations.md)** — Features and content that work well for each shop type
- **[FAQ](docs/faq.md)** — Common questions about cost, hosting, and troubleshooting
- **[Troubleshooting](docs/troubleshooting.md)** — Error recovery and common fixes

## Built For

- **Repair techs** — Service menus, pricing, intake forms, before/after galleries
- **Custom builders** — Portfolios, build logs, commission forms, materials showcase
- **Hybrid shops** — Both repair and building, with clear visual separation

## Cost

- **Claude Code:** $20/month while you're actively building or updating. Cancel between updates — your site stays live.
- **Hosting:** Free on Netlify (handles ~50-100K page views/month)
- **Domain name:** ~$15/year for a `.com` address
- **After launch:** Your only ongoing cost is the domain. You re-subscribe to Claude only when you want to make changes.

## Philosophy

- Every site is a one-of-a-kind digital experience, never a template
- You own your code, your data, and your hosting account
- If you outgrow this toolkit, take your code to any developer — there's no lock-in

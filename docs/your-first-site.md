# Building Your First Site

A step-by-step walkthrough from zero to a live website. The whole process takes about an hour of your time, spread across a few sessions if you prefer.

## Before You Start

**Hit your Claude quota mid-process?** No problem. After each step, Claude saves a handoff file in the `handoffs/` folder recording exactly what was decided and what to do next. When you come back — same session or days later — open this folder in Claude Code and say: *"I'm working on my website. Read the files in my handoffs/ folder and tell me where I left off."* Claude will pick up right where you stopped.

Make sure you've completed everything in `getting-started.md`:
- Claude Code installed (desktop or web app)
- Netlify account created
- This toolkit folder open in Claude Code

Also prepare your materials using the checklist in `what-to-prepare.md`. At minimum, you need 5 good photos, your services and prices, and your contact info. The full checklist gets better results but isn't required.

**iPhone photos?** Don't worry about `.HEIC` format — Claude converts them automatically on Mac.

---

## Step 1: The Interview

Type in Claude Code:
```
/luthier-interviewer
```

Claude will ask you about your business — who you are, what you do, where you're located, your services and pricing, your story. It's a conversation, not a form. Just answer naturally.

Claude will ask whether you primarily **build instruments**, **repair them**, or **both**. This shapes your entire site — a builder's site is portfolio-forward, a repair tech's site is service-forward, and a hybrid does both.

**This takes about 15-20 minutes.** At the end, Claude saves everything to `luthier-profile.json` — the single source of truth for your entire site. Claude also creates `pipeline-status.json` to track your progress through the pipeline.

---

## Step 2: Add Your Photos

Drop your prepared photos into the project folder. If you organized them per the checklist:
- `/photos` — Your best shots, logo, before/afters
- `/text` — Your story, pricing, repair notes (if you wrote them down)
- `/style` — Links to websites you like the look of

If you just have a folder of photos, that's fine too — Claude will sort through them.

---

## Step 3: Design Direction

Type:
```
/visual-vibe-translator
```

Claude will look at your photos, read your profile, and generate a complete design concept — colors, fonts, layout patterns, animation ideas. It presents the concept using physical analogies you'll understand (like "aged mahogany and warm amber" rather than "hex #C9A84C").

**Review the design direction.** Tell Claude if anything feels off:
- "I want it darker"
- "Can we use a different font? That feels too fancy"
- "I love that, but can the accent color be more blue?"

Claude revises until you're happy. This saves the design brief to your profile.

---

## Step 4: Photo Curation

Type:
```
/workbench-curator
```

Claude reviews all your photos, selects the best ones, assigns them to specific pages (hero, portfolio, about, etc.), and writes SEO-friendly descriptions for each.

During this step, Claude also:
- **Converts HEIC files** to JPEG if needed (automatic on Mac)
- **Optimizes image sizes** for fast loading (resizes large photos so your site loads quickly)
- **Copies curated photos** into your website's assets folder

If Claude thinks you need more photos, it'll tell you what's missing and suggest what to shoot.

---

## Step 5: Build the Site

Type:
```
/luthier-site-builder
```

This is where the magic happens. Claude reads your profile, design brief, and curated photos, then builds your entire website. For most luthiers, this produces a vanilla HTML/CSS/JS site — no special software needed to deploy it.

Claude also:
- **Sets up your contact form** using Netlify Forms (if hosting on Netlify) or Formspree. Claude will tell you which it chose and whether you need to do anything to activate it.
- **Copies your hosting config** (`netlify.toml`) into the website directory.
- **Starts a local preview server** so you can see the site in your browser at `http://localhost:8000`.

**Review every page.** Check:
- Does the layout feel right?
- Are the photos in the right places?
- Is the pricing correct?
- Does the mobile view work? (Resize your browser window to check)

Tell Claude about anything you want changed:
- "Make the hero text bigger"
- "Move the pricing section above the portfolio"
- "The contact form needs a field for instrument type"

Claude revises until you're satisfied.

---

## Step 6: SEO

Type:
```
/local-footprint-optimizer
```

Claude adds everything Google needs to find your site:
- Meta tags and page titles
- Schema.org markup (tells Google you're a repair shop or builder)
- A sitemap
- Social sharing tags (so your site looks good when shared on Facebook, Instagram, etc.)
- A Google Business Profile description you can copy/paste
- An `llms.txt` file so AI assistants (ChatGPT, Perplexity, etc.) can accurately describe your business

---

## Step 7: Go Live

Your site is ready to deploy.

1. Log into your Netlify account at [app.netlify.com](https://app.netlify.com)
2. Click **Add new site**
3. Click **Deploy manually**
4. Drag your entire `website/` folder onto the upload area
5. Wait about 30 seconds — Netlify gives you a temporary URL (something like `your-site-abc123.netlify.app`)
6. Visit that URL and verify everything works

### Post-Deploy Checklist

Run through these checks on the **live URL** (not localhost):

- [ ] All images load (no broken icons)
- [ ] Fonts look correct (not falling back to Times New Roman or Arial)
- [ ] Submit the contact form with test data — check that the submission appears in your Netlify Forms dashboard or Formspree inbox
- [ ] Open the URL on your phone — check that the layout, navigation, and text look good
- [ ] The URL bar shows a lock icon (HTTPS)
- [ ] The site loads in under 3 seconds
- [ ] Social sharing preview looks right — paste your URL into [opengraph.xyz](https://opengraph.xyz) to check the preview image and description
- [ ] Update your Google Business Profile with the new website URL and the GBP description Claude generated

If anything looks wrong, tell Claude and it'll fix it. See `troubleshooting.md` if you're stuck.

### Connect Your Domain

To use your custom domain (www.yourshop.com):
1. In Netlify, go to your site's **Domain settings**
2. Click **Add custom domain**
3. Follow the instructions — if you bought your domain through Netlify, it's automatic. If through another provider, you'll need to update DNS records (Claude can help you with this).

---

## You're Live

Your website is on the internet. A few things to do now:

- Share the URL with customers
- Add it to your Google Business Profile (use the GBP description Claude generated)
- Put it on your business cards and social media

When you need to make changes, see `updating-your-site.md`. If something goes wrong, see `troubleshooting.md`.

**Closing Claude Code?** No worries — next time you open this folder, say "Where did I leave off?" and Claude will read your pipeline status to pick up right where you stopped.

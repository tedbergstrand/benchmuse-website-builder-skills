# Troubleshooting & Error Recovery

Things go wrong sometimes. Here's how to fix the most common issues.

---

## "I closed Claude Code and forgot where I left off"

Just open the toolkit folder in Claude Code and say anything — "hi", "I'm back", "where was I?" — Claude automatically checks your progress files and asks you to confirm where you left off before continuing.

If you want to be explicit, you can say: *"I'm working on my website — where did I leave off?"* But you don't have to. Claude will find it either way.

---

## My profile file is broken (JSON error)

If Claude reports a JSON syntax error in `luthier-profile.json`:

1. **Don't panic** — your data isn't lost, it just has a formatting issue
2. Tell Claude: *"My profile has a JSON error. Can you fix it?"*
3. Claude will read the file, find the syntax issue (usually a missing comma or bracket), and fix it
4. If the file is severely corrupted, Claude can re-create it from the information in your conversation history. You may need to re-answer a few questions.

**Prevention:** Don't edit `luthier-profile.json` by hand unless you know JSON syntax. Let Claude handle it.

---

## My site looks different on Netlify than locally

Common causes:

**Images not loading:**
- Check that all image paths use relative paths (e.g., `assets/hero_01.jpg`), not absolute paths (e.g., `/Users/yourname/...`)
- Verify the images are inside the `website/` folder you dragged to Netlify

**Fonts not rendering:**
- Google Fonts require an internet connection. They should work on Netlify but won't work if you opened the HTML file directly with `file://` locally
- Check that the `@import url(...)` for Google Fonts is present in your CSS

**Layout looks broken:**
- Clear your browser cache (Cmd+Shift+R on Mac, Ctrl+Shift+R on Windows)
- Check that all CSS files are included in the `website/` folder

---

## My contact form doesn't work

**Using Netlify Forms:**
- The form must have the `netlify` attribute: `<form name="contact" method="POST" netlify>`
- Submissions appear in your Netlify dashboard under **Forms** (not your email, unless you set up notifications)
- Forms only work on Netlify — they won't submit when testing locally

**Using Formspree:**
- Verify your form's `action` URL matches your Formspree endpoint
- Check that you've confirmed your email address in Formspree
- Free tier allows 50 submissions/month

**Form works locally but not on Netlify (or vice versa):**
- Netlify Forms only activate after deployment. Test on the live site, not locally.
- If switching from Formspree to Netlify Forms (or vice versa), tell Claude and it will update the form HTML.

---

## I accidentally deleted my website folder

If you deleted the `website/` directory:

1. **Check your trash/recycle bin** — the folder may still be recoverable
2. If it's gone, tell Claude: *"I need to rebuild my site. My profile and design brief are still intact."*
3. Claude will re-run the site builder using your existing profile and curated assets (if the assets were backed up or are still in your original photos folder)
4. Run `/local-footprint-optimizer` again after rebuilding

**Prevention:** Consider keeping a backup copy of your `website/` folder after each successful deploy.

---

## I want to start over completely

If you want to scrap everything and start fresh:

1. Delete `luthier-profile.json` and `pipeline-status.json`
2. Delete the `website/` directory
3. Delete the `handoffs/` folder
4. Type `/luthier-interviewer` to start from scratch

Your original photos and the toolkit's skills/docs/templates are not affected.

---

## Images are loading slowly

Your images may be too large. Phone photos can be 3-12MB each.

1. Tell Claude: *"My site is loading slowly. Can you check the image sizes?"*
2. Claude will audit the assets directory and resize any oversized images
3. Redeploy to Netlify after optimization

**Target sizes:** Hero images under 400KB, gallery images under 200KB.

---

## I need to change my site's design direction

For small tweaks (colors, fonts, spacing):
- Tell Claude what to change directly. No need to re-run the full pipeline.

For a major redesign:
1. Run `/visual-vibe-translator` again with new references or direction
2. Run `/luthier-site-builder` to rebuild with the new design brief
3. Run `/local-footprint-optimizer` to update SEO
4. Redeploy to Netlify

---

## Something else is wrong

Open the toolkit folder in Claude Code and describe the problem. Claude can diagnose most issues by reading your project files and the browser's error console. If Claude can't fix it, your site is standard HTML/CSS/JS — any web developer can help.

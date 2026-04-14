# Updating Your Site

Once your site is live, you can make changes any time by opening this project folder in Claude Code and telling Claude what you want.

## How It Works

1. Open the toolkit folder in Claude Code
2. Tell Claude what to change
3. Claude updates your files
4. Preview the changes locally (Claude starts a preview server at `http://localhost:8000`)
5. Drag the updated `website/` folder to Netlify to redeploy

**Coming back after a break?** Just open the toolkit folder in Claude Code and say anything — Claude automatically checks your progress files and confirms where you left off before making any changes.

## Common Changes

**Pricing:**
> "Change my setup price from $85 to $95"
> "Add a new service: Plek machine leveling, starting at $200"

**Hours and Policies:**
> "Update my hours — I'm closed on Mondays now"
> "Change my booking policy to appointment-only, no walk-ins"

**Photos:**
> "Replace the hero image with this new photo" (drop the photo in)
> "Add these three guitars to the portfolio gallery"

Note: New photos added after the initial build may need resizing for the web. Claude will handle this — just drop in your originals (HEIC format from iPhone is fine).

**Content:**
> "I got my Taylor Gold certification — add that to the about page"
> "Add a testimonial from Mike R.: 'Best fretwork in the state'"

**Services:**
> "I stopped doing amp repairs — remove that from the services page"
> "Add a section about my custom nut and saddle work"

## After Making Changes

After Claude rebuilds your site:

1. **Preview locally** — Claude starts a server so you can check the changes in your browser
2. **Re-run SEO if needed** — Type `/local-footprint-optimizer` if you changed services, pricing, hours, or contact info. This keeps your Google search results and schema markup accurate.
3. **Redeploy** — Log into [Netlify](https://app.netlify.com), go to your site, click **Deploys**, then drag your updated `website/` folder onto the upload area

The changes go live in about 30 seconds.

4. **Verify on the live site** — Check that images load, fonts render, and your contact form still works on the live URL (not just localhost)

## How Often Should You Update?

There's no schedule — update when things change. Most shops update a few times a year:
- New pricing
- New portfolio photos
- Changed hours or policies
- New certifications or services

## Tips

- You don't need to re-run the full 5-step pipeline for small changes. Just tell Claude what to update and it'll edit the relevant files directly.
- For big changes (new branding, completely different design direction), you may want to re-run `/visual-vibe-translator` and rebuild. See `troubleshooting.md` for guidance on major redesigns.
- Your `luthier-profile.json` is the source of truth. Claude reads it before making changes, so everything stays consistent.
- If something breaks after an update, see `troubleshooting.md` for common fixes.

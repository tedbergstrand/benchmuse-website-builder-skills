# Frequently Asked Questions

## Cost

**How much does this cost?**
- **Claude Code:** Requires a Claude Pro ($20/month) or Max ($100/month) subscription. Pro is enough for most sites.
- **Hosting:** Free on Netlify for typical small business traffic. You'll likely never pay a hosting bill.
- **Domain name:** About $15/year if you want a custom `.com` address (e.g., www.yourshop.com).
- **Total:** About $20/month for Claude while you're building, then ~$15/year ongoing for just the domain.

**Is there a monthly fee after my site is built?**
No. Once your site is built and deployed, there's no ongoing cost beyond your domain name. You only need Claude Code when you want to make changes.

**Why is this cheaper than Squarespace/Wix?**
Those platforms charge $16-46/month because they host your site AND provide the editor. This toolkit separates those concerns — Netlify hosts for free, and Claude Code is your editor (only when you need it).

## Hosting

**What is Netlify?**
A hosting platform that serves your website to visitors. It's fast, reliable, and free for small sites. Big companies use it too.

**What if my site gets a lot of traffic?**
Netlify's free tier handles up to 100GB of bandwidth per month — that's roughly 50,000-100,000 page views. If you exceed that (which would be unusual for a repair shop), Netlify charges $19/month for more bandwidth.

**Can I use something other than Netlify?**
Yes. Your site is standard HTML/CSS/JS — it works on any hosting platform. Netlify is recommended because it's the easiest to set up and has a generous free tier.

## Technical

**Do I need to know how to code?**
No. You talk to Claude in plain English. Claude writes all the code.

**Do I need to install anything besides Claude Code?**
For most sites, no. Claude builds vanilla HTML/CSS/JS sites that don't require any build tools. If your site needs advanced interactivity (rare), Claude may ask you to install Node.js. See Step 6 in `getting-started.md` for installation instructions.

**What if something breaks?**
Open the project folder in Claude Code and describe the problem. Claude can diagnose and fix most issues. If you're truly stuck, you can zip up the project folder and send it to any web developer — there's nothing proprietary about the code.

**Can I edit the code myself?**
Absolutely. It's standard HTML, CSS, and JavaScript. If you know (or want to learn) web development, you can edit anything directly.

## Content

**How do I update my site after it's built?**
Open the project folder in Claude Code, tell Claude what to change, then redeploy to Netlify. See `updating-your-site.md` for details.

**Can I add a blog?**
Yes, but it requires manual updates through Claude Code each time you write a post. If you want a regularly updated blog, a platform like WordPress might be a better fit for that specific need. Your main site can link to an external blog.

**Can I sell products on my site?**
Yes, through Stripe Payment Links or Shopify Buy Buttons. These let you sell strings, merch, gift cards, etc. without handling payment data on your site. Claude can set this up for you.

**What about customer intake forms?**
Your site includes a contact/intake form by default. Claude chooses the best form backend for your setup:
- **Netlify Forms** (if hosting on Netlify): No setup needed — just deploy and submissions appear in your Netlify dashboard. Set up email notifications in Netlify to get alerted.
- **Formspree** (works with any host): Requires a free account at [formspree.io](https://formspree.io). Free tier handles 50 submissions/month.

File uploads for damage photos are supported with either option.

## Ownership

**Who owns my website?**
You do. 100% of the code, design, images, and content. There's no license, no lock-in, no fine print.

**What if I want to switch to a different platform later?**
Take your code and go. It's standard web technology that any developer can work with. Your `luthier-profile.json` contains all your business data in a portable format.

**What if the person who helped me set this up disappears?**
You have the complete project folder. Any developer (or you, with Claude Code) can pick up right where things left off. There's nothing hidden or proprietary.

## Troubleshooting

**My site looks broken after deploying to Netlify**
Usually an image path issue. See `docs/troubleshooting.md` for a full diagnosis guide.

**My contact form doesn't submit**
If using Netlify Forms, submissions appear in the Netlify dashboard (not your email by default). If using Formspree, check that your endpoint URL is correct. See `docs/troubleshooting.md` for details.

**I closed Claude Code and lost my place**
Just open the toolkit folder in Claude Code and say anything — "hi", "I'm back", "where was I?" Claude automatically checks your progress files and confirms where you left off before continuing. You don't need to remember a specific phrase.

**My photos look pixelated or huge**
The photo curator optimizes images automatically, but if you added photos after the curation step, they may not be optimized. Tell Claude: "Can you check the image sizes in my assets folder?"

**For more help:** See the full troubleshooting guide at `docs/troubleshooting.md`.

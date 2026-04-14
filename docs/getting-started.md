# Getting Started

Everything you need to set up before building your website.

## Step 1: Get Claude Code

Claude Code is the AI assistant that builds your site. You talk to it, it writes the code.

**Choose one:**

- **Desktop App (recommended)** — Download from [claude.ai/code](https://claude.ai/code). Works on Mac and Windows.
- **Web App** — Use directly in your browser at [claude.ai/code](https://claude.ai/code). No download needed.

You'll need a Claude Pro ($20/month) or Max ($100/month) subscription to use Claude Code. Pro is enough for most sites. You only need the subscription while actively building or updating — cancel anytime between. Sign up at [claude.ai](https://claude.ai).

## Step 2: Download This Toolkit

Download the toolkit folder to your computer. Put it somewhere easy to find — your Desktop or Documents folder works fine.

## Step 3: Open the Toolkit in Claude Code

- **Desktop App:** Open Claude Code, then open the toolkit folder as your project.
- **Web App:** Navigate to the toolkit folder when prompted.

You should see the files listed — `CLAUDE.md`, `README.md`, the `docs/` folder, etc. If you see those, you're in the right place.

## Step 4: Create Your Free Netlify Account

Netlify is where your website will live on the internet. It's free for small business websites.

1. Go to [netlify.com](https://app.netlify.com/signup)
2. Click **Sign Up** (use your Email or Google account)
3. If asked for a team name, use your shop name (e.g., "Smith Guitar Repair")
4. Add a payment method under **Team Settings > Billing** — your bill will almost certainly be $0/month, but Netlify requires a card on file

## Step 5: Your Domain Name (www.yourshop.com)

You have two options:

**Option A: Buy through Netlify (easiest)**
From your Netlify dashboard, search for and purchase a domain. Netlify handles all the technical setup automatically. Usually about $15/year.

**Option B: You already own a domain**
If you bought a domain from GoDaddy, Namecheap, Google, etc., you can point it to your Netlify site. When you're ready to deploy, Claude can help you set up the DNS records.

## Step 6: Node.js (Only If Needed)

Most sites don't need this. Claude builds vanilla HTML/CSS/JS sites by default, which require zero extra software.

If Claude recommends a React/Vite build (rare — only for sites with complex interactivity), you'll need Node.js:

1. Go to [nodejs.org](https://nodejs.org)
2. Download the **LTS** version (the green button)
3. Run the installer — accept all defaults
4. Verify by opening Terminal (Mac) or Command Prompt (Windows) and typing: `node --version`
5. If you see a version number (e.g., `v20.11.0`), you're set

Claude will tell you if Node.js is needed before starting the build. If it doesn't mention it, you don't need it.

## You're Ready

With Claude Code installed and a Netlify account created, you're ready to build.

**Next:** Prepare your materials using the checklist in `what-to-prepare.md` (even 5 photos and a service list is enough to start), then head to `your-first-site.md` for the step-by-step walkthrough.

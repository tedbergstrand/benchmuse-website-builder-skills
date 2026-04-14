# Getting Started

Everything you need to set up before building your website.

## Step 1: Get Claude Code

Claude Code is the AI assistant that builds your site. You talk to it, it writes the code.

**Choose one:**

- **Desktop App (recommended)** — Download from [claude.ai/code](https://claude.ai/code). Works on Mac and Windows.
- **Web App** — Use directly in your browser at [claude.ai/code](https://claude.ai/code). No download needed.

You'll need a Claude Pro ($20/month) or Max ($100/month) subscription to use Claude Code. Pro is enough for most sites. You only need the subscription while actively building or updating — cancel anytime between. Sign up at [claude.ai](https://claude.ai).

## Step 2: Get This Toolkit Onto Your Computer

You need the toolkit files living in a folder on your machine. There are three ways to do this. Pick whichever sounds least scary — they all end up with the same files.

### The easiest way: download a ZIP (no account needed)

1. Go to the toolkit's GitHub page: **[github.com/tedbergstrand/benchmuse-website-builder-skills](https://github.com/tedbergstrand/benchmuse-website-builder-skills)**
2. Look for a **green `< > Code` button** near the top of the file list. Click it.
3. A small menu appears. Click **`Download ZIP`** at the bottom.
4. The ZIP downloads to your Downloads folder. Double-click it to unzip — you'll get a folder called something like `benchmuse-website-builder-skills-main`.
5. Drag that folder somewhere you'll remember — your **Desktop** or **Documents** folder is perfect. You can rename it to something friendlier like `my-website-toolkit` if you want.

That's it. Skip to Step 3.

**Heads up about updates:** If the BenchMuse toolkit gets improvements later, you'll need to download the newest ZIP and copy your personal files (your `luthier-profile.json`, the `handoffs/` folder, your `website/` folder) from the old copy into the new one. It works but it's a little fiddly. If you want painless updates, the next method is better.

### The friendly-GUI way: GitHub Desktop

GitHub Desktop is a free app that makes it easy to keep the toolkit updated with one click. No command line, no typing commands. Recommended if you think you'll update the toolkit more than once.

1. Go to **[desktop.github.com](https://desktop.github.com)** and download GitHub Desktop for your operating system.
2. Install and open it.
3. It'll ask you to sign in with a **GitHub account** — create one if you don't have one. It's free and takes 30 seconds.
4. Once signed in, go to **File → Clone Repository → URL**.
5. In the URL field, paste this:
   ```
   https://github.com/tedbergstrand/benchmuse-website-builder-skills
   ```
6. Choose where to save the folder (your **Documents** folder is fine), then click **Clone**.

You now have the toolkit on your machine.

**Getting updates later:** When there's a newer version, open GitHub Desktop, click **`Fetch origin`** (top of the window), then **`Pull origin`**. Your personal data stays put — only the BenchMuse files update.

### The command-line way (if that's already your thing)

If you're comfortable with a terminal:

```bash
git clone https://github.com/tedbergstrand/benchmuse-website-builder-skills.git
cd benchmuse-website-builder-skills
```

Update with `git pull` from inside the folder.

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

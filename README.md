# Wealth Hack Factory — Website

A clean, responsive one-page website for the Wealth Hack Factory YouTube channel.

## What's inside

- **`index.html`** — the entire site in a single self-contained file
  - Hero section with animated chart bars
  - About section with drop cap typography
  - Featured videos grid (3 cards with custom SVG thumbnails)
  - Email signup form
  - Footer with links

The site is fully mobile-responsive and uses no external dependencies except Google Fonts.

---

## 🚀 Deploy to GitHub Pages — Free in 5 minutes

GitHub Pages will host your site at `https://<your-username>.github.io/wealth-hack-factory/` for free, forever.

### Step 1 — Create a GitHub account
If you don't already have one, sign up at [github.com](https://github.com). It's free.

### Step 2 — Create a new repository
1. Click the **+** button in the top-right corner of GitHub → **New repository**
2. Repository name: `wealth-hack-factory` (or anything you like)
3. Make it **Public** (required for free GitHub Pages)
4. Tick **"Add a README file"**
5. Click **Create repository**

### Step 3 — Upload `index.html`
1. On your new repo's page, click **Add file** → **Upload files**
2. Drag `index.html` (and this `README.md`) into the upload area
3. Scroll down, write a commit message like *"initial site"*
4. Click **Commit changes**

### Step 4 — Enable GitHub Pages
1. In your repo, click the **Settings** tab (top-right of the repo navigation)
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Under **Branch**, select **main** and **/ (root)**
5. Click **Save**

### Step 5 — Visit your site
Wait 30-60 seconds, then refresh the Pages settings screen. You'll see:

> ✅ Your site is live at `https://<your-username>.github.io/wealth-hack-factory/`

That URL is now your live website. Share it on YouTube, in your video descriptions, on Twitter, anywhere.

---

## 🛠️ Customising the site

Open `index.html` in any text editor (VS Code, Notepad, TextEdit). Everything is in one file — HTML, CSS, and JavaScript.

### Update YouTube link
Find and replace `https://youtube.com/@wealthhackfactory` with your actual channel URL (do this everywhere it appears — there are 5 instances).

### Update video cards
Search for `<!-- VIDEO 1 -->` in the file. Each video block has:
- A title in the `<h3 class="video-title">`
- A category and duration in `<div class="video-meta">`
- A clickable link wrapper — replace `https://youtube.com/@wealthhackfactory` with the actual video URL once you've published

To use real YouTube thumbnails instead of the SVG ones, replace the `<svg>` block inside `.video-thumb` with:
```html
<img src="https://img.youtube.com/vi/VIDEO_ID/maxresdefault.jpg" alt="" style="width:100%;height:100%;object-fit:cover;">
```
(replace `VIDEO_ID` with the actual ID from your YouTube URL — the bit after `?v=`)

### Connect the email signup to a real provider
The form currently shows a confirmation message but doesn't actually send the email anywhere. To collect real subscribers, sign up for one of these (all have free tiers):

- **Beehiiv** — best for a newsletter, great free tier ([beehiiv.com](https://beehiiv.com))
- **ConvertKit / Kit** — popular with creators ([kit.com](https://kit.com))
- **Mailchimp** — free up to 500 contacts ([mailchimp.com](https://mailchimp.com))

Each will give you an embed code. In `index.html`, find the comment `// TODO: Replace this block with your real form provider` and swap the form action with your provider's endpoint, OR replace the entire `<form>` block with the embed they give you.

### Custom domain (optional)
Once the site is live, you can buy a domain like `wealthhackfactory.com` from Namecheap, Google Domains, or Cloudflare for $10-15/year, then point it to your GitHub Pages site. GitHub has [step-by-step docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

---

## 📁 File structure

```
wealth-hack-factory/
├── index.html       ← your entire site
└── README.md        ← this file
```

That's it. No build step, no npm, no servers — just one HTML file you can edit in any text editor.

---

## 🎨 Design notes

- **Fonts:** Fraunces (editorial serif) + DM Sans (modern sans)
- **Palette:** Deep navy `#0a0e1a` · Gold `#d4a017` · Emerald `#00c853` · Bone `#f5f1e8`
- **Style:** Editorial financial publication — Bloomberg-meets-luxury-magazine aesthetic
- **Mobile breakpoints:** `900px` (tablet) and `480px` (small phone)

Made for Wealth Hack Factory. Engineering wealth, one video at a time.

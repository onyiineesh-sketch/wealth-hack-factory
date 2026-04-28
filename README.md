# Wealth Hack Factory — Website (v2)

A modern, conversion-focused, single-file storefront for the Wealth Hack Factory YouTube channel. Built around one product line: digital tools (PDFs, Notion templates, sheets) that pair with each video.

> **Tagline:** Engineer your wealth. One habit at a time.

## What's inside

- **`index.html`** — the entire site (HTML + CSS + JS) in a single self-contained file
  - Sticky glass nav with scroll state
  - Hero with animated wealth-OS card (live SVG chart, stats, status floater)
  - Auto-scrolling brand marquee
  - Flagship product banner ("The Wealth Mindset Playbook")
  - 6-card digital-products grid (tracker, workbook, sheet, newsletter, bundle, coaching call)
  - Latest YouTube video block (linked to the channel)
  - Founder/about section with editorial drop cap
  - 3-card testimonials grid
  - Free lead-magnet email capture (Sunday Letter + 7-day reset PDF)
  - 6-question accordion FAQ
  - 4-column footer with social icons
- **`README.md`** — this file

No build step, no npm, no servers — just one HTML file you can edit in any text editor.

## Design system

| Token | Value | Notes |
|---|---|---|
| Ink (background) | `#060912` | Deepest base |
| Navy | `#0a0e1a` / `#0f1424` / `#161c30` | Card layers |
| Bone | `#f5f1e8` | Body text |
| Gold | `#d4a017` / `#f0c14b` | Primary accent |
| Emerald | `#00c853` / `#1de982` | "Up" / success |
| Muted | `#8b8f9c` | Secondary text |
| Display | Fraunces (serif) | Headlines, prices |
| UI | DM Sans | Body, buttons |
| Data | JetBrains Mono | Stats, eyebrows |

Aesthetic: editorial fintech / luxury wealth magazine — Bloomberg meets Robinhood.

## Deploy to GitHub Pages — Free

GitHub Pages will host the site at `https://<your-username>.github.io/wealth-hack-factory/` for free.

1. Push this repo to GitHub (or commit on top of the existing `wealth-hack-factory` repo).
2. In the repo, click **Settings → Pages**.
3. Under **Source**, select **Deploy from a branch**, then pick `main` and `/ (root)`.
4. Click **Save**. Wait 30–60s, refresh — your site is live.

## Customising the site

Open `index.html` in any editor. Everything below is plain HTML + CSS + JS, no frameworks.

### 1. Wire your real product checkout URLs

Each product CTA in the shop has a placeholder `href="#"` and a `data-cta="..."` marker. Search for these and replace `#` with your storefront URL (Gumroad, Stripe Payment Link, Lemon Squeezy, Podia, etc.):

```
data-cta="flagship"   → The Wealth Mindset Playbook
data-cta="tracker"    → 5 Daily Habits Tracker
data-cta="workbook"   → Money Story Rewrite Workbook
data-cta="sheet"      → Net Worth Compounder
data-cta="bundle"     → The Wealth Operating System bundle
data-cta="coaching"   → Mindset Audit Call
```

### 2. Hook up the email signup

The form (`#signup`) currently shows a friendly confirmation message but doesn't store emails. To collect real subscribers, sign up for one of these (all free tiers):

- **Beehiiv** — best for newsletters · [beehiiv.com](https://www.beehiiv.com)
- **Kit (ConvertKit)** — popular with creators · [kit.com](https://kit.com)
- **Mailchimp** — free up to 500 contacts · [mailchimp.com](https://mailchimp.com)

In `index.html`, find the `// TODO: Replace this with your real provider's submission endpoint or embed.` comment, and either:

- Set the `<form>`'s `action` to your provider's POST endpoint, or
- Replace the entire `<form id="signup">` block with the provider's embed snippet.

### 3. Update YouTube links

Find and replace `https://www.youtube.com/@WealthHackFactory` with your live channel URL (or specific video URLs) — there are several instances in the file.

### 4. Update copy & products

Each product card has a `<h3>` title, a `<p>` description, a `.price` block, and a `.pill` category tag. Edit them in place. To add or remove a card, copy a `<article class="card-product">…</article>` block.

### 5. Custom domain (optional)

Buy a domain (Namecheap / Cloudflare / Google Domains, ~$10–15/year), point it at GitHub Pages. GitHub has step-by-step docs.

## File structure

```
wealth-hack-factory/
├── index.html   ← the entire site
└── README.md    ← this file
```

That's it.

---

Made for **Wealth Hack Factory**. Engineering wealth, one habit at a time.

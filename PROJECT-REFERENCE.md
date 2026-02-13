# Elite Signals Docs - Project Reference

## Overview
Knowledge base migrated from Crisp Chat to MkDocs Material theme, hosted on GitHub Pages.

## Live Site
- **URL:** https://docs.elitesignals.com
- **GitHub Repo:** https://github.com/myelitesignals/docs

## Tech Stack
- **Static Site Generator:** MkDocs with Material theme (v9.7.1)
- **Hosting:** GitHub Pages (free)
- **CI/CD:** GitHub Actions (auto-deploys on push to `main`)
- **DNS:** GoHighLevel (CNAME: `docs` -> `myelitesignals.github.io`)

## Brand Colors
- Background: `#171717`
- Accent (lime green): `#CBFB45`
- Nav background: `rgba(27, 29, 32, 0.95)`
- Text primary: white
- Text secondary: `#8B8B8B`
- Link: `#10A5FF`
- Font: Inter (text), JetBrains Mono (code)

## Project Structure
```
elite-signals-docs/
├── .github/workflows/deploy.yml    # GitHub Actions auto-deploy
├── docs/
│   ├── assets/
│   │   ├── logo.png                # Green bull/chart icon
│   │   └── favicon.png
│   ├── stylesheets/
│   │   └── extra.css               # Custom branding CSS
│   ├── getting-started/            # 4 articles
│   │   ├── elitealgo-course-full-setup.md
│   │   ├── trend-sniper-strategy.md
│   │   ├── supply-demand-signals-strategy.md
│   │   └── elite-price-action-concepts-strategy.md
│   ├── faq/                        # 18 articles
│   │   ├── what-is-elite-signals.md
│   │   ├── what-is-elitealgo.md
│   │   ├── what-is-tradingview.md
│   │   ├── how-to-get-elitealgo.md
│   │   ├── what-do-i-need-to-use-elitealgo.md
│   │   ├── why-join-discord-for-elitealgo.md
│   │   ├── how-do-i-download-discord.md
│   │   ├── can-i-cancel-and-how.md
│   │   ├── refund-policy.md
│   │   ├── markets-and-timeframes.md
│   │   ├── does-elitealgo-repaint.md
│   │   ├── do-i-need-tradingview-account.md
│   │   ├── do-i-need-tradingview-pro.md
│   │   ├── is-elitealgo-beginner-friendly.md
│   │   ├── can-i-use-on-metatrader.md
│   │   ├── free-trial.md
│   │   ├── invite-only-scripts.md
│   │   └── how-long-for-access.md
│   ├── index.md                    # Homepage with hero + category cards
│   └── CNAME                       # Custom domain config
├── overrides/
│   └── main.html                   # Jinja2 template with extra meta tags
├── mkdocs.yml                      # Main config file
└── .gitignore
```

## How to Edit Articles
1. Edit markdown files in `docs/` folder
2. Commit and push to `main` branch
3. GitHub Actions auto-builds and deploys in ~20 seconds

## How to Add a New Article
1. Create a new `.md` file in the appropriate folder (`docs/getting-started/` or `docs/faq/`)
2. Add the article to the `nav` section in `mkdocs.yml`
3. Commit and push

## How to Preview Locally
```bash
cd elite-signals-docs
pip install mkdocs-material
mkdocs serve
# Open http://127.0.0.1:8000
```

## DNS Configuration (GoHighLevel)
- **Domain:** elitesignals.com (Internal Domain in GHL)
- **CNAME Record:** `docs` -> `myelitesignals.github.io` (TTL: 1 min)
- **Location:** Settings > Domains & URL Redirects > elitesignals.com > DNS records

## GitHub Pages Configuration
- **Branch:** gh-pages / (root)
- **Custom Domain:** docs.elitesignals.com
- **Enforce HTTPS:** Enabled
- **Deploy Workflow:** `.github/workflows/deploy.yml`

## Git Config (for this repo)
- **User:** Elite Signals
- **Email:** support@elitesignals.com
- **Org:** myelitesignals

## Key Files to Know
- `mkdocs.yml` - Site config, navigation, theme settings
- `docs/stylesheets/extra.css` - All custom branding/CSS
- `docs/index.md` - Homepage content
- `.github/workflows/deploy.yml` - CI/CD pipeline

## Migration Date
February 13, 2026 - Migrated from Crisp Chat (custom.crisp.help) to GitHub Pages

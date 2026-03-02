# POML Lab Website (GitHub Pages)

This repository is configured for a **database-free** GitHub Pages website using Markdown/YAML content files.

## Why Home was redirecting to your personal site
For a project site (`https://mingyukim87.github.io/POML/`), `baseurl` must be set to `/POML`.
If `baseurl` is empty, `Home` can point to `/` and open `https://mingyukim87.github.io/` (your personal page).

## Required config (already set)
- `url: "https://mingyukim87.github.io"`
- `baseurl: "/POML"`

## Operate with `gh-pages` branch (recommended)
This repo includes `.github/workflows/deploy-gh-pages.yml`.

### One-time GitHub settings
1. Go to **Settings → Pages**.
2. Set **Source** to **Deploy from a branch**.
3. Select **Branch: `gh-pages`** and **Folder: `/ (root)`**.
4. Save.

### Daily workflow
1. Edit content in `main` branch.
2. Push to `main`.
3. GitHub Action auto-syncs site files to `gh-pages`.
4. Pages serves from `gh-pages`, so it does not conflict with your personal root page.

## Content management (manual admin)
Update these folders and push commits:
- `_people/`
- `_publications/`
- `_news/`
- `_gallery/`

## Logo
Add your logo image at:
- `assets/images/logo.png`

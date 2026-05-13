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

## Admin operation (not shown in website nav)
This project intentionally does **not** expose an Admin menu/page on the website.
Management is done directly in repository files:

- `_people/` → members
- `_publications/` → publications
- `_news/` → news
- `_gallery/` → gallery images

### Member format (OSI-style card)
Use this template in `_people/your-name.md`:

```yaml
---
name: Your Name
role: Faculty
position: Assistant Professor
order: 1
email: your-email@example.com
keywords:
  - Keyword 1
  - Keyword 2
  - Keyword 3
webpage: "https://your-webpage"
photo: "/assets/images/people/your-photo.jpg"
---
```

- `keywords` are shown in small font tags (max 3 on card).
- If `webpage` exists, a **Webpage** link is shown.

## Add your photo
1. Put image file in `assets/images/people/` (example: `mingyu-kim.jpg`).
2. Set `photo: "/assets/images/people/mingyu-kim.jpg"` in `_people/mingyu-kim.md`.

## Logo
Add your logo image at:
- `assets/images/logo.png`

## Local build / error troubleshooting
If GitHub Pages build logs stop during `Reading:` or local `jekyll` commands fail, use Bundler with the repository Gemfile:

1. `bundle install`
2. `bundle exec jekyll build`
3. `bundle exec jekyll serve --livereload`

This repo now includes a `Gemfile` pinned to the GitHub Pages gem set (`github-pages` v232-compatible), which matches the build stack shown in Pages logs.

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Site Is

A Jekyll-based workshop website for a UbiComp workshop on health-centric wearable devices, hosted on GitHub Pages at `health-wearables-ubicomp.github.io`. Built on the [al-folio](https://github.com/alshedivat/al-folio) academic theme.

## Development Commands

```bash
# Start local dev server (recommended)
docker compose pull && docker compose up
# Site runs at http://localhost:8080

# Rebuild after Gemfile/Dockerfile changes
docker compose up --build

# Stop server and free port 8080
docker compose down

# Format code before committing (mandatory)
npx prettier . --write
```

No `npm run dev` — `package.json` only contains Prettier. This is a Ruby/Jekyll site.

## Pre-Commit Requirements

Both steps are required before pushing:

1. Run `npx prettier . --write` (CI will fail PRs with unformatted code)
2. Verify the site builds and renders correctly at `http://localhost:8080`

## Architecture

### How Pages Are Built

- `_pages/` — the actual site pages (`about.md`, `cfp.md`, `organizers.md`, `schedule.md`, `workshop.md`)
- `_layouts/` — Liquid templates that pages reference via `layout:` frontmatter
- `_includes/` — reusable Liquid components injected into layouts
- `_sass/` — SCSS styles
- `_config.yml` — single source of truth for all feature flags and site-wide settings

### Configuration Priority

1. `_config.yml` — start here for any site-wide change; feature flags (`enable_darkmode`, `enable_math`, etc.) live here
2. `_data/` — structured content (socials, CV, repos)
3. `_bibliography/papers.bib` — BibTeX publications managed by jekyll-scholar

### url/baseurl Relationship

These two must stay in sync — broken together means CSS/JS won't load:
- `url: health-wearables-ubicomp.github.io`
- `baseurl:` (empty — this is a personal/org site, not a project subpath)

## Common Pitfalls

- **YAML special characters** — quote strings containing `:`, `&`, or `#` in `_config.yml`
- **ImageMagick** — required by `jekyll-imagemagick`; Docker includes it automatically; native installs need `brew install imagemagick`
- **Port conflicts** — if port 8080 is busy: `docker compose down` then `docker compose up`
- **Prettier CI failures** — always run `npx prettier . --write` before pushing; install once with `npm install --save-dev prettier @shopify/prettier-plugin-liquid`

# HackAtlas Slides

Slide deck for the HackAtlas product idea, built with [Slidev](https://sli.dev/).

## What this repo contains

- `slides.md` — main presentation content
- `package.json` — scripts and dependencies
- `.github/workflows/deploy-slides.yml` — auto deploy to GitHub Pages on push to `main`

## Requirements

- Node.js 20+ recommended
- npm

## Run locally

Install dependencies:

```bash
npm install
```

Start dev server:

```bash
npm run dev
```

Build static site:

```bash
npm run build
```

Export to PDF (optional):

```bash
npm run export
```

## Slide metadata (frontmatter)

At the top of `slides.md`, metadata is defined in YAML frontmatter:

```yaml
---
theme: default
title: HackAtlas
info: |
  Mapping the world's top hackathon builders.
class: text-center
transition: slide-left
mdc: true
---
```

Common fields you can edit:

- `theme`: visual theme
- `title`: deck/browser title
- `info`: short deck description
- `class`: default class applied to slides
- `transition`: slide transition style
- `mdc`: enable Markdown components

## Deploy (auto)

This repo uses GitHub Actions to deploy to GitHub Pages automatically.

Trigger:
- Push to `main`

Workflow:
- Install deps
- Build Slidev with repo base path
- Publish `dist/` to GitHub Pages

Make sure your GitHub repo has Pages source set to **GitHub Actions** in Settings → Pages.

## Edit flow

1. Update content in `slides.md`
2. Preview with `npm run dev`
3. Commit and push to `main`
4. Wait for Actions to finish, then view updated Pages site
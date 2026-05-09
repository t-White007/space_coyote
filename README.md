# tyler-site

Personal site — writing, music, projects, tools.

Built with [Astro](https://astro.build), written in Obsidian, deployed on Netlify.

## Stack

- **Astro** — static site generator, zero JS by default
- **Markdown / MDX** — all content lives as `.md` files
- **Netlify** — deploys on every push to `main`
- **IBM Plex Mono + Libre Baskerville** — typographic identity

## Local development

```bash
npm install
npm run dev
```

Open `http://localhost:4321`.

## Content

All content lives in `src/content/`:

| Folder | What goes here |
|--------|----------------|
| `writing/` | Essays, newsletter pieces, long reads |
| `projects/` | Tools and things I've shipped |
| `notes/` | Shorter, rougher thinking |

### Adding a writing post

Create `src/content/writing/your-slug.md`:

```markdown
---
title: "Post title"
date: 2024-01-15
description: "One-sentence description (optional)"
tags: ["tag1", "tag2"]
draft: false
---

Your content here.
```

### Obsidian workflow

Point your Obsidian vault at `src/content/` (or symlink). Write normally. Frontmatter syncs automatically.

## Deployment

Push to `main` → Netlify builds and deploys automatically.

Build command: `npm run build`  
Publish directory: `dist`

## Design principles

- Paper-toned, typographic, raw
- Mono for structure, serif for reading
- Accumulates in public over time — not launched, grown

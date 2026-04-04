# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

OpenWalk (LiteSeed) is a personal technical blog built on [AstroPaper](https://github.com/satnaing/astro-paper). The site is deployed at https://wangyiguo.top/ and records thoughts on technology, efficiency, and minimalism.

## Tech Stack

- **Framework**: Astro 5.x with SSR
- **Styling**: TailwindCSS 4.x (via @tailwindcss/vite)
- **Search**: Pagefind (static search index built at build time)
- **Deployment**: Cloudflare Pages
- **Syntax Highlighting**: Shiki with custom transformers

## Development Commands

```bash
pnpm install      # Install dependencies
pnpm run dev     # Start dev server (http://localhost:4321)
pnpm run build   # Production build + generate search index
pnpm run preview # Preview production build locally
pnpm run format  # Format code with Prettier
pnpm run lint    # Lint with ESLint
pnpm run sync    # Sync Astro types
pnpm run astro   # Run Astro CLI commands
```

## Project Structure

- `src/pages/` - Route pages (index, archives, tags, search, etc.)
- `src/layouts/` - Page layouts (Base, Post, etc.)
- `src/components/` - Astro components (Card, Breadcrumb, etc.)
- `src/content/` - Blog posts (Markdown with frontmatter)
- `src/styles/` - Global styles
- `src/utils/` - Utility functions and transformers
- `src/config.ts` - Site configuration (title, description, author, etc.)

## Content Writing

Articles are stored in `src/content/` as Markdown files with YAML frontmatter. Each article lives in its own folder with images placed inside:

```
src/content/blog/post-title/
├── index.md
└── cover.jpg
```

## Article Sync Workflow

This directory (`4-发表`) is used for writing new articles before they are published. When adding new articles:
1. Review the article for quality and format
2. Place the Markdown file here first
3. Move to `src/content/blog/` after review

## Configuration

Site configuration is centralized in `src/config.ts`:
- `SITE.website` - Deployed domain
- `SITE.author` - Author name
- `SITE.title` - Site title
- `SITE.showArchives` - Show/hide archives page

## Build Output

Production build outputs to `dist/` with Pagefind search index copied to `public/pagefind/`.

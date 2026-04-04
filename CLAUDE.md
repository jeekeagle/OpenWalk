# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository stores blog articles for [OpenWalk](https://github.com/jeekeagle/OpenWalk) — a personal tech blog focused on technology, cognition, and human agency in the AI era. Articles are synchronized to GitHub for publishing.

## Article Format

Articles are written in Markdown with YAML frontmatter:

```yaml
---
title: Article Title
author: Theo
pubDatetime: 2026-04-04T10:00:00.000+08:00
slug: article-slug
featured: true
draft: false
tags:
  - OpenWalk
  - Technology
description: Article description
tableOfContents: true
---
```

## Common Commands

- `git add .` — Stage all new articles
- `git commit -m "message"` — Commit changes
- `git push origin main` — Push to GitHub

## Workflow

When user adds a new article:
1. Review the article for quality and format
2. Stage, commit with descriptive message (e.g., "add: article-title")
3. Push to remote origin

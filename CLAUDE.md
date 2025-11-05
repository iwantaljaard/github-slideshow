# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Jekyll-based slideshow presentation system using reveal.js, designed as a GitHub Learning Lab training repository. The site generates an interactive HTML slideshow from markdown files and deploys to GitHub Pages.

## Development Commands

```bash
# Initial setup - installs Ruby dependencies and git submodules
script/setup

# Run local development server (serves at http://localhost:4000)
bundle exec jekyll serve
# or use the shorthand:
script/server

# Build and test (builds site and runs html-proofer)
script/cibuild

# Build only
bundle exec jekyll build

# Deploy to staging environment (GitHub Enterprise)
script/stage [repo-name]
```

## Architecture

### Content Flow
1. **Slide Creation**: Slides are markdown files in `_posts/` with date-based naming: `0000-01-01-slidename.md`
2. **Jekyll Processing**: Jekyll reads posts in reverse chronological order (controlled by `{% for post in site.posts reversed %}` in index.html)
3. **Rendering**: Each post is wrapped in `_includes/slide.html` which creates a reveal.js `<section>` element
4. **Presentation**: All sections are wrapped in `_layouts/presentation.html` which initializes reveal.js

### Layout System
- **presentation.html** - Main layout that wraps all slides with reveal.js container
- **slide.html** - Individual slide layout (used for single slide views)
- **_includes/slide.html** - Template that renders each post as a `<section>` with title and content

### Adding New Slides
Create a markdown file in `_posts/` with:
```markdown
---
layout: slide
title: "Your Slide Title"
---

Slide content in markdown
```

The filename determines slide order (earlier dates appear first due to reversed loop). Convention is to use year 0000 and increment month/day: `0000-01-01-first.md`, `0000-01-02-second.md`, etc.

### Configuration
- `_config.yml` controls Jekyll settings and reveal.js initialization
- Site baseurl is `/github-slideshow` (configured for GitHub Pages)
- Reveal.js settings (transitions, controls, progress bar, etc.) are in the `reveal:` section
- Theme is configurable via `solarized.theme` (default: dark)

### Key Dependencies
- **reveal.js** - Located in `node_modules/reveal.js/`, handles presentation functionality
- **Jekyll** - Static site generator (via github-pages gem)
- **html-proofer** - Tests built HTML for validity

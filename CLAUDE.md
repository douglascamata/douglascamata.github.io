# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo static site using the PaperMod theme. The site is configured with `hugo.yaml` and uses Hugo's git submodule approach for theme management (PaperMod theme is in `themes/PaperMod/`).

## Development Commands

### Local Development
- `hugo server` - Start local development server with live reload
- `hugo server -D` - Start server including draft content
- `hugo server --bind 0.0.0.0` - Start server accessible from other devices

### Content Creation
- `hugo new posts/post-name.md` - Create a new blog post
- `hugo new page-name.md` - Create a new page

### Building
- `hugo` - Build the site for production (outputs to `public/`)
- `hugo --minify` - Build with minification enabled
- `hugo -D` - Build including draft content

### Theme Management
- The PaperMod theme is managed as a git submodule in `themes/PaperMod/`
- `git submodule update --remote themes/PaperMod` - Update theme to latest version

## Architecture

### Content Structure
- `content/` - All markdown content files (currently empty)
- `archetypes/` - Content templates for new posts/pages
- `static/` - Static assets (images, files, etc.)
- `data/` - YAML/JSON data files for the site

### Configuration
- `hugo.yaml` - Main site configuration
- `themes/PaperMod/` - Theme files (git submodule)
- Content uses frontmatter in YAML format with date, title, draft status

### PaperMod Theme Features
- Supports multiple modes: Regular, Home-Info, Profile
- Built-in search functionality with Fuse.js
- Light/dark theme switching
- Social icons and share buttons
- Multilingual support
- SEO optimized
- No build dependencies (webpack, nodejs) required

### Minimum Requirements
- Hugo v0.146.0+ (currently using v0.147.8+extended)
- Git (for submodule management)
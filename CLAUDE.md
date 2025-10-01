# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a presentation slide system built with Reveal.js and Tailwind CSS. Content is authored in Markdown (`slides.md`) and displayed in an HTML presentation (`index.html`). The project is automatically deployed to GitHub Pages when changes are pushed to the main branch.

## Development Commands

### Setup
```bash
# Use Node.js 22 (recommended)
nvm use

# Install dependencies
npm install

# Build Tailwind CSS
npm run build:css
```

### Development Workflow
```bash
# Start development server with live reload (recommended)
npm run dev
# Opens at http://localhost:8000
# Automatically reloads when CSS, HTML, or MD files change

# Or run separately:
npm run watch:css  # Watch CSS changes
npm run serve      # Serve locally
```

## Architecture

### Content Structure
- **slides.md**: Markdown source for all presentation content
  - Horizontal slides separated by `---`
  - Vertical slides separated by `--`
  - Speaker notes prefixed with `Note:`

- **index.html**: Reveal.js presentation container
  - Loads slides.md dynamically via data-markdown attribute
  - Configured with hash navigation, slide numbers, and plugins

### Styling System
- **src/input.css**: Tailwind source with custom Reveal.js overrides
  - Uses @apply directives to style Reveal.js elements (h1-h3, p, ul, code)
  - Compiles to dist/output.css

- **tailwind.config.js**: Scans index.html and slides.md for Tailwind classes

### Deployment
- GitHub Actions workflow (.github/workflows/deploy.yml) automatically:
  1. Installs Node.js 22 and npm dependencies
  2. Builds Tailwind CSS
  3. Deploys to GitHub Pages on push to main

## Key Files
- **slides.md**: Edit presentation content here
- **src/input.css**: Modify slide styling here (requires rebuild)
- **index.html**: Rarely needs editing (Reveal.js configuration only)

## Presentation Controls
- Arrow keys / Space: Navigate slides
- ESC / O: Slide overview
- F: Fullscreen
- S: Speaker notes view

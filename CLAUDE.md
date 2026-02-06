# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Polish-language educational web applications repository, currently containing an interactive Git & GitHub guide. Hosted via GitHub Pages at https://mlynarzpiotr.github.io/GitApp-ClaudeCode/.

## Tech Stack

- Pure HTML, CSS, and vanilla JavaScript — no frameworks, no build tools, no package manager
- Each application lives in its own subfolder with a self-contained `index.html`
- Root `index.html` serves as a redirect/landing page for GitHub Pages

## Architecture

```
index.html              ← GitHub Pages entry point (redirect)
git-guide/index.html    ← Self-contained single-page app (~60KB)
```

Each app is a single HTML file containing all CSS (in `<style>`) and JS (in `<script>`). No external dependencies.

## Design Conventions

- **Language**: All UI text in Polish
- **Theme**: Dark mode, GitHub-inspired color palette using CSS custom properties (`--bg-primary`, `--text-primary`, etc.)
- **Layout**: Sticky navigation, hero section, numbered content sections, responsive design
- **Components**: Accordions, copyable code blocks, info boxes (tip/warning/danger), feature cards grid, cheat sheet grid
- **Approach**: Semantic HTML, no CSS frameworks, minimal vanilla JS for interactivity

## Deployment

- GitHub Pages from `main` branch, root source
- Remote: `https://github.com/mlynarzpiotr/GitApp-ClaudeCode`
- No build step — files are served as-is

## When Adding New Content

- Create a new subfolder with its own `index.html`
- Follow the existing dark theme and CSS variable system
- Keep everything self-contained (no external CDN dependencies)
- Update root `index.html` if navigation between apps is needed

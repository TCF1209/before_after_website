# CLAUDE.md - before_after_website

> **Documentation Version**: 1.0
> **Last Updated**: 2026-03-23
> **Project**: before_after_website
> **Description**: DuoCode Before/After Website Demo — a single-file HTML/CSS/JS showcase with Azure Dragon theme

This file provides essential guidance to Claude Code when working with this repository.

## Project Overview

A **single `index.html` file** (no frameworks, no build tools) that demonstrates a before/after website transformation for **DuoCode Technology**, a Malaysian web development agency. A toggle switches between a deliberately ugly "before" state and a cinematic "after" state featuring an Azure Dragon (青龙) canvas animation.

### Key Technical Details
- **Single file**: Everything lives in `index.html` — HTML, CSS, and JavaScript
- **No dependencies**: Only Google Fonts CDN is allowed as an external resource
- **Toggle mechanism**: CSS class on `<body>` (e.g. `body.after-mode`) controls visual state
- **Canvas animation**: Azure Dragon made of teal/cyan particles with gold accents, 60fps target
- **Brand colors**: Navy `#1B3A5C`, Teal `#00D4AA`, Gold `#FFD700`
- **Target**: Desktop-first (for Instagram Reels screen recording)

### Reference
- Full project brief: `duocode-before-after-brief.md`

## Rules

- Keep everything in `index.html` — do not split into separate CSS/JS files unless explicitly asked
- All animations must be pauseable/removable in Before mode
- Canvas dragon animation must target 60fps
- Both modes share the same HTML structure; switching is CSS class + canvas visibility only
- Desktop-optimized layout is the priority

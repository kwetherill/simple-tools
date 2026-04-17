# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A collection of AI-generated single-page HTML applications, served via GitHub Pages from the `docs/` directory.

## Architecture

- All tools live as standalone `.html` files in `docs/` — each file contains its own HTML, CSS, and JavaScript with no external build step or dependencies beyond optional CDN-loaded libraries.
- `docs/index.html` is the homepage that lists and links to each tool.
- `docs/logins-manager-plugin/` contains a browser plugin (zipped) for a logins manager.
- No bundler, no package manager, no test framework — just static files.

## Adding a New Tool

1. Create `docs/<tool-name>.html` as a self-contained page (inline styles and scripts).
2. Add a link to it in `docs/index.html`.
3. Follow the established visual style: `font-family: 'Segoe UI'`, purple gradient background (`#667eea` → `#764ba2`), white card container with `border-radius: 20px` and `box-shadow`.

## Previewing Locally

Open any `.html` file directly in a browser — no server required. For example:

```
open docs/index.html
```

## Deployment

Pushing to `main` deploys automatically via GitHub Pages (source: `docs/` folder).

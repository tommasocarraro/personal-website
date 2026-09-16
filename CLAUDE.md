# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This repo is a single-file personal/portfolio website for Tommaso Carraro (Applied AI Scientist). The entire site — markup, CSS, and JavaScript — lives in `index.html`. There is no build system, package manager, or test suite; it is meant to be opened/served directly as static HTML.

## Development

There are no build, lint, or test commands — this is plain static HTML/CSS/JS.

- Preview locally by opening `index.html` in a browser, or serving the directory with any static file server (e.g. `python3 -m http.server`).
- Fonts are loaded from Google Fonts (Space Grotesk, Inter) via CDN links in `<head>`.

## Architecture

`index.html` is organized into three inline sections in this order:

1. `<style>` block in `<head>` — all CSS, using custom properties defined on `:root` (colors, fonts, max-width) as design tokens. Sections are separated by comment banners (e.g. "Tokens", "Background field").
2. HTML body — page content/sections.
3. `<script>` block(s) — page behavior (e.g. scroll effects, background animation), inline at the bottom of the file.

When editing styles, prefer reusing/extending the existing `:root` custom properties rather than introducing new hard-coded values.

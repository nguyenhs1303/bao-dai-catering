# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

A single-page static website for **Bảo Đại Catering** — a Vietnamese catering service in Hưng Yên province. The entire site lives in one file: `index.html`.

## Development

No build step, no package manager, no framework. Open `index.html` directly in a browser to preview.

## Architecture

`index.html` is fully self-contained — HTML structure, all CSS (in a `<style>` block in `<head>`), and no JavaScript. Layout uses CSS Grid and custom properties defined in `:root`. External resources are Google Fonts (loaded via `<link>`) and Unsplash placeholder images.

Page sections in order: nav → hero → stats bar → about → services → gallery → process → contact form → footer. Each section has an `id` matching its nav anchor (`#about`, `#services`, `#gallery`, `#process`, `#contact`).

The color palette is defined as CSS variables (`--brown-deep`, `--brown-mid`, `--orange-earth`, `--orange-warm`, `--cream`, `--cream-light`, `--gold`, `--text-dark`, `--text-mid`) — use these when adding or modifying any styled elements.

Responsive breakpoints: `max-width: 900px` (stack grids, hide nav links) and `max-width: 600px` (minor adjustments).

The contact form (`#contact`) is presentational only — it has no backend or form submission handler.

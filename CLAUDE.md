# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A single-page personal portfolio website for Utkarsh Sinha. No build tools, frameworks, or dependencies — everything is self-contained in one file.

## Structure

- `index.html` — the entire site: HTML structure, embedded CSS (`<style>`), and content
- `gabriel-dizzi-WPXxp36tkHQ-unsplash.jpg` — full-viewport background image (grayscale + dark overlay applied via CSS)

## Development

Open `index.html` directly in a browser — no server or build step needed. All styles are in the `<style>` block in `<head>`.

## Layout

- Fixed background image via `body::before` (grayscale filter) + dark overlay via `body::after`
- 1100px max-width container, 28px side padding
- `section:not(#skills)` rule applies a 2-column CSS grid to Education, Experience, Projects, and Outside of Work sections — `#skills` and `#outside` both opt out with `display: block`
- Cards (`.exp-item`, `.proj-item`, `.edu-item`) show a white border on hover via CSS transition
- Responsive breakpoints: 700px (single-column sections, stacked nav) and 540px (single-column skills grid)

## Content conventions

- Experience/project bullets follow the pattern: outcome metric first, method/tool second (one line each)
- Skills and Outside of Work use dot-separated plain text (`·`) — no chips, tags, or icons (except the 😉 on Doomscrolling)
- Section headers use `.section-head`: 13px, uppercase, `letter-spacing: 1.5px`, `rgba(255,255,255,0.4)`

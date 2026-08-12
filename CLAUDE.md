# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is Kyle Bareis's personal website, a static single-page site with no build process, package manager, or test suite. It is deployed via GitHub Pages using the custom domain declared in `CNAME` (bareis.me).

## Development

There are no build, lint, or test commands — this is plain HTML/CSS. To preview changes locally, open `index.html` directly in a browser, or serve the directory with any static file server, e.g.:

    python3 -m http.server

## Structure

- `index.html` — the entire site content (single page: header/nav, intro text, footer). Loads Bootstrap 4.3.1, jQuery, and Popper.js from CDNs (jsdelivr/code.jquery.com) rather than local/bundled copies.
- `css/style.css` — custom overrides layered on top of Bootstrap (dark background, masthead/nav styling, footer styling).
- `CNAME` — GitHub Pages custom domain config; do not remove or this breaks the custom domain routing.

Since everything lives in one HTML file with no templating, adding content means editing `index.html` directly (e.g., new `<section>`/`<p>` inside `<main class="inner">`, or nav links inside `.nav-masthead`).

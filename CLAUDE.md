# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

James River Ops — a static marketing site for an AI integration consultancy based in Lynchburg, Virginia, serving Central VA businesses.

## Architecture

Plain static site: HTML + CSS, no build tools, no frameworks, no bundler. Files are served as-is.

- `index.html` — Home page (hero, services, CTA)
- `about.html` — About page (company story, values)
- `contact.html` — Contact page (form + contact details)
- `styles.css` — Single shared stylesheet for all pages

Each HTML page includes its own inline `<script>` for the mobile nav toggle. There is no shared JS file.

## Development & Hosting

Static site hosted on GitHub Pages. No build step, no dependencies.

To preview locally, open any `.html` file directly in a browser.

## Design System

Color palette is drawn from the James River corridor and Lynchburg's built environment — defined as CSS custom properties in `:root` at the top of `styles.css`:

| Token       | Hex       | Reference                |
|-------------|-----------|--------------------------|
| `--river`   | `#2e4a62` | Deep James River blue    |
| `--ridge`   | `#3b6e5e` | Blue Ridge green         |
| `--brick`   | `#9e4a3a` | Lynchburg brick red      |
| `--stone`   | `#d6cfc4` | River-stone warm gray    |
| `--fog`     | `#f4f1ec` | Morning fog off-white    |

Typography: Georgia (headings), Inter/system-ui (body). Max content width is 1080px (`--max-w`).

## Key Conventions

- **No AI slop.** Copy is direct, plainspoken, and regionally grounded. Avoid generic tech-marketing language.
- **Minimal by design.** Don't add JS frameworks, CSS preprocessors, or build tooling unless the project scope genuinely demands it.
- Navigation is duplicated in each HTML file — update all three pages when changing nav links.
- The contact form action points to `https://formspree.io/f/YOUR_FORM_ID` — this must be replaced with a real Formspree (or equivalent) endpoint before going live.
- Placeholder email is `hello@jamesriverops.com` — confirm actual contact email before launch.

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Context

This folder is one lesson in a frontend/Python bootcamp repo (`bootcamp-frontend-python-g34-lmv`), laid out as `semanaNN/diaNN-<topic>/`. Each lesson folder stands on its own. This one (week 3, day 3) builds a static landing page in HTML and CSS from a Figma design.

Right now the folder holds only `image.png`, a full-page desktop mockup (1440×2672) of the **"Healthy Recipe Finder"** landing page. It has these sections, top to bottom:

1. Header: logo, nav (Home / About / Recipes, with the active link underlined in orange) and a dark "Browse recipes" button
2. Hero: an h1 "Healthy meals, zero fuss" with an orange highlight behind "Healthy", a subtitle, a "Start exploring" button, a rounded image inside a white frame, and decorative lavender curves at the sides
3. "What you'll get": three feature columns, each with an icon tile, a title and text
4. "Built for real life": a two-column block (text on the left, image on the right) with "30 minutes" highlighted
5. CTA card "Ready to cook smarter?": a light green-gray card with fork and knife shapes and squiggle decorations
6. Footer: "Made with ❤️ and 🥑" and social icons (Instagram, Bluesky, TikTok)

The palette is a cream background, dark green for text and buttons, and orange, teal and lavender accents. Get exact values, fonts and assets from Figma. Don't guess them from the PNG.

## Running

There's no build step, package manager or test suite. Open `index.html` in a browser, or serve the folder with something like VS Code Live Server.

## Conventions from earlier lessons

See `../dia02-css-landing-page/` for the pattern this course follows:

- Files sit flat: `index.html` and `styles.css` in the lesson root, with assets in `images/`.
- Fonts load from Google Fonts with `<link>` tags in `<head>`.
- Classes use **BEM** naming (`.hero`, `.hero__title`, `.header__nav--active`).
- `styles.css` is split into commented sections: `/* GENERALES */` (reset with `* { box-sizing: border-box; margin: 0 }`, base `html`/`body`/`a`/`img`), `/* UTILS */` (`.wrapper`, `.hidden`), then one block per page section (`/* HEADER SECTION */`, `/* HERO SECTION */`, ...).
- Layout is Flexbox-based. Widths are responsive, using `min()`, for example `.wrapper { width: min(100% - 42px, 1440px); }`.
- Spacing uses `rem`, often with a comment showing the px conversion (`/* 42px <> 3rem <> 3 * 14px */`).
- Code comments, TODOs and commit messages are in **Spanish**. Commits follow the form `semanaNN, diaNN, <topic>`.
- Students finish sections marked with `/* TODO: ... */`.

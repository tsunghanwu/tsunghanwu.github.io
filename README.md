# Tsung-Han Wu — Personal Website

Personal website of Tsung-Han Wu, Senior Staff Applications Engineer specializing in semiconductor process modeling, simulation, applied machine learning, and agentic AI.

[Visit the website](https://tsunghanwu.github.io/) · [Connect on LinkedIn](https://linkedin.com/in/tsung-han-wu/)

## Overview

The site presents professional experience at Synopsys and Lam Research, technical expertise, and contact information. Each employer has three visible highlights, with a concise role history that visitors can expand.

Features include:

- Responsive layouts and mobile navigation.
- Light and dark themes that follow the visitor's system setting, with a header toggle that remembers their choice.
- Expandable experience timelines.
- Keyboard focus indicators and a skip-to-content link.
- Reduced-motion support.
- Search and social-sharing metadata, plus structured person data.
- A WebP portrait with a JPEG fallback.
- A lightweight animated mesh background, a grid deformed by an evolving level-set field like a simulation mesh around an etch front, that starts after the page renders, pauses in hidden tabs and is skipped when reduced motion is requested.
- Navigation that highlights the section in view.
- A print layout that expands every role history.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Page content, styles, metadata, and interactive behavior |
| `tailwind.css` | Compiled Tailwind CSS (generated; do not edit by hand) |
| `src/tailwind.css`, `tailwind.config.js`, `package.json` | Tailwind build input and configuration |
| `fonts/` | Self-hosted Inter and Roboto Mono (Latin subset, SIL OFL licenses included) |
| `404.html` | Page shown for unknown URLs |
| `robots.txt`, `sitemap.xml` | Search-engine crawling hints; update `lastmod` when content changes |
| `MyAvatar.webp` | Primary portrait |
| `MyAvatar.jpg` | Portrait fallback |
| `og-image.jpg` | Social-sharing image |
| `favicon.ico`, `favicon-32.png` | Browser icons |
| `apple-touch-icon.png` | Apple touch icon |

## Preview locally

The site uses plain HTML, CSS, and JavaScript. Tailwind CSS is precompiled into `tailwind.css`, icons are inline SVGs, fonts are self-hosted in `fonts/`, and the animated mesh background is drawn on a 2D canvas. Nothing loads from an external service, so the site works offline.

Clone the repository:

```sh
git clone https://github.com/tsunghanwu/tsunghanwu.github.io.git
cd tsunghanwu.github.io
```

With Python 3 installed, serve the repository folder:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

On Windows, use `py -m http.server 8000 --bind 127.0.0.1` if your Python installation uses the `py` launcher.

Open [the local preview](http://127.0.0.1:8000/) in your browser. Stop the server with Ctrl+C.

## Update the content

Edit the corresponding section in `index.html`:

- `#home`: name, headline, introduction, and portrait.
- `#about`: professional summary.
- `#experience`: employer highlights and role histories.
- `#skills`: expertise and tools.
- `#contact`: contact text and LinkedIn link.

Keep experience highlights concise and put supporting detail in the expandable role histories. When editing those controls, preserve the matching `aria-controls`, panel IDs, and `aria-labelledby` attributes.

If your title, profile links, or portrait change, also update the page title, description, social metadata, and structured data in the document head.

## Rebuild the CSS

`tailwind.css` contains only the Tailwind classes used in `index.html`. If you add or change Tailwind classes, rebuild it with [Node.js](https://nodejs.org/) 18 or later:

```sh
npm install
npm run build:css
```

Commit the updated `tailwind.css` with your change. Use `npm run watch:css` to rebuild automatically while editing. A GitHub Actions check fails on pull requests whose `tailwind.css` is out of date. Content-only edits that don't add new classes don't need a rebuild.

## Review changes

Before publishing, preview at desktop and mobile widths. Check navigation, keyboard access, experience expansion and collapse, portrait loading, and contact links. Confirm that dates and outcome metrics match the intended copy.

Use a branch and pull request to review changes before merging into `main`. Check the repository's GitHub Pages settings for the configured publishing source, then verify the deployed website after publication.

## Icons

Interface and section icons are inline SVGs from [Font Awesome Free 6.4.0](https://fontawesome.com/license/free) (icons under CC BY 4.0).

The seven AI and ML badge logos are embedded SVGs from [Simple Icons v16.34.0](https://github.com/simple-icons/simple-icons/tree/16.34.0), distributed under CC0. Codex uses the OpenAI mark, and Claude Code uses the Claude mark. Icons inherit the badge color and are hidden from assistive technology because each badge includes its tool name.

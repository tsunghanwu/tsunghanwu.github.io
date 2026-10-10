# Tsung-Han Wu — Personal Website

Personal website of Tsung-Han Wu, Senior Staff Applications Engineer specializing in semiconductor process modeling, simulation, applied machine learning, and agentic AI.

[Visit the website](https://tsunghanwu.github.io/) · [Connect on LinkedIn](https://linkedin.com/in/tsung-han-wu/)

## Overview

The site presents professional experience at Synopsys and Lam Research, technical expertise, and contact information. Each employer has three visible highlights, with a concise role history that visitors can expand.

Features include:

- Responsive layouts and mobile navigation.
- Expandable experience timelines.
- Keyboard focus indicators and a skip-to-content link.
- Reduced-motion support.
- Search and social-sharing metadata, plus structured person data.
- A WebP portrait with a JPEG fallback.
- An animated wireframe background, skipped when reduced motion is requested.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Page content, styles, metadata, and interactive behavior |
| `MyAvatar.webp` | Primary portrait |
| `MyAvatar.jpg` | Portrait fallback |
| `og-image.jpg` | Social-sharing image |
| `favicon.ico`, `favicon-32.png` | Browser icons |
| `apple-touch-icon.png` | Apple touch icon |

## Preview locally

No build step or package installation is required. The site uses plain HTML, CSS, and JavaScript, with Tailwind CSS, Font Awesome, Google Fonts, and Three.js loaded from external services. An internet connection is needed for those resources.

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

## Review changes

Before publishing, preview at desktop and mobile widths. Check navigation, keyboard access, experience expansion and collapse, portrait loading, and contact links. Confirm that dates and outcome metrics match the intended copy.

Use a branch and pull request to review changes before merging into `main`. Check the repository's GitHub Pages settings for the configured publishing source, then verify the deployed website after publication.

## Skill logos

The six AI and ML badge logos are embedded SVGs from [Simple Icons v16.34.0](https://github.com/simple-icons/simple-icons/tree/16.34.0), distributed under CC0. Codex uses the OpenAI mark. Icons inherit the badge color and are hidden from assistive technology because each badge includes its tool name.

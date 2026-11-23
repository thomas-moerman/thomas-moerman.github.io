# t/m · Thomas Moerman

My personal site: what I offer, notes and a bit about me.

**Live at [thomas-moerman.github.io](https://thomas-moerman.github.io)**

## Writing a note

Add a Markdown file to `_posts/`, named with the date and a short title:

```
_posts/2026-11-10-burgundy-became-blue.md
```

Start the file with a title, then write:

```markdown
---
title: Burgundy became blue
---

Your note goes here.
```

Push it, and the note shows up under **Notes** on the site within a minute.

## Contact details and facts

Email, booking link, company line, LinkedIn and GitHub live in `_config.yml`.

## How it's built

- [Jekyll](https://jekyllrb.com), built by GitHub Pages itself. No build step, no plugins.
- Design "Drawn to scale": one idea per screen, no JavaScript. Design in Figma (t/m website).
- Styling follows the t/m brand guidelines: Princess Blue `#00539C`, Anise Flower `#F4E3B5`,
  Bricolage Grotesque for headings, Familjen Grotesk for text and DM Mono for labels.
- Fonts are self-hosted under the SIL Open Font License, see assets/fonts/OFL.txt.
- All styles are in `assets/css/style.css`; page layouts are in `_layouts/`, shared pieces in `_includes/`.

To preview locally without installing Ruby:

```sh
podman run --rm -p 4000:4000 -v "$PWD":/srv/jekyll:Z docker.io/jekyll/jekyll:4.2.2 jekyll serve
```

Then open http://localhost:4000.

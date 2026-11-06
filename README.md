# t/m — thomas moerman

My personal site: projects, notes and a bit about me.

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

Push it, and the note shows up under **notes** on the site within a minute.

## Adding a project

Projects live in `_data/projects.yml`. Copy an existing entry and change the
label, title, text, tags and link.

## How it's built

- [Jekyll](https://jekyllrb.com), built by GitHub Pages itself. No build step, no plugins.
- Styling follows the t/m brand guidelines: Princess Blue `#00539C`, Anise Flower `#F4E3B5`,
  Bricolage Grotesque for headings, Familjen Grotesk for text and DM Mono for labels.
- All styles are in `assets/css/style.css`; the page layout is in `_layouts/default.html`.

To preview locally without installing Ruby:

```sh
podman run --rm -p 4000:4000 -v "$PWD":/srv/jekyll:Z docker.io/jekyll/jekyll:4.2.2 jekyll serve
```

Then open http://localhost:4000.

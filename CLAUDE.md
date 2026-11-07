# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Teaching materials for a university intro-to-web-development session (audience: complete beginners, pure HTML only — no CSS/JS in the student exercise). There is no application code, package.json, test suite, or git repo; the content is a Marp slide deck plus a sample resume page.

- `presentation/introduction/` — the Marp deck (see its `README.md` for the 8-section outline).
  - `slides.md` — the source; edit this. Slides are separated by `---`.
  - `theme.css` — custom "doodle" Marp theme (`@theme doodle`) with fonts embedded as base64 so the deck works offline.
  - `assets/fonts.css` — generated `@font-face` block that is embedded in `theme.css`; don't hand-edit the base64.
  - `assets/icons/` — OpenMoji SVGs, referenced from slides.
  - `slides.pdf`, `slides.html` — generated outputs; regenerate after editing `slides.md`/`theme.css`.
  - `examples/resume.example.html` — reference solution for the "Your turn" section (section 7).
- `presentation/tables-and-forms/` — session 2 deck (tables, forms, 2 exercises). Same layout; `theme.css` and `assets/` are copies of the introduction deck's plus extra `.demo` styles for live form controls.
- `presentation/css/` — session 3 deck (CSS basics → layout → frameworks). `theme.css` and `assets/` copied from tables-and-forms, plus `.demo.plain` and `.sw` helpers.
- `resume/resume.html` — a standalone resume page.

Each deck has its own `README.md` with its section outline. Theme changes are not shared: edit the copy in the deck you are working on.

## Commands

Requires Node.js and Marp CLI (`npm i -g @marp-team/marp-cli`). Run from a deck's folder (e.g. `presentation/introduction/`). Add `--no-stdin` when running marp in the background or from a script, otherwise it hangs waiting on stdin:

```bash
# PDF
marp slides.md --theme theme.css --html --allow-local-files -o slides.pdf
# Standalone HTML (keep assets/ next to it)
marp slides.md --theme theme.css --html --allow-local-files -o slides.html
# Live preview
marp slides.md --theme theme.css --html --allow-local-files --preview
# PNG per slide (for visual review)
marp slides.md --theme theme.css --html --allow-local-files --images png
```

`--html` and `--allow-local-files` are required: slides use raw HTML (`<div class="row">`, `<img>`) and local icon files.

## Conventions

- Per-slide styling uses Marp directives, e.g. `<!-- _class: title -->`, `<!-- _class: section s2 -->`, `<!-- _class: dense -->`; the classes are defined in `theme.css`. Front matter sets `theme: doodle`, `paginate`, `html: true`, and the footer.
- Icons: `![w:120](assets/icons/robot.svg)` or inline `<img src="assets/icons/...">`.
- `theme.css` is large mostly because of embedded base64 fonts (Bangers, Caveat, Comic Neue, Fira Code) — avoid reading it whole; grep for the class you need.
- Keep the deck beginner-friendly: the exercise restricts students to HTML tags (headings, `br`, `img`, `p`, lists, forms).

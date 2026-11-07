# Intro to Web Development — Marp deck

A doodle-style slide deck that introduces **university students to web
development** through pure HTML. Built with [Marp](https://marp.app/).

- **Audience:** complete beginners (first contact with code)
- **Goal:** understand that web pages are HTML, learn the essential tags,
  create a first document, and build a resume page — with AI as a co-pilot.

## Files

```
presentation/introduction/
├── slides.md                  # the presentation (edit this)
├── theme.css                  # custom "doodle" theme (fonts embedded)
├── slides.pdf                 # rendered deck (generated)
├── slides.html                # rendered deck, browser presentation (generated)
├── assets/
│   ├── fonts.css              # generated @font-face (embedded in theme.css)
│   └── icons/                 # OpenMoji doodle SVGs
└── examples/
    └── resume.example.html    # reference solution for section 7
```

## The 8 sections

1. **Web pages are HTML** — HTML is the structure of every page, and it is
   built from tags.
2. **Meet the tags** — `h1`…`h6`, `br`, `img`, `p`, `ul`, `ol`, `li`, forms,
   plus a cheat sheet.
3. **Your first HTML document** — the skeleton every page shares, and how to
   create/open your first file.
4. **Coding with AI in 2026** — free tools (OpenCode, Claude, Gemini, Codex,
   Copilot, Cursor) and how to use them responsibly.
5. **A full example** — one page, read line by line.
6. **Quiz** — 6 questions, with answers.
7. **Your turn** — build `resume.html` using HTML only (no CSS, no JS).
8. **Thank you** — and let's code.

## Build / present

Requires Node.js and the Marp CLI (`npm i -g @marp-team/marp-cli`).

```bash
cd presentation/introduction

# Export a PDF
marp slides.md --theme theme.css --html --allow-local-files -o slides.pdf

# Export a standalone HTML file (keep the assets/ folder next to it)
marp slides.md --theme theme.css --html --allow-local-files -o slides.html

# Live preview while editing
marp slides.md --theme theme.css --html --allow-local-files --preview

# Quick PNGs of every slide (great for review)
marp slides.md --theme theme.css --html --allow-local-files --images png
```

In the HTML deck: `F` fullscreen, `←`/`→` to navigate, `P` presenter view.

## Editing tips

- Slides are separated by `---`. Directives like `<!-- _class: section s2 -->`
  and `<!-- _class: dense -->` style individual slides (see `theme.css`).
- Icons live in `assets/icons/`. Use them like
  `![w:120](assets/icons/robot.svg)` or as inline `<img>`.
- The font is embedded in `theme.css`, so the deck works **offline**.

## Credits

- Icons: [OpenMoji](https://openmoji.org/) — CC BY-SA 4.0.
- Fonts: Bangers, Caveat, Comic Neue, Fira Code via Google Fonts — SIL OFL 1.1.
  Subsets are embedded as base64 in `theme.css`.

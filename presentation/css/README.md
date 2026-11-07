# CSS — Marp deck

Session 3 of the intro-to-web-development course. Same doodle theme as the other
decks. Builds on the `resume.html` (with its table and form) from sessions 1–2.

## Sections (27 slides, deliberately basic)

1. **Meet CSS** — what it is, anatomy of a rule, inline / internal / external
2. **Selectors** — element, class, id
3. **Colors & text** — color formats, text properties
4. **The box model** — margin / padding / border
5. **Practice** — 4-question quiz; style your resume in `style.css` (starter stylesheet)
6. **CSS frameworks** — a first look: what they are, component vs utility-first, Bootstrap, Tailwind
7. **Recap**

Flexbox/grid, responsive design, units, fonts and the framework comparison exercise
were cut from an earlier 49-slide version.

## Build

```bash
cd presentation/css
marp --no-stdin slides.md --theme theme.css --html --allow-local-files -o slides.html
marp --no-stdin slides.md --theme theme.css --html --allow-local-files -o slides.pdf
```

## Notes

- `theme.css` and `assets/` are copies from `../tables-and-forms`; the end of `theme.css`
  adds `.demo.plain` (live demo boxes without the heading font) and `.sw` (color swatches).
- Framework CDN snippets use Bootstrap 5.3.3 and the Tailwind v4 browser build
  (`@tailwindcss/browser@4`), which is for learning only. Check the versions before teaching.
- Use class `dense` on slides whose code overflows.

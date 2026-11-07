# HTML Tables & Forms — Marp deck

Session 2 of the intro-to-web-development course. Same doodle theme as
`../introduction`, still **pure HTML** (no CSS, no JavaScript for students).

- **Audience:** beginners who finished session 1 (headings, lists, images, a first `resume.html`)
- **Goal:** display data with tables, collect input with forms, and add both to the resume.

## Sections

1. **Tables** — `table`, `tr`, `th`, `td`
2. **Table pro** — `caption`, `thead`/`tbody`/`tfoot`, `colspan`, `rowspan`
   - **Exercise 1:** build the structure of an invoice (with solution)
3. **Forms** — `form`, `label`/`input`, input types, `select`, `textarea`, buttons
4. **Good forms** — validation attributes, `fieldset`, checklist, full example
   - **Exercise 2:** event registration form (with solution)
5. **Quiz** — 6 questions with answers
6. **Your turn** — add a skills table and a contact form to `resume.html`
7. **Recap**

## Build

Requires the Marp CLI (`npm i -g @marp-team/marp-cli`). PNG/PDF export launches a
browser and takes a couple of minutes.

```bash
cd presentation/tables-and-forms
marp slides.md --theme theme.css --html --allow-local-files -o slides.html
marp slides.md --theme theme.css --html --allow-local-files -o slides.pdf
marp slides.md --theme theme.css --html --allow-local-files --preview
```

## Notes

- `theme.css` and `assets/` are copies of the introduction deck's; the end of
  `theme.css` adds styles so real form controls and tables render inside `.demo`.
- Demo forms use live HTML controls; use class `dense` on slides whose code block overflows.

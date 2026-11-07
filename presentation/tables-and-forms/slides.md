---
marp: true
theme: doodle
paginate: true
html: true
footer: 'Web Dev #2  ·  tables & forms'
---

<!-- _class: title -->
<!-- _footer: "" -->
<!-- _paginate: false -->

# TABLES & FORMS

<p class="subtitle">data in, data out</p>

<div class="row">
<img src="assets/icons/memo.svg" alt="">
<img src="assets/icons/keyboard.svg" alt="">
<img src="assets/icons/rocket.svg" alt="">
</div>

<p class="big">Show <span class="mark">data</span> in a grid — and <span class="mark">collect</span> it from your visitors.</p>
<p class="who">Session 2 · still pure HTML — no CSS, no JavaScript</p>

---

<!-- _class: title -->

# Today's roadmap

<div class="cards four">
<div class="card tint-coral"><h3>1 · Tables</h3>Rows, cells and headers: <code>table</code> <code>tr</code> <code>th</code> <code>td</code>.</div>
<div class="card tint-blue"><h3>2 · Table pro</h3>Sections, captions and merged cells.</div>
<div class="card tint-green"><h3>3 · Forms</h3>Let visitors type, pick and send.</div>
<div class="card tint-yellow"><h3>4 · Input types</h3>Email, date, number, checkbox, radio, select…</div>
<div class="card tint-purple"><h3>5 · Good forms</h3>Labels, validation, structure.</div>
<div class="card tint-coral"><h3>6 · Quiz</h3>Check what stuck.</div>
<div class="card tint-blue"><h3>7 · You code</h3>Upgrade your resume.</div>
<div class="card tint-green"><h3>8 · Wrap-up</h3>Recap and next steps.</div>
</div>

<!-- ============================================================
     SECTION 1 — TABLES
     ============================================================ -->

---

<!-- _class: section s1 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 01</p>

# Tables

<p class="sub">Timetables, prices, scores, schedules — whenever data has rows and columns, you need a table.</p>

<img class="divider-ico" src="assets/icons/books.svg" alt="">

---

# Why a table?

<div class="cols">
<div class="col">

A table shows **data in a grid**: each row is one record, each column is one kind of information.

Good uses:

- a class timetable
- a price list
- exam results
- a comparison of options

</div>
<div class="col">

<div class="demo">
<table>
<tr><th>Course</th><th>Day</th><th>Room</th></tr>
<tr><td>Web Dev</td><td>Monday</td><td>B12</td></tr>
<tr><td>Databases</td><td>Tuesday</td><td>A03</td></tr>
</table>
</div>

</div>
</div>

<blockquote>Tables are for <b>data</b>, never for page layout. Layout is CSS's job (later!).</blockquote>

---

# Your first table

<div class="cols">
<div class="col">

```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Amal</td>
    <td>20</td>
  </tr>
  <tr>
    <td>Youssef</td>
    <td>22</td>
  </tr>
</table>
```

</div>
<div class="col">

<div class="demo">
<table>
<tr><th>Name</th><th>Age</th></tr>
<tr><td>Amal</td><td>20</td></tr>
<tr><td>Youssef</td><td>22</td></tr>
</table>
</div>

<p class="caveat">The browser draws the grid. You only describe the data.</p>

</div>
</div>

---

# The four tags

<img class="float-r ico" src="assets/icons/label.svg" alt="">

<div class="cards">
<div class="card tint-coral"><h3><code>table</code></h3>The whole table. Everything lives inside it.</div>
<div class="card tint-blue"><h3><code>tr</code></h3><b>T</b>able <b>R</b>ow. One horizontal line of cells.</div>
<div class="card tint-yellow"><h3><code>th</code></h3><b>T</b>able <b>H</b>eader cell. Bold, centered — a title.</div>
<div class="card tint-green"><h3><code>td</code></h3><b>T</b>able <b>D</b>ata cell. A normal piece of data.</div>
</div>

<blockquote>Think in order: a <b>table</b> has <b>rows</b>, and a row has <b>cells</b>. You never write columns — they appear from the cells.</blockquote>

---

# Rows first, columns follow

Every `tr` must contain the **same number of cells** (unless you merge them — coming up).

<div class="cols">
<div class="col">

```html
<tr>
  <td>A1</td>
  <td>B1</td>
  <td>C1</td>
</tr>
<tr>
  <td>A2</td>
  <td>B2</td>
  <td>C2</td>
</tr>
```

</div>
<div class="col">

<div class="demo">
<table>
<tr><td>A1</td><td>B1</td><td>C1</td></tr>
<tr><td>A2</td><td>B2</td><td>C2</td></tr>
</table>
</div>

<p class="caveat">3 cells per row → 3 columns.</p>

</div>
</div>

---

<!-- _class: dense -->

# Table pro

Group rows by role, and give the table a title:

<div class="cols">
<div class="col">

```html
<table>
  <caption>Monthly budget</caption>
  <thead>
    <tr><th>Item</th><th>Cost</th></tr>
  </thead>
  <tbody>
    <tr><td>Rent</td><td>300</td></tr>
    <tr><td>Food</td><td>150</td></tr>
  </tbody>
  <tfoot>
    <tr><th>Total</th><td>450</td></tr>
  </tfoot>
</table>
```

</div>
<div class="col">

<div class="demo">
<table>
<caption>Monthly budget</caption>
<thead><tr><th>Item</th><th>Cost</th></tr></thead>
<tbody><tr><td>Rent</td><td>300</td></tr><tr><td>Food</td><td>150</td></tr></tbody>
<tfoot><tr><th>Total</th><td>450</td></tr></tfoot>
</table>
</div>

<div class="muted"><b>caption</b> = title · <b>thead</b> = header rows · <b>tbody</b> = main data · <b>tfoot</b> = totals. Screen readers love this.</div>

</div>
</div>

---

<!-- _class: dense -->

# Merging cells

<div class="cols">
<div class="col">

```html
<table>
  <tr>
    <th colspan="2">Monday</th>
  </tr>
  <tr>
    <td>8:30</td><td>Web Dev</td>
  </tr>
  <tr>
    <td rowspan="2">Lunch</td>
    <td>12:00</td>
  </tr>
  <tr>
    <td>13:00</td>
  </tr>
</table>
```

</div>
<div class="col">

<div class="demo">
<table>
<tr><th colspan="2">Monday</th></tr>
<tr><td>8:30</td><td>Web Dev</td></tr>
<tr><td rowspan="2">Lunch</td><td>12:00</td></tr>
<tr><td>13:00</td></tr>
</table>
</div>

<div class="muted"><code>colspan="2"</code> → stretch across 2 <b>columns</b>.<br><code>rowspan="2"</code> → stretch down 2 <b>rows</b>. The cells it covers are <b>not</b> written again.</div>

</div>
</div>

---

# Table cheat sheet

| Tag / attribute | What it does | Example |
| --- | --- | --- |
| `table` | The whole table | `<table>…</table>` |
| `tr` | A row | `<tr>…</tr>` |
| `th` / `td` | Header cell / data cell | `<td>42</td>` |
| `caption` | Table title | `<caption>Budget</caption>` |
| `thead` `tbody` `tfoot` | Header / body / footer rows | `<tbody>…</tbody>` |
| `colspan` / `rowspan` | Merge cells across / down | `<td colspan="2">` |

<p class="caveat">Table = rows of cells. Everything else is a refinement.</p>

---

<!-- _class: section s1 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">EXERCISE 1</p>

# Build an invoice

<p class="sub">Tables in the real world: structure a complete invoice, using everything from this section.</p>

<img class="divider-ico" src="assets/icons/memo.svg" alt="">

---

<!-- _class: dense -->

# Exercise 1 — the invoice

<div class="cols">
<div class="col">

Create **`invoice.html`** with the **structure** of this invoice (no styling needed):

- a `caption` with the invoice number
- a `thead` with 4 columns: *Description*, *Qty*, *Unit price*, *Total*
- a `tbody` with **3 items**
- a `tfoot` with **Subtotal**, **VAT (20%)** and **Total**, where the label cell uses `colspan="3"`

</div>
<div class="col">

<div class="demo">
<table>
<caption>Invoice #2026-014</caption>
<thead><tr><th>Description</th><th>Qty</th><th>Unit price</th><th>Total</th></tr></thead>
<tbody>
<tr><td>Web hosting</td><td>1</td><td>50</td><td>50</td></tr>
<tr><td>Domain name</td><td>2</td><td>12</td><td>24</td></tr>
<tr><td>Support</td><td>3</td><td>20</td><td>60</td></tr>
</tbody>
<tfoot>
<tr><th colspan="3">Subtotal</th><td>134</td></tr>
<tr><th colspan="3">VAT (20%)</th><td>26.80</td></tr>
<tr><th colspan="3">Total</th><td>160.80</td></tr>
</tfoot>
</table>
</div>

</div>
</div>

<blockquote>Bonus: add a header row with <b>your company</b> and the <b>client</b> (use <code>colspan</code>).</blockquote>

---

<!-- _class: dense -->

# Exercise 1 — solution

<div class="cols">
<div class="col">

```html
<table>
  <caption>Invoice #2026-014</caption>
  <thead>
    <tr><th>Description</th><th>Qty</th>
        <th>Unit price</th><th>Total</th></tr>
  </thead>
  <tbody>
    <tr><td>Web hosting</td><td>1</td>
        <td>50</td><td>50</td></tr>
    <tr><td>Domain name</td><td>2</td>
        <td>12</td><td>24</td></tr>
    <tr><td>Support</td><td>3</td>
        <td>20</td><td>60</td></tr>
  </tbody>
  <tfoot>
    <tr><th colspan="3">Subtotal</th><td>134</td></tr>
    <tr><th colspan="3">VAT (20%)</th><td>26.80</td></tr>
    <tr><th colspan="3">Total</th><td>160.80</td></tr>
  </tfoot>
</table>
```

</div>
<div class="col">

<div class="card tint-green">
<h3>Check yourself</h3>
Every body row has <b>4 cells</b>. Every footer row is <b>3 + 1</b>: one cell stretched over 3 columns, plus the amount.
</div>

<div class="card tint-yellow" style="margin-top:16px;">
<h3>Common slip</h3>
Writing <code>colspan="3"</code> <i>and</i> 3 empty cells → the row gets too wide. Merged cells are <b>not</b> written again.
</div>

</div>
</div>

<!-- ============================================================
     SECTION 2 — FORMS
     ============================================================ -->

---

<!-- _class: section s2 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 02</p>

# Forms

<p class="sub">Login, sign-up, search, contact… every time you type something on a website, you're using a form.</p>

<img class="divider-ico" src="assets/icons/keyboard.svg" alt="">

---

# Anatomy of a form

<div class="cols">
<div class="col">

```html
<form action="/send" method="post">
  <label for="email">Email</label>
  <input type="email" id="email"
         name="email">

  <button type="submit">Join</button>
</form>
```

</div>
<div class="col">

<div class="demo">
<form onsubmit="return false">
<label for="d-email">Email</label>
<input type="email" id="d-email" placeholder="you@example.com">
<button type="button">Join</button>
</form>
</div>

<div class="muted"><b>action</b> = where the data is sent · <b>method</b> = how (<code>get</code> or <code>post</code>).</div>

</div>
</div>

<blockquote>Without a server to receive it, a form can't really "send" anything yet. Today we build the <b>front</b> of the form.</blockquote>

---

# `label` + `input` = a pair

<img class="float-r ico" src="assets/icons/label.svg" alt="">

```html
<label for="city">City</label>
<input type="text" id="city" name="city">
```

<div class="cards">
<div class="card tint-blue"><h3><code>for</code> = <code>id</code></h3>The label's <code>for</code> must match the input's <code>id</code>. Then clicking the label focuses the field.</div>
<div class="card tint-yellow"><h3><code>name</code></h3>The key under which the value is sent. No <code>name</code> → the data is lost.</div>
<div class="card tint-green"><h3><code>type</code></h3>Decides what kind of field it is. Default: <code>text</code>.</div>
</div>

---

<!-- _class: dense -->

# Input types (1/2) — text-like

| `type` | Gives you | Bonus |
| --- | --- | --- |
| `text` | One line of text | the default |
| `email` | An email address | checks for `@` |
| `password` | Hidden characters | shows dots |
| `number` | A number | arrows, rejects letters |
| `date` | A calendar picker | no typing errors |

<div class="demo" style="margin-top:14px;">
<div class="cols">
<div class="col"><label>Email</label><input type="email" placeholder="you@example.com"></div>
<div class="col"><label>Password</label><input type="password" value="secret123"></div>
<div class="col"><label>Number</label><input type="number" value="3"></div>
</div>
</div>

---

<!-- _class: dense -->

# Input types (2/2) — choices

<div class="cols">
<div class="col">

```html
<!-- checkbox: 0, 1 or many -->
<input type="checkbox" id="h" name="skill">
<label for="h">HTML</label>

<!-- radio: one per name -->
<input type="radio" id="m" name="lvl">
<label for="m">Beginner</label>
<input type="radio" id="a" name="lvl">
<label for="a">Advanced</label>
```

</div>
<div class="col">

<div class="demo inline">
<b>Skills</b><br>
<input type="checkbox" id="d1" checked><label for="d1">HTML</label>
<input type="checkbox" id="d2"><label for="d2">CSS</label>
<br><br>
<b>Level</b><br>
<input type="radio" id="d3" name="dl" checked><label for="d3">Beginner</label>
<input type="radio" id="d4" name="dl"><label for="d4">Advanced</label>
</div>

<p class="caveat">Radios with the <b>same <code>name</code></b> form a group: pick only one.</p>

</div>
</div>

---

<!-- _class: dense -->

# Dropdown & text area

<div class="cols">
<div class="col">

```html
<label for="uni">Faculty</label>
<select id="uni" name="faculty">
  <option value="">-- choose --</option>
  <option value="sci">Sciences</option>
  <option value="law">Law</option>
</select>

<label for="msg">Message</label>
<textarea id="msg" name="msg"
          rows="4"></textarea>
```

</div>
<div class="col">

<div class="demo">
<label>Faculty</label>
<select><option>-- choose --</option><option>Sciences</option><option>Law</option></select>
<label>Message</label>
<textarea></textarea>
</div>

<div class="muted"><code>select</code> + <code>option</code> → one pick from a list.<br><code>textarea</code> → several lines (it has a closing tag!).</div>

</div>
</div>

---

# Buttons

```html
<button type="submit">Send</button>   <!-- sends the form -->
<button type="reset">Clear</button>   <!-- empties the fields -->
<button type="button">Click me</button>  <!-- does nothing yet -->
```

<div class="cards">
<div class="card tint-green"><h3>submit</h3>The default inside a form. Triggers the sending.</div>
<div class="card tint-yellow"><h3>reset</h3>Puts every field back to its start value.</div>
<div class="card tint-blue"><h3>button</h3>No built-in action. JavaScript will use it later.</div>
</div>

<blockquote>Always write the <code>type</code> explicitly — a forgotten one defaults to <code>submit</code>.</blockquote>

<!-- ============================================================
     SECTION 3 — GOOD FORMS
     ============================================================ -->

---

<!-- _class: section s3 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 03</p>

# Good forms

<p class="sub">A form that works is nice. A form that is clear, safe to fill, and accessible is professional.</p>

<img class="divider-ico" src="assets/icons/check-mark-button.svg" alt="">

---

# Help the user — free validation

HTML can check input **before** it is sent. Just add attributes:

<div class="cols">
<div class="col">

```html
<input type="text" name="user"
       required
       minlength="3"
       placeholder="Your name">

<input type="number" name="age"
       min="16" max="99">
```

</div>
<div class="col">

- **`required`** → cannot be left empty
- **`minlength` / `maxlength`** → text length
- **`min` / `max`** → number or date range
- **`placeholder`** → grey hint inside the field
- **`value`** → pre-filled content

</div>
</div>

<blockquote>A <code>placeholder</code> is a hint, <b>not</b> a replacement for a <code>label</code>.</blockquote>

---

# Group fields

<div class="cols">
<div class="col">

```html
<fieldset>
  <legend>Contact</legend>
  <label for="n">Name</label>
  <input type="text" id="n" name="n">
  <label for="e">Email</label>
  <input type="email" id="e" name="e">
</fieldset>
```

</div>
<div class="col">

<div class="demo">
<fieldset>
<legend>Contact</legend>
<label>Name</label><input type="text">
<label>Email</label><input type="email">
</fieldset>
</div>

<div class="muted"><code>fieldset</code> draws a box around related fields; <code>legend</code> is its title.</div>

</div>
</div>

---

# Form checklist

<ul>
<li>Every field has a visible <b><code>label</code></b> linked with <code>for</code> / <code>id</code></li>
<li>Every field has a <b><code>name</code></b></li>
<li>Pick the <b>right <code>type</code></b> (email, number, date…)</li>
<li>Mark mandatory fields with <b><code>required</code></b></li>
<li>Group related fields with <b><code>fieldset</code></b></li>
<li>The button has an explicit <b><code>type</code></b></li>
</ul>

<p class="caveat">Tick all six and your form is already better than half of the web.</p>

---

<!-- _class: dense -->

# A full example

<div class="cols">
<div class="col">

```html
<form action="/register" method="post">
  <label for="n">Name</label>
  <input type="text" id="n" name="n" required>

  <label for="d">Birth date</label>
  <input type="date" id="d" name="d">

  <label for="f">Faculty</label>
  <select id="f" name="f">
    <option>Sciences</option>
    <option>Law</option>
  </select>

  <input type="checkbox" id="ok" name="ok">
  <label for="ok">I accept the rules</label>

  <button type="submit">Register</button>
</form>
```

</div>
<div class="col">

<div class="demo">
<label>Name</label><input type="text">
<label>Birth date</label><input type="date">
<label>Faculty</label>
<select><option>Sciences</option><option>Law</option></select>
<div class="inline" style="margin-top:8px;"><input type="checkbox" id="d9"><label for="d9">I accept the rules</label></div>
<button type="button">Register</button>
</div>

</div>
</div>

---

<!-- _class: section s3 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">EXERCISE 2</p>

# Build a form

<p class="sub">Put the whole forms toolbox together in one registration page.</p>

<img class="divider-ico" src="assets/icons/keyboard.svg" alt="">

---

# Exercise 2 — event registration

Create **`register.html`** — a sign-up form for a student event:

<div class="cols">
<div class="col">

1. A `fieldset` **"About you"**: full name (required), email (required), birth date
2. A `fieldset` **"Your event"**: a `select` of 3 workshops, **radio** buttons for the day (Saturday / Sunday), **checkboxes** for the meals you want
3. A `textarea` for questions
4. A required **checkbox** "I accept the rules"
5. **Submit** and **reset** buttons

</div>
<div class="col">

<div class="card tint-yellow">
<h3>Rules</h3>
Every field: a linked <code>label</code>, a <code>name</code>, the right <code>type</code>. Radios share one <code>name</code>.
</div>

<div class="card tint-blue" style="margin-top:16px;">
<h3>Test it</h3>
Click each label. Submit empty — does the browser complain? Try a bad email.
</div>

</div>
</div>

---

<!-- _class: dense -->

# Exercise 2 — solution

<div class="cols">
<div class="col">

```html
<form action="#" method="post">
  <fieldset>
    <legend>About you</legend>
    <label for="n">Full name</label>
    <input type="text" id="n" name="name" required>
    <label for="e">Email</label>
    <input type="email" id="e" name="email" required>
    <label for="b">Birth date</label>
    <input type="date" id="b" name="birth">
  </fieldset>

  <!-- fieldset "Your event" → next column -->

  <label for="q">Questions</label>
  <textarea id="q" name="questions"></textarea>
  <input type="checkbox" id="ok" name="ok" required>
  <label for="ok">I accept the rules</label>

  <button type="submit">Register</button>
  <button type="reset">Clear</button>
</form>
```

</div>
<div class="col">

```html
<fieldset>
  <legend>Your event</legend>
  <label for="w">Workshop</label>
  <select id="w" name="workshop">
    <option>HTML</option>
    <option>CSS</option>
    <option>Git</option>
  </select>
  <input type="radio" id="sat" name="day">
  <label for="sat">Saturday</label>
  <input type="radio" id="sun" name="day">
  <label for="sun">Sunday</label>
  <input type="checkbox" id="lu" name="meal">
  <label for="lu">Lunch</label>
</fieldset>
```

<p class="caveat">Check: both radios share <code>name="day"</code>, every field has a <code>for</code>/<code>id</code> pair.</p>

</div>
</div>

<!-- ============================================================
     SECTION 4 — QUIZ
     ============================================================ -->

---

<!-- _class: section s4 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 04</p>

# Quiz time

<p class="sub">Six questions. Answers right after. No pressure!</p>

<img class="divider-ico" src="assets/icons/question-mark.svg" alt="">

---

# Question 1

<ul class="quiz">
<li><span class="qn">1</span>Which tag creates a table <b>row</b>?
<span class="opts"><b>A.</b> <code>&lt;td&gt;</code>  <b>B.</b> <code>&lt;tr&gt;</code>  <b>C.</b> <code>&lt;th&gt;</code></span></li>
<li><span class="qn">2</span>How do you make a cell span <b>3 columns</b>?
<span class="opts"><b>A.</b> <code>rowspan="3"</code>  <b>B.</b> <code>colspan="3"</code>  <b>C.</b> <code>width="3"</code></span></li>
<li><span class="qn">3</span>Should you use a table to position your page layout?
<span class="opts"><b>A.</b> Yes  <b>B.</b> Only for headers  <b>C.</b> No — tables are for data</span></li>
</ul>

---

# Question 2

<ul class="quiz">
<li><span class="qn">4</span>What links a <code>label</code> to its <code>input</code>?
<span class="opts"><b>A.</b> <code>for</code> = <code>id</code>  <b>B.</b> <code>name</code> = <code>type</code>  <b>C.</b> <code>href</code> = <code>src</code></span></li>
<li><span class="qn">5</span>How do you let users choose <b>exactly one</b> option among several?
<span class="opts"><b>A.</b> checkboxes  <b>B.</b> radios sharing a <code>name</code>  <b>C.</b> a textarea</span></li>
<li><span class="qn">6</span>Which attribute stops a form being sent with an empty field?
<span class="opts"><b>A.</b> <code>placeholder</code>  <b>B.</b> <code>value</code>  <b>C.</b> <code>required</code></span></li>
</ul>

---

# Answers

<ul class="quiz">
<li class="answer"><span class="qn">1</span><b>B — <code>&lt;tr&gt;</code>.</b> <code>td</code> and <code>th</code> are cells <i>inside</i> a row.</li>
<li class="answer"><span class="qn">2</span><b>B — <code>colspan="3"</code>.</b> <code>rowspan</code> merges downward instead.</li>
<li class="answer"><span class="qn">3</span><b>C — no.</b> Tables describe data; layout is done with CSS.</li>
<li class="answer"><span class="qn">4</span><b>A — <code>for</code> = <code>id</code>.</b> Clicking the label then focuses the field.</li>
<li class="answer"><span class="qn">5</span><b>B — radios with the same <code>name</code>.</b> Checkboxes allow several.</li>
<li class="answer"><span class="qn">6</span><b>C — <code>required</code>.</b> A placeholder is only a hint.</li>
</ul>

<!-- ============================================================
     SECTION 5 — YOUR TURN
     ============================================================ -->

---

<!-- _class: section s5 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 05</p>

# Your turn

<p class="sub">Upgrade your resume with a table and a contact form. Still HTML only.</p>

<img class="divider-ico" src="assets/icons/memo.svg" alt="">

---

# Your mission

<div class="cols">
<div class="col">

Open your **`resume.html`** from last session and add:

1. **A skills table** — columns: *Skill*, *Level*, *Years*. Use `caption`, `thead` and `tbody`.
2. **A timetable or experience table** using at least one `colspan` or `rowspan`.
3. **A contact form** with: name, email, a subject `select`, a message `textarea`, and a submit button.

</div>
<div class="col">

<div class="card tint-yellow">
<h3>Rules</h3>
HTML only. Same file. Every field has a <code>label</code>, a <code>name</code>, and the right <code>type</code>. Mandatory fields use <code>required</code>.
</div>

<div class="card tint-green" style="margin-top:16px;">
<h3>Tip</h3>
Build the table first, refresh, then the form. Test by clicking labels and trying to submit empty.
</div>

</div>
</div>

---

<!-- _class: dense -->

# Starter snippet

```html
<h2>Skills</h2>
<table>
  <caption>My skills</caption>
  <thead>
    <tr><th>Skill</th><th>Level</th><th>Years</th></tr>
  </thead>
  <tbody>
    <tr><td>HTML</td><td>Beginner</td><td>0</td></tr>
  </tbody>
</table>

<h2>Contact me</h2>
<form action="#" method="post">
  <label for="name">Name</label>
  <input type="text" id="name" name="name" required>
  <label for="email">Email</label>
  <input type="email" id="email" name="email" required>
  <label for="msg">Message</label>
  <textarea id="msg" name="msg"></textarea>
  <button type="submit">Send</button>
</form>
```

<p class="caveat">Now grow it: more rows, a subject dropdown, a fieldset. Make it yours!</p>

<!-- ============================================================
     SECTION 6 — WRAP-UP
     ============================================================ -->

---

<!-- _class: section s6 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 06</p>

# Recap

<p class="sub">Two big skills in one session: displaying data and collecting it.</p>

<img class="divider-ico" src="assets/icons/party-popper.svg" alt="">

---

# What you learned

<div class="cards">
<div class="card tint-coral"><h3>Tables</h3><code>table</code> → <code>tr</code> → <code>th</code>/<code>td</code>. Refine with <code>caption</code>, <code>thead</code>, <code>colspan</code>, <code>rowspan</code>.</div>
<div class="card tint-blue"><h3>Forms</h3><code>form</code> wraps <code>label</code> + <code>input</code> / <code>select</code> / <code>textarea</code> and a <code>button</code>.</div>
<div class="card tint-green"><h3>Quality</h3>Link labels, name fields, pick the right <code>type</code>, add <code>required</code>.</div>
</div>

<blockquote>Next time: <b>CSS</b> — make your tables and forms beautiful.</blockquote>

---

<!-- _class: title -->
<!-- _footer: "" -->
<!-- _paginate: false -->

# Now let's code

<div class="row">
<img src="assets/icons/rocket.svg" alt="">
<img src="assets/icons/laptop.svg" alt="">
<img src="assets/icons/star.svg" alt="">
</div>

<p class="big">Add a table and a form to <code>resume.html</code>.<br>Ask AI when you're stuck — then <span class="mark">understand every line</span>.</p>

<p class="who">Questions? Hands up. Let's build.</p>

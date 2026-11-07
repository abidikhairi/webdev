---
marp: true
theme: doodle
paginate: true
html: true
footer: 'Web Dev #3  ·  CSS'
---

<!-- _class: title -->
<!-- _footer: "" -->
<!-- _paginate: false -->

# CSS

<p class="subtitle">make it beautiful</p>

<div class="row">
<img src="assets/icons/framed-picture.svg" alt="">
<img src="assets/icons/star.svg" alt="">
<img src="assets/icons/rocket.svg" alt="">
</div>

<p class="big">Turn plain HTML into a <span class="mark">designed</span> web page.</p>
<p class="who">Session 3 · a very basic introduction</p>

---

<!-- _class: title -->

# Today's roadmap

<div class="cards four">
<div class="card tint-coral"><h3>1 · CSS</h3>What CSS is and how to add it.</div>
<div class="card tint-blue"><h3>2 · Selectors</h3>Choose <b>what</b> to style.</div>
<div class="card tint-green"><h3>3 · Colors & text</h3>Make it readable and pretty.</div>
<div class="card tint-yellow"><h3>4 · Boxes</h3>Margin, padding, border.</div>
<div class="card tint-purple"><h3>5 · Practice</h3>Quiz + style your resume.</div>
<div class="card tint-coral"><h3>6 · Frameworks</h3>A first look at Bootstrap & Tailwind.</div>
</div>

---

<!-- _class: section s1 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 01</p>

# Meet CSS

<p class="sub">HTML built the walls. CSS is the paint, the furniture and the lighting.</p>

<img class="divider-ico" src="assets/icons/framed-picture.svg" alt="">

---

# Same HTML, different CSS

<div class="cols">
<div class="col">

```html
<h1>My page</h1>
<p>Hello, I am a student.</p>
```

<p class="muted">The HTML is <b>identical</b> on both sides. Only the CSS changes.</p>

</div>
<div class="col">

<div class="demo plain">
<p class="muted" style="margin:0;">Without CSS</p>
<h1 style="font-family:Times,serif;font-size:30px;margin:4px 0;">My page</h1>
<p style="font-family:Times,serif;margin:0 0 12px;">Hello, I am a student.</p>
<p class="muted" style="margin:0;">With CSS</p>
<div style="background:#3b82f6;color:#fff;padding:14px 18px;border-radius:14px;">
<h1 style="font-size:34px;margin:0 0 4px;color:#fff;">My page</h1>
<p style="margin:0;color:#ffe9a8;font-size:22px;">Hello, I am a student.</p>
</div>
</div>

</div>
</div>

<blockquote>CSS = <b>C</b>ascading <b>S</b>tyle <b>S</b>heets. It describes how HTML elements <b>look</b>.</blockquote>

---

# Anatomy of a CSS rule

<img class="float-r ico" src="assets/icons/label.svg" alt="">

<div class="anatomy" style="font-size:34px;line-height:1.5;">
<span class="name">p</span> <span class="br">{</span><br>
&nbsp;&nbsp;<span class="attr">color</span><span class="br">:</span> <span class="val">blue</span><span class="br">;</span><br>
&nbsp;&nbsp;<span class="attr">font-size</span><span class="br">:</span> <span class="val">20px</span><span class="br">;</span><br>
<span class="br">}</span>
</div>

<div class="label-row">
<div class="lab"><b>selector</b>which elements?</div>
<div class="lab"><b>property</b>what to change</div>
<div class="lab"><b>value</b>the new setting</div>
<div class="lab"><b>; and { }</b>punctuation matters!</div>
</div>

<blockquote>"For <b>every paragraph</b>, make the <b>color</b> blue and the <b>font size</b> 20 pixels."</blockquote>

---

# Three ways to add CSS

<div class="cards">
<div class="card tint-coral"><h3>1 · Inline</h3>The <code>style</code> attribute on one tag.<br><span class="pill">avoid</span></div>
<div class="card tint-yellow"><h3>2 · Internal</h3>A <code>&lt;style&gt;</code> block in the <code>head</code>.<br><span class="pill">ok for tests</span></div>
<div class="card tint-green"><h3>3 · External</h3>A separate <code>.css</code> file, linked.<br><span class="pill green">best</span></div>
</div>

```html
<p style="color: red;">Inline</p>

<style>
  p { color: red; }
</style>

<link rel="stylesheet" href="style.css">
```

---

# The best way: an external file

<div class="cols">
<div class="col">

**`index.html`**

```html
<head>
  <meta charset="utf-8">
  <title>My page</title>
  <link rel="stylesheet"
        href="style.css">
</head>
```

</div>
<div class="col">

**`style.css`**

```css
body {
  font-family: sans-serif;
  background: #fffbf0;
}
h1 {
  color: #ff6b6b;
}
```

</div>
</div>

<blockquote>One <code>.css</code> file can style <b>every page</b> of a website — change it once, everything updates.</blockquote>

---

<!-- _class: section s2 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 02</p>

# Selectors

<p class="sub">Before you can style something, you must point at it.</p>

<img class="divider-ico" src="assets/icons/bullseye.svg" alt="">

---

<!-- _class: dense -->

# Element, class and id

<div class="cols">
<div class="col">

```css
/* every <p> */
p { color: gray; }

/* anything with class="note" */
.note { background: #fff3c4; }

/* the one element with id="logo" */
#logo { font-size: 40px; }
```

```html
<p>Normal paragraph</p>
<p class="note">Important</p>
<h1 id="logo">MySite</h1>
```

</div>
<div class="col">

<div class="cards wrap">
<div class="card tint-blue"><h3><code>p</code></h3>By <b>tag name</b>.</div>
<div class="card tint-yellow"><h3><code>.note</code></h3>By <b>class</b>: a dot. Reusable.</div>
<div class="card tint-coral"><h3><code>#logo</code></h3>By <b>id</b>: a hash. Unique.</div>
</div>

</div>
</div>

<blockquote>Use <b>classes</b> most of the time. An <code>id</code> must appear only <b>once</b> per page.</blockquote>

---

<!-- _class: dense -->

# Classes in action

<div class="cols">
<div class="col">

```html
<p class="note">Remember the quiz!</p>
<p class="note warn">Deadline: Friday</p>
<p>Plain text.</p>
```

```css
.note {
  background: #fff3c4;
  padding: 8px;
}
.warn {
  color: #c2410c;
  font-weight: bold;
}
```

<p class="muted">An element can have <b>several classes</b>, separated by spaces.</p>

</div>
<div class="col">

<div class="demo plain">
<p style="background:#fff3c4;padding:8px;border-radius:6px;">Remember the quiz!</p>
<p style="background:#fff3c4;padding:8px;border-radius:6px;color:#c2410c;font-weight:bold;">Deadline: Friday</p>
<p>Plain text.</p>
</div>

</div>
</div>

---

<!-- _class: section s3 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 03</p>

# Colors & text

<p class="sub">The fastest way to make a page look professional.</p>

<img class="divider-ico" src="assets/icons/light-bulb.svg" alt="">

---

# Colors — four ways to write them

```css
h1 { color: tomato; }                 /* name */
h1 { color: #ff6347; }                /* hex */
h1 { color: rgb(255, 99, 71); }       /* red, green, blue */
h1 { color: hsl(9, 100%, 64%); }      /* hue, saturation, lightness */
```

<div style="margin:14px 0;">
<span class="sw" style="background:#ff6b6b"></span><span class="sw" style="background:#3b82f6"></span><span class="sw" style="background:#22c55e"></span><span class="sw" style="background:#f5c518"></span><span class="sw" style="background:#8b5cf6"></span><span class="sw" style="background:#22303f"></span>
</div>

<blockquote>Two properties you will use all the time: <code>color</code> (the text) and <code>background-color</code> (behind it).</blockquote>

---

# Text properties

<div class="cols">
<div class="col">

```css
p {
  font-family: Arial, sans-serif;
  font-size: 20px;
  font-weight: bold;
  font-style: italic;
  text-align: center;
  line-height: 1.6;
  text-decoration: underline;
  text-transform: uppercase;
}
```

</div>
<div class="col">

<div class="demo plain">
<p style="font-family:Arial,sans-serif;font-size:20px;font-weight:bold;font-style:italic;text-align:center;line-height:1.6;text-decoration:underline;text-transform:uppercase;">I am a styled paragraph</p>
</div>

<div class="muted">Always give a <b>fallback</b>: <code>Arial, sans-serif</code>. If the first font is missing, the browser tries the next.</div>

</div>
</div>

---

<!-- _class: section s4 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 04</p>

# The box model

<p class="sub">Every element on a page is a rectangular box.</p>

<img class="divider-ico" src="assets/icons/gear.svg" alt="">

---

# Four layers

<div class="cols">
<div class="col">

<div class="demo plain" style="padding:16px;">
<div style="background:#ffe3e3;border:3px dashed #ff6b6b;padding:16px;text-align:center;">
<b>margin</b> <span class="muted">(outside space)</span>
<div style="background:#22303f;color:#fff;padding:12px;margin-top:6px;">
<b>border</b>
<div style="background:#ddf7e5;color:#22303f;padding:14px;margin-top:6px;">
<b>padding</b> <span class="muted">(inside space)</span>
<div style="background:#fff3c4;color:#22303f;padding:12px;margin-top:6px;"><b>content</b><br>text, image…</div>
</div>
</div>
</div>
</div>

</div>
<div class="col">

- **content** → the text or image itself
- **padding** → space **inside**, between content and border
- **border** → the edge line
- **margin** → space **outside**, pushing neighbours away

<p class="caveat">Padding = inside the box. Margin = outside the box.</p>

</div>
</div>

---

# Margin, padding, border

<div class="cols">
<div class="col">

```css
.card {
  padding: 20px;
  border: 3px solid #22303f;
  border-radius: 16px;
  margin: 24px;
}

/* shorthands: top right bottom left */
.card { padding: 10px 20px 10px 20px; }
/* vertical | horizontal */
.card { margin: 0 auto; }
```

</div>
<div class="col">

<div class="demo plain" style="background:#fffdf6;">
<div style="padding:20px;border:3px solid #22303f;border-radius:16px;background:#fff;margin:4px;">I am a card.</div>
</div>

<div class="muted"><code>margin: 0 auto</code> centers a box with a fixed <code>width</code>. <code>border-radius</code> rounds the corners.</div>

</div>
</div>

---

<!-- _class: section s5 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 05</p>

# Practice

<p class="sub">A tiny quiz, then style your own resume.</p>

<img class="divider-ico" src="assets/icons/question-mark.svg" alt="">

---

# Quick quiz

<ul class="quiz">
<li><span class="qn">1</span>Best way to add CSS to a whole website?
<span class="opts"><b>A.</b> inline <code>style</code>  <b>B.</b> an external <code>.css</code> file</span></li>
<li><span class="qn">2</span>Which selector targets <code>class="note"</code>?
<span class="opts"><b>A.</b> <code>#note</code>  <b>B.</b> <code>.note</code>  <b>C.</b> <code>note</code></span></li>
<li><span class="qn">3</span>Space <b>inside</b> an element's border is…
<span class="opts"><b>A.</b> margin  <b>B.</b> padding</span></li>
<li><span class="qn">4</span>Which property changes the <b>text</b> color?
<span class="opts"><b>A.</b> <code>color</code>  <b>B.</b> <code>text-color</code>  <b>C.</b> <code>font-color</code></span></li>
</ul>

<p class="caveat">Answers: 1 B · 2 B · 3 B · 4 A</p>

---

# Your mission

<div class="cols">
<div class="col">

Create **`style.css`**, link it from your **`resume.html`**, and:

1. Pick a **font** and **2–3 colors**
2. Style headings, text and links (add `:hover`)
3. Give the page a **background color**
4. Put your content in a **centered box** (`max-width`, `margin: 0 auto`, `padding`)
5. Style the **table** with borders and padding

</div>
<div class="col">

<div class="card tint-yellow">
<h3>Rules</h3>
One external <code>style.css</code>. No inline styles.
</div>

<div class="card tint-green" style="margin-top:16px;">
<h3>Tip</h3>
Save, refresh, repeat. Press <b>F12</b> to try values live.
</div>

</div>
</div>

---

<!-- _class: dense -->

# Starter stylesheet

```css
* { box-sizing: border-box; }

body {
  font-family: "Segoe UI", sans-serif;
  line-height: 1.6;
  color: #22303f;
  background: #fffbf0;
  margin: 0;
}

.container { max-width: 800px; margin: 0 auto; padding: 24px; }

h1, h2 { color: #3b82f6; }
a { color: #ff6b6b; }
a:hover { text-decoration: underline; }

table { border-collapse: collapse; width: 100%; }
th, td { border: 2px solid #22303f; padding: 8px; }
```

<p class="caveat">Wrap your page content in <code>&lt;div class="container"&gt;</code> and grow from here.</p>

---

<!-- _class: section s6 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 06</p>

# CSS frameworks

<p class="sub">Ready-made CSS written by thousands of developers. Here is a first look.</p>

<img class="divider-ico" src="assets/icons/rocket.svg" alt="">

---

# What is a CSS framework?

<div class="cols">
<div class="col">

A **framework** is a ready-made stylesheet (often with a little JavaScript) that gives you:

- a **grid** and responsive layout tools
- styled **buttons, forms, cards, navbars**…
- a consistent **design system** (colors, spacing, fonts)
- **cross-browser** fixes already done

</div>
<div class="col">

<div class="cards wrap">
<div class="card tint-green"><h3>Pros</h3>Fast to build · consistent look · battle-tested · big communities</div>
<div class="card tint-coral"><h3>Cons</h3>Pages can look alike · extra size · you can forget how CSS works</div>
</div>

</div>
</div>

<blockquote>A framework is a <b>shortcut</b>, not a replacement. You still need the CSS you learned today.</blockquote>

---

# Two big families

<div class="cards">
<div class="card tint-purple"><h3>Component frameworks</h3>Pre-designed pieces: <code>btn</code>, <code>card</code>, <code>navbar</code>. You assemble them.<br><br><b>Bootstrap · Bulma · Foundation</b></div>
<div class="card tint-blue"><h3>Utility-first frameworks</h3>Tiny single-purpose classes: <code>p-4</code>, <code>text-center</code>, <code>bg-blue-500</code>. You compose your own design.<br><br><b>Tailwind CSS · UnoCSS</b></div>
</div>

<p class="caveat">Component = "here is a button". Utility = "here are the paint tubes".</p>

---

<!-- _class: dense -->

# Bootstrap

<span class="pill purple">components · since 2011</span>

```html
<link rel="stylesheet"
 href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css">
```

<div class="cols">
<div class="col">

```html
<div class="container">
  <div class="row">
    <div class="col-md-6">
      <button class="btn btn-primary">Join</button>
    </div>
    <div class="col-md-6">
      <div class="alert alert-success">Hi!</div>
    </div>
  </div>
</div>
```

</div>
<div class="col">

- **12-column grid**: `container` → `row` → `col-*`
- Ready components: buttons, cards, navbar, forms…
- `col-md-6` = half width from medium screens up
- Best for quick prototypes and school projects

</div>
</div>

---

<!-- _class: dense -->

# Tailwind CSS

<span class="pill blue">utility-first · since 2019</span>

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
```

<div class="cols">
<div class="col">

```html
<div class="max-w-md mx-auto p-6 bg-white">
  <h1 class="text-2xl font-bold">Hello</h1>
  <button class="px-4 py-2 bg-blue-500
                 text-white rounded
                 hover:bg-blue-600">
    Join
  </button>
</div>
```

</div>
<div class="col">

- **No pre-made look**: tiny classes, right in the HTML
- `p-6` = padding, `rounded` = round corners, `hover:` = state, `md:` = responsive
- Real projects use a **build step**; the CDN script is for **learning only**
- Best for custom designs and modern apps

</div>
</div>

---

# What to remember

<div class="cards">
<div class="card tint-coral"><h3>CSS</h3>A rule = selector + properties. Link one external file.</div>
<div class="card tint-blue"><h3>Look</h3>Colors, fonts and the <b>box model</b>.</div>
<div class="card tint-purple"><h3>Frameworks</h3>Bootstrap = components. Tailwind = utilities.</div>
</div>

<blockquote>Learn plain CSS first — every framework is CSS underneath. Next time: <b>JavaScript</b>.</blockquote>

---

<!-- _class: title -->
<!-- _footer: "" -->
<!-- _paginate: false -->

# Now let's style

<div class="row">
<img src="assets/icons/rocket.svg" alt="">
<img src="assets/icons/laptop.svg" alt="">
<img src="assets/icons/star.svg" alt="">
</div>

<p class="big">Create <code>style.css</code>, link it, and <span class="mark">make it yours</span>.</p>

<p class="who">Questions? Hands up. Let's build.</p>

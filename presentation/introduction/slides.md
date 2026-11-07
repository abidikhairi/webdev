---
marp: true
theme: doodle
paginate: true
html: true
footer: 'Intro to Web Dev  ·  your first web page'
---

<!-- _class: title -->
<!-- _footer: "" -->
<!-- _paginate: false -->

# WEB DEVELOPMENT

<p class="subtitle">your first step</p>

<div class="row">
<img src="assets/icons/laptop.svg" alt="">
<img src="assets/icons/globe-with-meridians.svg" alt="">
<img src="assets/icons/rocket.svg" alt="">
</div>

<p class="big">From <span class="mark">zero</span> to your <span class="mark">first web page</span> — in one session.</p>
<p class="who">Built for students who have never written a line of code</p>

---

<!-- _class: title -->

# Today's roadmap

<div class="cards four">
<div class="card tint-coral"><h3>1 · HTML</h3>Web pages are made of HTML — and HTML is all about <b>structure</b>.</div>
<div class="card tint-blue"><h3>2 · Tags</h3>Meet the building blocks: <code>h1</code> <code>p</code> <code>img</code> <code>ul</code> <code>form</code>…</div>
<div class="card tint-green"><h3>3 · First page</h3>Create your very <b>first</b> HTML document from scratch.</div>
<div class="card tint-yellow"><h3>4 · AI</h3>It's 2026 — AI codes with us. How to use it <b>well</b>.</div>
<div class="card tint-purple"><h3>5 · Example</h3>A full page, explained line by line.</div>
<div class="card tint-coral"><h3>6 · Quiz</h3>Show what you know. No pressure!</div>
<div class="card tint-blue"><h3>7 · You code</h3>Build your own resume in HTML.</div>
<div class="card tint-green"><h3>8 · Let's go</h3>Thank you — and time to code.</div>
</div>

<!-- ============================================================
     SECTION 1 — WEB PAGES ARE HTML
     ============================================================ -->

---

<!-- _class: section s1 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 01</p>

# Web pages are HTML

<p class="sub">Every page you've ever visited — Instagram, YouTube, your school portal — is a text document written in one language.</p>

<img class="divider-ico" src="assets/icons/globe-with-meridians.svg" alt="">

---

# What is a web page, really?

<div class="cols">
<div class="col">

A web page is a **plain text file** that a browser knows how to read.

That file is written in **HTML** — the language of the web.

When you open it, the browser **reads the HTML** and **draws** (renders) the page you see.

</div>
<div class="col">

<div class="demo center">
<p class="caveat">Type it once…</p>
<p class="big"><code>HTML</code> → browser → page</p>
<img class="ico-lg" src="assets/icons/books.svg" alt="" style="display:block;margin:14px auto 0;">
</div>

</div>
</div>

<blockquote>HTML is not a programming language — it has no logic, no math. It simply <b>describes</b> what is on the page.</blockquote>

---

# HTML = the structure

<img class="float-r ico-lg" src="assets/icons/gear.svg" alt="">

Think of a page like a **house**:

<div class="cards">
<div class="card tint-coral">
<h3>HTML</h3>
The <b>walls and rooms</b>. It decides what exists and where.<br>
<span class="pill">today</span>
</div>
<div class="card tint-blue">
<h3>CSS</h3>
The <b>paint and furniture</b>. Colors, fonts, layout.<br>
<span class="pill blue">later</span>
</div>
<div class="card tint-green">
<h3>JavaScript</h3>
The <b>electricity</b>. Makes things react and move.<br>
<span class="pill green">later</span>
</div>
</div>

<p class="caveat" style="margin-top:22px;">First we build a solid structure. Decoration comes later.</p>

---

# …and HTML is based on TAGS

<img class="float-r ico" src="assets/icons/label.svg" alt="">

A **tag** is a keyword wrapped in angle brackets. Tags usually come in **pairs**:

<div class="anatomy">
<span class="br">&lt;</span><span class="name">p</span><span class="br">&gt;</span><span class="txt">Hello!</span><span class="br">&lt;/</span><span class="name">p</span><span class="br">&gt;</span>
</div>

<div class="label-row">
<div class="lab"><b>opening tag</b>starts here</div>
<div class="lab"><b>content</b>what is shown</div>
<div class="lab"><b>closing tag</b>ends it (note the <span class="slash">/</span>)</div>
</div>

Some tags carry **attributes** — extra information:

<div class="anatomy">
<span class="br">&lt;</span><span class="name">a</span> <span class="attr">href</span><span class="br">=</span><span class="val">"https://github.com"</span><span class="br">&gt;</span><span class="txt">my profile</span><span class="br">&lt;/</span><span class="name">a</span><span class="br">&gt;</span>
</div>

<div class="label-row">
<div class="lab"><b>tag name</b>what it is</div>
<div class="lab"><b>attribute</b>a setting</div>
<div class="lab"><b>value</b>in quotes</div>
<div class="lab"><b>content</b>what's clicked</div>
</div>

---

# Tags that stand alone

<img class="float-r ico" src="assets/icons/light-bulb.svg" alt="">

Some tags have **no content**, so they **close themselves**. We call them **void elements**.

<div class="cols">
<div class="col">

```html
<br>

<img src="cat.png" alt="A cat">
```

</div>
<div class="col">

- **`br`** → a line break (like pressing Enter)
- **`img`** → an image, loaded from a file
- No closing `</br>` or `</img>` — there is nothing inside them

</div>
</div>

<blockquote>Rule of thumb: if a tag <b>contains</b> something, it needs a closing tag. If it <b>is</b> something, it doesn't.</blockquote>

<!-- ============================================================
     SECTION 2 — MEET THE TAGS
     ============================================================ -->

---

<!-- _class: section s2 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 02</p>

# Meet the tags

<p class="sub">A handful of tags is enough to build a real page. Here are the ones you'll use every single day.</p>

<img class="divider-ico" src="assets/icons/label.svg" alt="">

---

# Headings — `h1` to `h6`

<div class="cols">
<div class="col">

```html
<h1>My Web Page</h1>
<h2>About me</h2>
<h3>My studies</h3>
<h4>First year</h4>
<h5>Notes</h5>
<h6>Tiny detail</h6>
```

<div class="muted">Use <b>one</b> <code>h1</code> per page. Then <code>h2</code> for main sections, <code>h3</code>… for subsections. This is the page outline.</div>

</div>
<div class="col">

<div class="demo">
<div class="d1">Heading 1</div>
<div class="d2">Heading 2</div>
<div class="d3">Heading 3</div>
<div class="d4">Heading 4</div>
<div class="d5">Heading 5</div>
<div class="d6">Heading 6</div>
</div>

</div>
</div>

<blockquote>Headings are not for making text <b>big</b> — they give the page meaning. Search engines and screen readers rely on them.</blockquote>

---

# Paragraphs & line breaks — `p`, `br`

<div class="cols">
<div class="col">

```html
<p>I am a student.</p>

<p>I study computer science.<br>
This is on a new line, same paragraph.</p>
```

- **`p`** → a paragraph. The browser adds space before and after.
- **`br`** → a line break *inside* a paragraph.

</div>
<div class="col">

<div class="demo">
<p style="margin:0 0 8px;">I am a student.</p>
<p style="margin:0;">I study computer science.<br>This is on a new line, same paragraph.</p>
</div>

<p class="caveat">Don't use lots of <code>&lt;br&gt;</code> to fake spacing — use real tags for real structure.</p>

</div>
</div>

---

# Images — `img`

<div class="cols">
<div class="col">

```html
<img src="photo.jpg" alt="My portrait">
```

- **`src`** → the path to the image file
- **`alt`** → text shown if the image fails, and read aloud by screen readers

</div>
<div class="col">

<img src="assets/icons/framed-picture.svg" alt="" style="display:block;margin:0 auto;width:150px;transform:rotate(-5deg);">

<div class="muted center"><code>alt</code> is not optional — it is how blind users "see" your image.</div>

</div>
</div>

<blockquote>A good <code>alt</code> describes the image: <code>alt="Cat sleeping on a laptop"</code>, not <code>alt="cat"</code>.</blockquote>

---

# Lists — `ul`, `ol`, `li`

<div class="cols">
<div class="col">

**Unordered** (bullets) and **ordered** (numbers):

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
</ul>

<ol>
  <li>Open the editor</li>
  <li>Write the code</li>
</ol>
```

</div>
<div class="col">

<div class="demo">
<ul style="margin:0 0 10px;">
<li>HTML</li>
<li>CSS</li>
</ul>
<ol style="margin:0;">
<li>Open the editor</li>
<li>Write the code</li>
</ol>
</div>

<p class="caveat">Every item lives in its own <code>&lt;li&gt;</code>. Lists can even nest inside each other.</p>

</div>
</div>

---

# Forms — collecting input

<div class="cols">
<div class="col">

```html
<form>
  <label for="name">Your name:</label>
  <input type="text" id="name">

  <label for="msg">Message:</label>
  <textarea id="msg"></textarea>

  <button type="submit">Send</button>
</form>
```

</div>
<div class="col">

<div class="cards wrap">
<div class="card tint-yellow"><h3><code>form</code></h3>Wraps the whole input area.</div>
<div class="card tint-blue"><h3><code>label</code></h3>Describes a field. Links to it with <code>for</code>.</div>
<div class="card tint-green"><h3><code>input</code></h3>The field itself. <code>type</code> = text, email, checkbox…</div>
<div class="card tint-purple"><h3><code>button</code></h3>Sends the form.</div>
</div>

</div>
</div>

---

# Your cheat sheet <span class="muted">(1/2)</span>

| Tag | What it does | Example |
| --- | --- | --- |
| `h1`…`h6` | Headings (1 = biggest) | `<h1>Hi</h1>` |
| `p` | Paragraph of text | `<p>Hello</p>` |
| `br` | Line break (self-closing) | `line one<br>line two` |
| `img` | Image (self-closing) | `<img src="a.png" alt="a">` |
| `ul` / `ol` | Unordered / ordered list | `<ul><li>x</li></ul>` |
| `li` | A list item | `<li>Item</li>` |

<p class="caveat">Spotted the pattern? Some tags <b>wrap</b> content, some <b>stand alone</b>.</p>

---

# Your cheat sheet <span class="muted">(2/2)</span>

| Tag | What it does | Example |
| --- | --- | --- |
| `form` | Input area | `<form>…</form>` |
| `input` | A form field | `<input type="text">` |
| `label` | Describes a field | `<label for="x">X</label>` |
| `button` | Clickable button | `<button>Send</button>` |
| `a` | A link | `<a href="…">go</a>` |

<p class="caveat">You now know more than enough HTML to build a real page!</p>

<!-- ============================================================
     SECTION 3 — YOUR FIRST HTML DOCUMENT
     ============================================================ -->

---

<!-- _class: section s3 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 03</p>

# Your first HTML document

<p class="sub">Every page on the web starts with the same skeleton. Learn it once, use it forever.</p>

<img class="divider-ico" src="assets/icons/open-book.svg" alt="">

---

# The skeleton of every page

<div class="cols">
<div class="col">

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>My first page</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
    <p>This is my very first page.</p>
  </body>
</html>
```

</div>
<div class="col">

- **`<!DOCTYPE html>`** → "this is a modern HTML page"
- **`<html>`** → the whole document
- **`<head>`** → invisible info (title, encoding, links)
- **`<title>`** → text in the browser tab
- **`<body>`** → everything you actually see

</div>
</div>

<blockquote>The <code>head</code> is the page's brain (info). The <code>body</code> is its face (visible content).</blockquote>

---

# Create it in 4 steps

<ol>
<li><b>Make a folder</b> for your project, e.g. <code>my-site</code>.</li>
<li><b>Create a file</b> called <code>index.html</code>. The <code>.html</code> ending tells the computer it's a web page.</li>
<li><b>Write</b> the skeleton, then your content, and <b>save</b>.</li>
<li><b>Open it</b> — double-click the file, or drag it into a browser. Refresh (<code>F5</code>) to see your changes.</li>
</ol>

<div class="cards">
<div class="card tint-green"><h3>Editor</h3>VS Code, or any text editor. Not Word!</div>
<div class="card tint-blue"><h3>Preview</h3>Your browser <b>is</b> the preview. No install needed.</div>
<div class="card tint-yellow"><h3>index.html</h3>The name browsers use for the home page.</div>
</div>

---

# See your mistakes — the browser Developer Tools

<img class="float-r ico-lg" src="assets/icons/keyboard.svg" alt="">

- Press **`F12`** (or right-click → *Inspect*) to open **DevTools**.
- The **Elements** tab shows the HTML as the browser understood it.
- Red errors in the **Console** help you find problems.

This is your **best friend** when something looks wrong.

<blockquote>Professional developers keep DevTools open <b>all day long</b>. Start the habit now.</blockquote>

<!-- ============================================================
     SECTION 4 — CODING WITH AI IN 2026
     ============================================================ -->

---

<!-- _class: section s4 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 04</p>

# Coding with AI in 2026

<p class="sub">You will never code alone again. AI is a co-pilot — but you are the pilot.</p>

<img class="divider-ico" src="assets/icons/robot.svg" alt="">

---

# Free AI coding tools you can use today

<div class="cards wrap">
<div class="card tint-blue"><h3>OpenCode</h3>An open-source AI coding agent in your terminal. Great for learning by asking questions.</div>
<div class="card tint-coral"><h3>Claude</h3>Excellent at explaining code and fixing mistakes you paste in.</div>
<div class="card tint-green"><h3>Gemini</h3>Google's assistant — handy for quick snippets and debugging.</div>
<div class="card tint-purple"><h3>Codex</h3>OpenAI's coding assistant, built into many editors.</div>
<div class="card tint-yellow"><h3>GitHub Copilot</h3>Free for students — autocompletes as you type.</div>
<div class="card tint-blue"><h3>Cursor</h3>An editor with AI built right in.</div>
</div>

<p class="caveat" style="margin-top:18px;">Free tiers change fast — check what your school provides, and always use your own account.</p>

---

# Be the pilot, not the passenger

<div class="cols">
<div class="col">

<div class="card tint-green">
<h3>Do <img src="assets/icons/bullseye.svg" style="width:30px;vertical-align:-6px;" alt=""></h3>
<ul>
<li>Ask AI to <b>explain</b> code line by line</li>
<li>Ask <b>"why"</b>, not just "give me the answer"</li>
<li>Run everything in the browser and test</li>
<li>Rewrite the code in your own words</li>
</ul>
</div>

</div>
<div class="col">

<div class="card tint-coral">
<h3>Don't <img src="assets/icons/cross-mark.svg" style="width:30px;vertical-align:-6px;" alt=""></h3>
<ul>
<li>Paste code you don't understand</li>
<li>Trust it blindly — it <b>will</b> be wrong sometimes</li>
<li>Give away passwords, keys or private data</li>
<li>Let it do your homework (you're learning, not it)</li>
</ul>
</div>

</div>
</div>

<blockquote>Good prompt: <i>"Show me the HTML for a page with my name as a title and a list of 3 skills, and explain every tag."</i></blockquote>

<!-- ============================================================
     SECTION 5 — A FULL EXAMPLE, EXPLAINED
     ============================================================ -->

---

<!-- _class: section s5 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 05</p>

# A full example

<p class="sub">One small page that uses everything we've seen — then we read it together.</p>

<img class="divider-ico" src="assets/icons/magnifying-glass-tilted-left.svg" alt="">

---

<!-- _class: dense -->

# The complete document <span class="muted">(1/2)</span>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Sara's page</title>
  </head>
  <body>
    <!-- notes for humans; the browser ignores this -->

    <h1>Sara Benali</h1>
    <img src="sara.jpg" alt="Portrait of Sara">
```

---

<!-- _class: dense -->

# …and the body continues <span class="muted">(2/2)</span>

```html
    <h2>About me</h2>
    <p>First-year student.<br>I love maths and music.</p>

    <h2>Skills</h2>
    <ul>
      <li>HTML</li>
      <li>Problem solving</li>
    </ul>
    <h2>Contact</h2>
    <form>
      <label for="email">Email:</label>
      <input type="email" id="email">
      <button type="submit">Send</button>
    </form>
  </body>
</html>
```

---

# Reading it line by line

| Lines | What it is | Why it matters |
| --- | --- | --- |
| `<!DOCTYPE html>` | The declaration | Tells the browser to use modern standards |
| `<html lang="en">` | The root element | `lang` helps screen readers & translators |
| `<head> … </head>` | Invisible info | Not shown, but essential |
| `<meta charset="utf-8">` | Text encoding | So accents like `é` display correctly |
| `<title>` | Tab title | Shows in the browser tab & search results |
| `<body> … </body>` | Visible content | Everything the visitor sees |
| `<!-- … -->` | A comment | Notes for you, hidden from visitors |

---

# Reading it line by line (part 2)

| Tag used | Role in the page |
| --- | --- |
| `<h1>Sara Benali</h1>` | The main title — the person's name |
| `<img src="sara.jpg" alt="Portrait of Sara">` | Adds a picture, with a description |
| `<h2>About me</h2>` | Starts a new section |
| `<p> … <br> … </p>` | A paragraph with a line break inside |
| `<ul><li>…</li></ul>` | A bullet list of skills |
| `<form>` + `<input>` + `<button>` | A way for visitors to contact Sara |

<div class="cards">
<div class="card tint-yellow"><h3>Structure</h3>Notice how headings create an outline: <code>h1</code> then several <code>h2</code>.</div>
<div class="card tint-blue"><h3>No CSS, no JS</h3>It's ugly — and that's fine. The <b>meaning</b> is already all there.</div>
</div>

<!-- ============================================================
     SECTION 6 — QUIZ
     ============================================================ -->

---

<!-- _class: section s6 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 06</p>

# Quiz time!

<p class="sub">Five quick questions. Shout out your answer — or write it down. No grades, I promise.</p>

<img class="divider-ico" src="assets/icons/question-mark.svg" alt="">

---

# Question 1

<ul class="quiz">
<li><span class="qn">1</span>What does HTML stand for?</li>
</ul>

<div class="cards wrap">
<div class="card"><b>A.</b> Hyperlinks and Text Markup Language</div>
<div class="card"><b>B.</b> HyperText Markup Language</div>
<div class="card"><b>C.</b> Home Tool Markup Language</div>
</div>

<ul class="quiz" style="margin-top:22px;">
<li><span class="qn">2</span>Which tag makes the biggest heading?
<span class="opts"><b>A.</b> <code>&lt;h6&gt;</code>  <b>B.</b> <code>&lt;head&gt;</code>  <b>C.</b> <code>&lt;h1&gt;</code></span></li>
<li><span class="qn">3</span>Which tag is <b>self-closing</b> (void)?
<span class="opts"><b>A.</b> <code>&lt;br&gt;</code>  <b>B.</b> <code>&lt;p&gt;</code>  <b>C.</b> <code>&lt;li&gt;</code></span></li>
</ul>

---

# Question 2

<ul class="quiz">
<li><span class="qn">4</span>Where do you put the content that visitors actually <b>see</b>?
<span class="opts"><b>A.</b> inside <code>&lt;head&gt;</code>  <b>B.</b> inside <code>&lt;body&gt;</code>  <b>C.</b> inside <code>&lt;title&gt;</code></span></li>
<li><span class="qn">5</span>What is the <code>alt</code> attribute for on an image?
<span class="opts"><b>A.</b> To set the image size  <b>B.</b> To describe the image  <b>C.</b> To change its colour</span></li>
<li><span class="qn">6</span>Should you paste AI code you don't understand into your project?
<span class="opts"><b>A.</b> Yes, always  <b>B.</b> Only if it runs  <b>C.</b> No — understand it first</span></li>
</ul>

---

# Answers

<ul class="quiz">
<li class="answer"><span class="qn">1</span><b>B — HyperText Markup Language.</b> "Markup" means we <i>mark up</i> content with tags.</li>
<li class="answer"><span class="qn">2</span><b>C — <code>&lt;h1&gt;</code>.</b> Headings go from <code>h1</code> (biggest) to <code>h6</code> (smallest).</li>
<li class="answer"><span class="qn">3</span><b>A — <code>&lt;br&gt;</code>.</b> It has no content, so it doesn't need a closing tag.</li>
<li class="answer"><span class="qn">4</span><b>B — inside <code>&lt;body&gt;</code>.</b> The <code>head</code> holds invisible info.</li>
<li class="answer"><span class="qn">5</span><b>B — to describe the image.</b> It also helps screen readers and shows when an image fails to load.</li>
<li class="answer"><span class="qn">6</span><b>C — no, understand it first.</b> AI is your co-pilot, not your replacement.</li>
</ul>

<!-- ============================================================
     SECTION 7 — YOUR TURN: BUILD YOUR RESUME
     ============================================================ -->

---

<!-- _class: section s7 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 07</p>

# Your turn: build your resume

<p class="sub">One HTML file. No CSS. No JavaScript. Just you, your structure, and your story.</p>

<img class="divider-ico" src="assets/icons/memo.svg" alt="">

---

# Your mission

<div class="cols">
<div class="col">

Create a file called **`resume.html`** that presents **your resume** in pure HTML.

**Rules:**

- <img src="assets/icons/check-mark-button.svg" style="width:24px;vertical-align:-4px;"> Only **HTML** — no CSS, no JavaScript, no frameworks
- <img src="assets/icons/check-mark-button.svg" style="width:24px;vertical-align:-4px;"> One single file
- <img src="assets/icons/check-mark-button.svg" style="width:24px;vertical-align:-4px;"> It must open and look correct in a browser
- <img src="assets/icons/check-mark-button.svg" style="width:24px;vertical-align:-4px;"> Use your own information (or invent a character!)
- <img src="assets/icons/check-mark-button.svg" style="width:24px;vertical-align:-4px;"> Test it before finishing

</div>
<div class="col">

<div class="card tint-yellow">
<h3>Why no CSS?</h3>
Because today is about <b>structure and meaning</b>. Ugly is fine. A solid skeleton is what matters — the pretty version comes next lesson.
</div>

<div class="card tint-green" style="margin-top:16px;">
<h3>Tip</h3>
Copy the skeleton from section 3 and grow it. Add sections one at a time and refresh often.
</div>

</div>
</div>

---

# Your page must contain…

<div class="cards four">
<div class="card tint-blue"><h3>Structure</h3><code>&lt;!DOCTYPE&gt;</code>, <code>html</code>, <code>head</code>, <code>body</code>, and a <code>title</code>.</div>
<div class="card tint-coral"><h3>Your name</h3>As an <code>h1</code>, plus <code>h2</code> headings for each section.</div>
<div class="card tint-green"><h3>A photo</h3>An <code>img</code> with a real <code>alt</code> description (a placeholder is OK).</div>
<div class="card tint-purple"><h3>A summary</h3>A <code>p</code> paragraph introducing yourself.</div>
<div class="card tint-yellow"><h3>Two lists</h3>A <code>ul</code> for skills, an <code>ol</code> for education or experience.</div>
<div class="card tint-blue"><h3>A contact form</h3><code>form</code> + <code>label</code> + <code>input</code> + <code>button</code>.</div>
<div class="card tint-coral"><h3>A line break</h3>Somewhere sensible, using <code>br</code>.</div>
<div class="card tint-green"><h3>Comments</h3>Separate your sections with <code>&lt;!-- … --&gt;</code> notes.</div>
</div>

---

<!-- _class: dense -->

# Starter skeleton <span class="muted">(1/2)</span>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>My Resume</title>
  </head>
  <body>

    <!-- Header -->
    <h1>Your Name</h1>
    <img src="me.jpg" alt="Photo of Your Name">
```

---

<!-- _class: dense -->

# Starter skeleton <span class="muted">(2/2)</span>

```html
    <!-- About -->
    <h2>About me</h2>
    <p>Write one or two sentences about yourself here.</p>

    <!-- Skills -->
    <h2>Skills</h2>
    <ul>
      <li>Your first skill</li>
      <li>Your second skill</li>
    </ul>

    <!-- Next: Education, Experience, Contact... -->

  </body>
</html>
```

<p class="caveat">Now add Education, Experience, Languages, and a Contact form. Make it yours!</p>

<!-- ============================================================
     SECTION 8 — THANK YOU
     ============================================================ -->

---

<!-- _class: section s8 -->
<!-- _footer: "" -->
<!-- _paginate: false -->

<p class="kicker">SECTION 08</p>

# Thank you!

<p class="sub">You just learned the language of the entire web. That's a big deal.</p>

<img class="divider-ico" src="assets/icons/party-popper.svg" alt="">

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

<p class="big">Open your editor. Create <code>resume.html</code>.<br>Ask AI when you're stuck — then <span class="mark">make it yours</span>.</p>

<p class="who">Questions? Hands up. Let's build.</p>

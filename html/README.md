# HTML Module — Challenges

The HTML module of the [Frontend Diploma Challenges](../README.md). Twelve
real-world practice challenges for students who have finished the HTML
fundamentals and now need to build whole pages.

Every challenge is built with **HTML only**. No CSS, no JavaScript, no
frameworks. Every page in this module is displayed with the browser's default
styling, and that is the point: when nothing is styled, the only thing holding
the page together is the structure you wrote.

**Live pages:** `https://USERNAME.github.io/REPOSITORY/html/`

---

## What each challenge gives you

- A **brief** (`README.md`) that starts with *What You Will Practice*, so you
  know exactly which concepts the task drills
- A difficulty level and a realistic time estimate
- A scenario, detailed requirements, technical rules, accessibility requirements
  and optional bonus work
- A **complete reference implementation** (`index.html`) you compare against
  *after* you have built your own
- Its own `assets/` folder, so the challenge can be opened, copied or handed out
  on its own

The briefs deliberately do **not** tell you which element to use for each piece
of content. "Create a speakers area containing three independent speaker
profiles" is the instruction; whether that is a `<section>` of `<article>`
elements is your decision to make and to defend. Choosing elements is the skill
being taught.

---

## Who it is for

Students who:

- Know the HTML elements individually, but have never structured a whole page
- Can write a form field, but not a form
- Have used `<table>`, but not `colspan`, `scope` or `<tfoot>`
- Want to be able to say *why* they chose an element, not just that it worked

You do not need CSS or JavaScript for any of this. If you already know them, you
will still learn something from being made to stop using them.

---

## How this module is organised

```text
html/
├── index.html                    ← module directory, links to all twelve
├── README.md                     ← this file
│
├── medium/
│   ├── 01-personal-portfolio/
│   ├── 02-restaurant-menu/
│   ├── 03-blog-article/
│   └── 04-product-page/
│
├── hard/
│   ├── 01-tech-conference/
│   ├── 02-job-application/
│   ├── 03-university-course/
│   └── 04-travel-booking/
│
└── advanced/
    ├── 01-ecommerce-checkout/
    ├── 02-online-course/
    ├── 03-clinic-appointment/
    └── 04-news-magazine/
```

Each challenge folder looks like this:

```text
01-personal-portfolio/
├── index.html                    ← the reference implementation
├── README.md                     ← the brief
└── assets/
    └── images/                   ← only what this challenge uses
```

Numbering restarts at `01` inside each difficulty. "Hard 03" is a complete
address for a challenge; there is no global 1-to-12 numbering to remember.

---

## Difficulty levels

| Level | Challenges | What changes |
| ----- | ---------- | ------------ |
| **Medium** | medium 01–04 | Combining what you already know. Landmarks, heading hierarchy, images and figures, the three list types, your first data table, your first form. Every requirement maps fairly directly onto markup. |
| **Hard** | hard 01–04 | Structures that do not fit a single pattern. Multi-fieldset forms with real validation attributes, tables with `colspan`, `rowspan` and `<tfoot>`, embedded audio and video, `<iframe>`, `<details>`, `<time>`, skip links. |
| **Advanced** | advanced 01–04 | Whole-document thinking. You decide the outline, the metadata, the navigation structure and the accessibility approach. Several requirements have more than one defensible answer, and the brief will not tell you which one it wants. |

---

## The HTML-only rule

This is the rule that makes the module work. In your solutions:

- ❌ No `style.css` or any other stylesheet
- ❌ No `<style>` element
- ❌ No `style` attribute
- ❌ No Tailwind, Bootstrap or any CSS framework
- ❌ No `<script>`, no event attributes, no JavaScript of any kind
- ❌ No `<center>`, `<font>`, `border="1"`, or `<br>`/`<hr>` used for spacing
- ❌ No tables for layout
- ✅ Default browser styling, correct indentation, valid nesting

Two clarifications:

- The SVG files in each challenge's `assets/images/` are **images**, exactly like
  a JPEG. Using them does not break the rule.
- ARIA is allowed only where HTML genuinely cannot express a relationship —
  labelling several navigation areas on one page, or connecting hint text to its
  field. Native semantics first, always. If you find yourself adding
  `role="button"` to a `<div>`, use a `<button>`.

CSS and JavaScript have their own modules later in the diploma. Leaving them out
here is deliberate, not a limitation.

---

## How to open a challenge

**From disk**

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
cd REPOSITORY
open html/index.html          # macOS
# xdg-open html/index.html    # Linux
# start html/index.html       # Windows
```

Opening files directly works for every challenge, because each one keeps its
media beside it. Two reference pages embed an external map, which needs an
internet connection; everything else is local.

**On GitHub Pages**

The module directory is at `https://USERNAME.github.io/REPOSITORY/html/`, and
each challenge at, for example,
`https://USERNAME.github.io/REPOSITORY/html/medium/01-personal-portfolio/`.

Challenge briefs are Markdown, so read them on GitHub itself — GitHub Pages
serves `README.md` as a plain file rather than rendering it.

Nothing in this module needs a build step, a server or a package manager.

---

## Recommended workflow

1. **Read the whole brief first.** All of it, including the accessibility
   requirements. They are requirements, not suggestions.
2. **Write the outline before the markup.** On paper or in a comment: what is the
   `h1`, what are the `h2`s, what is inside what. Ten minutes here saves an hour
   later.
3. **Build in one file**, top to bottom, structure before content detail.
4. **Do not open the reference page or its source** until you have finished. The
   whole value of the exercise is in making the decisions yourself.
5. **Test before comparing:**
   - Tab through the page. Can you reach everything? In a sensible order?
   - Read only your headings. Do they form a table of contents that makes sense?
   - Turn images off, or read only your `alt` text. Is anything lost?
   - Run the page through the [W3C validator](https://validator.w3.org/).
6. **Then compare.** Open the reference page, compare structure, and only then
   read its source.
7. **Write down every difference** and decide which markup is better. The
   reference is one competent answer, not the only one — but if you disagree with
   it, you should be able to say why in a sentence.
8. **Do the bonus tasks** for at least one challenge per level.

> Students should first read the challenge requirements, build their own
> solution, and only then compare it with the reference implementation.

---

## How to submit your solutions

Keep your work separate from the reference pages so the comparison stays honest.
Mirror the repository's own hierarchy — technology, then difficulty, then
challenge:

```text
solutions/
└── html/
    └── medium/
        └── 01-personal-portfolio/
            └── index.html
```

1. Fork this repository, or create your own from it.
2. Create a branch for each challenge:
   `git checkout -b solution/html-medium-01`.
3. Put your page in `solutions/html/<difficulty>/<challenge>/index.html`. Never
   edit a reference `index.html`.
4. Commit with a message that says what you built and what you found hard:
   `html medium 01: landmarks, dl for skills, unsure about figure vs img`.
5. Push and open a pull request against your own `main`, or against the class
   repository if your instructor asked for that.
6. In the pull request description, answer three questions:
   - Which element choice were you least sure about, and why did you choose it?
   - What did your heading outline look like?
   - What did you change after comparing with the reference?

Your instructor reviews the markup, not the appearance. A plain page with a
correct outline beats a clever page with a broken one.

---

## The twelve challenges

| Difficulty | # | Challenge | Main concepts | Estimated time |
| ---------- | - | --------- | ------------- | -------------- |
| Medium | 01 | [Personal Portfolio & CV](medium/01-personal-portfolio/) | Document head, landmarks, heading hierarchy, `figure`/`figcaption`, `ul`/`ol`/`dl`, internal and external links, `mailto:`, `tel:`, `download`, `address` | 45–60 min |
| Medium | 02 | [Restaurant Menu & Reservations](medium/02-restaurant-menu/) | Nested sections, `dl` for dishes, first data table with `caption` and `scope`, `blockquote`/`cite`, `time`, `abbr`, `small` | 60–75 min |
| Medium | 03 | [Blog Article Page](medium/03-blog-article/) | `article`, `aside`, article `header`/`footer`, breadcrumbs, in-page contents, `time`, `q`, `code`, `pre`, `kbd`, nested lists | 60–75 min |
| Medium | 04 | [Product Details Page](medium/04-product-page/) | First form: `label`, `radio`, `checkbox`, `select`, `number`, `fieldset`/`legend`, `required`, `disabled`; `details`/`summary`; `meter`; `del`/`ins`; specification table | 75–90 min |
| Hard | 01 | [Technology Conference & Registration](hard/01-tech-conference/) | Two-day schedule with `colspan`, `rowspan`, `tfoot`; multi-fieldset registration form; `date`, `tel`, `url`, `optgroup`, `pattern`, `autocomplete`; skip link; calendar download | 90–120 min |
| Hard | 02 | [Job Vacancy & Application Form](hard/02-job-application/) | `file` with `accept` and `multiple`, `select multiple`, `readonly` against `disabled`, `enctype`, row-grouped benefits table, essential against desirable structure | 90–120 min |
| Hard | 03 | [University Course & Weekly Schedule](hard/03-university-course/) | `audio` with two `source`s and fallback, `iframe` with `title`, timetable with merged cells, assessment table with a total, twelve-week `details` syllabus, `abbr` for course units | 90–120 min |
| Hard | 04 | [Travel Booking Information](hard/04-travel-booking/) | `datalist`, date ranges with `min`/`max`, priced table with `tfoot` totals, embedded map plus text directions, `lang` on individual phrases, policies in `details` | 90–120 min |
| Advanced | 01 | [E-Commerce Product & Checkout](advanced/01-ecommerce-checkout/) | Metadata, canonical, Open Graph, `data`, nested `fieldset`, `month` input, `inputmode`, `autocomplete` shipping and payment tokens, order summary with tax, `aria-describedby` | 120–150 min |
| Advanced | 02 | [Online Learning Course Platform](advanced/02-online-course/) | `video` with `poster`, two `source`s and three `track`s, captions in two languages, descriptions track, transcript, `progress` against `meter`, nested `details`, quiz form | 120–150 min |
| Advanced | 03 | [Clinic Appointment Booking](advanced/03-clinic-appointment/) | Safety-critical structure, `time` input with `step`, `dfn`, `pattern` with plain-language hints, nested group for third-party booking, availability table with row groups, `lang` on names | 120–150 min |
| Advanced | 04 | [News & Magazine Homepage](advanced/04-news-magazine/) | Homepage architecture, `hgroup`, `search`, independent `article`s, three navigation areas, `hreflang` and feed links, weather and market tables, unique link text | 120–150 min |

---

## Assets

Each challenge keeps everything it needs inside its own `assets/` folder, so no
challenge depends on another and any folder can be copied out whole. Only files
that more than one module would share belong in the repository's
[root `assets/`](../assets/README.md) folder.

- **`assets/images/`** — simple SVG placeholder graphics generated for this
  repository. Each carries a visible label so you can tell which photograph it
  stands in for. The reference pages write `alt` text as though the final
  photograph were in place: describing the intended photograph is the skill being
  practised, and it is what you do on a real project where the design lands
  before the photography does.
- **`assets/audio/`** (hard 03) — a short synthesised lecture excerpt in two
  formats, so the challenge can practise offering more than one `<source>`.
- **`assets/video/`** (advanced 02) — a five second silent time-lapse, 960 × 540,
  in MP4 and WebM. Source: [MDN shared
  assets](https://github.com/mdn/shared-assets), published under [CC0
  1.0](https://creativecommons.org/publicdomain/zero/1.0/). Included so the
  challenge works offline.
- **`assets/captions/`** (advanced 02) — WebVTT tracks: English captions, Arabic
  captions and an English text-description track. The clip is silent on purpose —
  the clearest way to show that captions carry information, not just dialogue.
- **`assets/downloads/`** — plain text and calendar files used to practise
  `<a download>` and links to non-HTML resources. They are text files so every
  asset in this repository stays readable and reviewable.
- **`assets/embeds/`** — small standalone HTML documents that a page embeds with
  `<iframe>`. They follow the same HTML-only rule as the challenges themselves.

---

## A note on the content

Everything on these pages is invented for teaching: the companies, the people,
the prices, the quotations. Nothing is real, and nothing should be read as
advice — the clinic challenge in particular is a markup exercise, not medical
guidance. Names of real organisations are not used.

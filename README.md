# HTML Challenges

Twelve real-world practice challenges for students who have finished the HTML
fundamentals and now need to build whole pages.

Every challenge is built with **HTML only**. No CSS, no JavaScript, no
frameworks. Every page in this repository is displayed with the browser's default
styling, and that is the point: when nothing is styled, the only thing holding
the page together is the structure you wrote.

**Live pages:** `https://USERNAME.github.io/REPOSITORY/` — for example
<https://USERNAME.github.io/html-challenges/>. Fork or clone this repository,
turn on GitHub Pages, and every path below works unchanged, because every link
in the repository is relative.

---

## What this repository is

A graded set of twelve briefs, each describing a page a real client might ask
for: a portfolio, a restaurant menu, a conference registration, a job
application, a checkout, a clinic booking, a newspaper homepage.

Each challenge gives you:

- A **brief** (`README.md`) that starts with *What You Will Practice*, so you
  know exactly which concepts the task drills
- A difficulty level and a realistic time estimate
- A scenario, detailed requirements, technical rules, accessibility requirements
  and optional bonus work
- A **complete reference implementation** (`index.html`) you compare against
  *after* you have built your own

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
- Have used `<table border="1">`, but not `colspan`, `scope` or `<tfoot>`
- Want to be able to say *why* they chose an element, not just that it worked

You do not need CSS or JavaScript for any of this. If you already know them, you
will still learn something from being made to stop using them.

---

## How the challenges are organised

```text
<repository root>/
│
├── index.html                    ← the challenge index, links to all twelve
├── README.md                     ← this file
│
├── medium/
│   ├── 01-personal-portfolio/    ← index.html + README.md
│   ├── 02-restaurant-menu/
│   ├── 03-blog-article/
│   └── 04-product-page/
│
├── hard/
│   ├── 05-tech-conference/
│   ├── 06-job-application/
│   ├── 07-university-course/
│   └── 08-travel-booking/
│
├── advanced/
│   ├── 09-ecommerce-checkout/
│   ├── 10-online-course/
│   ├── 11-clinic-appointment/
│   └── 12-news-magazine/
│
└── assets/
    ├── README.md                 ← what every asset is, and its licence
    ├── images/                   ← SVG placeholder graphics
    ├── audio/                    ← lecture excerpt, two formats
    ├── video/                    ← sample clip, two formats (CC0)
    ├── captions/                 ← WebVTT caption and description tracks
    ├── downloads/                ← text and calendar files for download links
    └── embeds/                   ← small HTML documents embedded with <iframe>
```

Every challenge folder contains exactly two files: the brief and the reference
page. Assets are shared, and every reference page reaches them with relative
paths such as `../../assets/images/...`, so the repository works both from disk
and from GitHub Pages.

---

## Difficulty levels

| Level | Challenges | What changes |
| ----- | ---------- | ------------ |
| **Medium** | 01–04 | Combining what you already know. Landmarks, heading hierarchy, images and figures, the three list types, your first data table, your first form. Every requirement maps fairly directly onto markup. |
| **Hard** | 05–08 | Structures that do not fit a single pattern. Multi-fieldset forms with real validation attributes, tables with `colspan`, `rowspan` and `<tfoot>`, embedded audio and video, `<iframe>`, `<details>`, `<time>`, skip links. |
| **Advanced** | 09–12 | Whole-document thinking. You decide the outline, the metadata, the navigation structure and the accessibility approach. Several requirements have more than one defensible answer, and the brief will not tell you which one it wants. |

---

## The HTML-only rule

This is the rule that makes the repository work. In your solutions:

- ❌ No `style.css` or any other stylesheet
- ❌ No `<style>` element
- ❌ No `style` attribute
- ❌ No Tailwind, Bootstrap or any CSS framework
- ❌ No `<script>`, no event attributes, no JavaScript of any kind
- ❌ No `<center>`, `<font>`, `border="1"`, or `<br>`/`<hr>` used for spacing
- ❌ No tables for layout
- ✅ Default browser styling, correct indentation, valid nesting

Two clarifications:

- The SVG files in `assets/images/` are **images**, exactly like a JPEG. Using
  them does not break the rule.
- ARIA is allowed only where HTML genuinely cannot express a relationship —
  labelling several navigation areas on one page, or connecting hint text to its
  field. Native semantics first, always. If you find yourself adding
  `role="button"` to a `<div>`, use a `<button>`.

---

## How to open a challenge

**From disk**

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
cd REPOSITORY
open index.html          # macOS
# xdg-open index.html    # Linux
# start index.html       # Windows
```

Opening files directly works for every challenge. Two reference pages embed an
external map, which needs an internet connection; everything else is local.

**On GitHub Pages**

Push the repository, then in **Settings → Pages** choose "Deploy from a branch",
branch `main`, folder `/ (root)`. Within a minute the index is at
`https://USERNAME.github.io/REPOSITORY/`, and each challenge at, for example,
`https://USERNAME.github.io/REPOSITORY/medium/01-personal-portfolio/`.
Challenge briefs are Markdown, so read them on GitHub itself — GitHub Pages
serves `README.md` as a plain file rather than rendering it.

Nothing in this repository needs a build step, a server or a package manager.

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

```text
solutions/
└── 01-personal-portfolio/
    └── index.html
```

1. Fork this repository, or create your own from it.
2. Create a branch for each challenge: `git checkout -b solution/01-portfolio`.
3. Put your page in `solutions/<challenge-folder>/index.html`. Never edit the
   reference `index.html`.
4. Commit with a message that says what you built and what you found hard:
   `01 portfolio: landmarks, dl for skills, unsure about figure vs img`.
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

| # | Challenge | Difficulty | Main concepts | Estimated time |
| - | --------- | ---------- | ------------- | -------------- |
| 01 | [Personal Portfolio & CV](medium/01-personal-portfolio/) | Medium | Document head, landmarks, heading hierarchy, `figure`/`figcaption`, `ul`/`ol`/`dl`, internal and external links, `mailto:`, `tel:`, `download`, `address` | 45–60 min |
| 02 | [Restaurant Menu & Reservations](medium/02-restaurant-menu/) | Medium | Nested sections, `dl` for dishes, first data table with `caption` and `scope`, `blockquote`/`cite`, `time`, `abbr`, `small` | 60–75 min |
| 03 | [Blog Article Page](medium/03-blog-article/) | Medium | `article`, `aside`, article `header`/`footer`, breadcrumbs, in-page contents, `time`, `q`, `code`, `pre`, `kbd`, nested lists | 60–75 min |
| 04 | [Product Details Page](medium/04-product-page/) | Medium | First form: `label`, `radio`, `checkbox`, `select`, `number`, `fieldset`/`legend`, `required`, `disabled`; `details`/`summary`; `meter`; `del`/`ins`; specification table | 75–90 min |
| 05 | [Technology Conference & Registration](hard/05-tech-conference/) | Hard | Two-day schedule with `colspan`, `rowspan`, `tfoot`; multi-fieldset registration form; `date`, `tel`, `url`, `optgroup`, `pattern`, `autocomplete`; skip link; calendar download | 90–120 min |
| 06 | [Job Vacancy & Application Form](hard/06-job-application/) | Hard | `file` with `accept` and `multiple`, `select multiple`, `readonly` against `disabled`, `enctype`, row-grouped benefits table, essential against desirable structure | 90–120 min |
| 07 | [University Course & Weekly Schedule](hard/07-university-course/) | Hard | `audio` with two `source`s and fallback, `iframe` with `title`, timetable with merged cells, assessment table with a total, twelve-week `details` syllabus, `abbr` for course units | 90–120 min |
| 08 | [Travel Booking Information](hard/08-travel-booking/) | Hard | `datalist`, date ranges with `min`/`max`, priced table with `tfoot` totals, embedded map plus text directions, `lang` on individual phrases, policies in `details` | 90–120 min |
| 09 | [E-Commerce Product & Checkout](advanced/09-ecommerce-checkout/) | Advanced | Metadata, canonical, Open Graph, `data`, nested `fieldset`, `month` input, `inputmode`, `autocomplete` shipping and payment tokens, order summary with tax, `aria-describedby` | 120–150 min |
| 10 | [Online Learning Course Platform](advanced/10-online-course/) | Advanced | `video` with `poster`, two `source`s and three `track`s, captions in two languages, descriptions track, transcript, `progress` against `meter`, nested `details`, quiz form | 120–150 min |
| 11 | [Clinic Appointment Booking](advanced/11-clinic-appointment/) | Advanced | Safety-critical structure, `time` input with `step`, `dfn`, `pattern` with plain-language hints, nested group for third-party booking, availability table with row groups, `lang` on names | 120–150 min |
| 12 | [News & Magazine Homepage](advanced/12-news-magazine/) | Advanced | Homepage architecture, `hgroup`, `search`, twelve independent `article`s, three navigation areas, `hreflang` and feed links, weather and market tables, unique link text | 120–150 min |

---

## A note on the content

Everything on these pages is invented for teaching: the companies, the people,
the prices, the quotations. Nothing is real, and nothing should be read as
advice — the clinic page in particular is a markup exercise, not medical
guidance. Names of real organisations are not used.

The images are simple SVG placeholders generated for this repository; the
`alt` text is written as though the final photographs were in place, because
writing that `alt` text is part of the exercise. Asset licences are documented in
[`assets/README.md`](assets/README.md).

---

## Licence

Briefs, reference implementations and generated assets in this repository are
free to use and adapt for teaching. The sample video in `assets/video/` comes
from [MDN shared assets](https://github.com/mdn/shared-assets) and is published
under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).

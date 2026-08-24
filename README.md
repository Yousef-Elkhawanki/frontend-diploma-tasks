# Frontend Diploma Challenges

Practice challenges for the Frontend Development Diploma: real-world tasks that
build up from a single page of markup to whole applications, one technology at a
time.

Each module contains graded challenges. Each challenge gives you a brief, a set
of requirements, and a complete reference implementation to compare against once
you have built your own.

**Live pages:** `https://USERNAME.github.io/REPOSITORY/` — fork or clone this
repository, turn on GitHub Pages, and every path below works unchanged, because
every link in the repository is relative.

---

## Modules

| Module | Status | Challenges | Guide |
| ------ | ------ | ---------- | ----- |
| [HTML](html/) | Available | 12 — four medium, four hard, four advanced | [HTML module guide](html/README.md) |
| [CSS](css/) | Available | 12 — four medium, four hard, four advanced | [CSS module guide](css/README.md) |
| JavaScript | Not started | — | — |
| TypeScript | Not started | — | — |
| React | Not started | — | — |
| Next.js | Not started | — | — |

Modules appear here as they start. Nothing is listed before its challenges exist,
so everything in this table is something a student can open today. Later modules
may include topics beyond the list above — Git and GitHub, Tailwind, performance,
frontend security — and each one slots into the same structure without changing
anything that already exists.

**Start here:** [HTML Challenges](html/), then [CSS Challenges](css/).

---

## Repository architecture

The hierarchy is always the same, four levels deep:

```text
Technology / Topic  →  Difficulty  →  Challenge  →  Challenge files
```

```text
frontend-diploma-tasks/
│
├── index.html                        ← diploma directory, links to each module
├── README.md                         ← this file
├── assets/                           ← files shared across more than one module
│   └── README.md
│
├── html/                             ← one folder per technology
│   ├── index.html                    ← module directory, links to its challenges
│   ├── README.md                     ← module guide: rules, workflow, submission
│   │
│   ├── medium/
│   │   ├── 01-personal-portfolio/
│   │   │   ├── index.html            ← reference implementation
│   │   │   ├── README.md             ← the brief
│   │   │   └── assets/               ← only what this challenge uses
│   │   ├── 02-restaurant-menu/
│   │   ├── 03-blog-article/
│   │   └── 04-product-page/
│   │
│   ├── hard/
│   │   ├── 01-tech-conference/
│   │   ├── 02-job-application/
│   │   ├── 03-university-course/
│   │   └── 04-travel-booking/
│   │
│   └── advanced/
│       ├── 01-ecommerce-checkout/
│       ├── 02-online-course/
│       ├── 03-clinic-appointment/
│       └── 04-news-magazine/
│
└── css/
    ├── index.html
    ├── README.md
    │
    ├── medium/
    │   ├── 01-recycling-guide/
    │   │   ├── index.html            ← reference implementation
    │   │   ├── styles.css            ← reference stylesheet
    │   │   ├── README.md             ← the brief
    │   │   └── assets/
    │   │       ├── design/           ← the design reference wireframe
    │   │       └── images/
    │   ├── 02-trail-hero/
    │   ├── 03-workshop-packages/
    │   └── 04-cinema-programme/
    │
    ├── hard/
    │   ├── 01-membership-form/
    │   ├── 02-gallery-wall/
    │   ├── 03-transport-landing/
    │   └── 04-pricing-plans/
    │
    └── advanced/
        ├── 01-print-catalogue/
        ├── 02-property-listings/
        ├── 03-streaming-browse/
        └── 04-saas-capstone/
```

A future module is added by creating one folder and following the same shape:

```text
javascript/
├── index.html
├── README.md
└── hard/
    └── 03-shopping-cart/
        ├── index.html
        ├── README.md
        └── assets/
```

Nothing outside that new folder has to change, except adding one row to the
module table above and one entry to the root `index.html`.

---

## Conventions

**Numbering.** Challenge numbers restart at `01` inside each difficulty, so a
challenge's address is *module → difficulty → number*: `html/hard/03`. There is
no global numbering to renumber when a challenge is inserted or moved.

**Naming.** Lowercase kebab-case everywhere, for folders and files:
`html/`, `javascript/`, `01-personal-portfolio/`, `02-restaurant-menu/`. Never
`HTML/`, `JavaScript/`, `Task 1/` or `Personal_Profile/`.

**Challenge files.** Every challenge folder contains `index.html` (the reference
implementation) and `README.md` (the brief). It may also contain `assets/`, and
whatever else its module needs — a CSS challenge adds `styles.css`.

**Assets.** If a file belongs to one challenge, it lives inside that challenge:
`html/medium/01-personal-portfolio/assets/images/`. That keeps unrelated media
from piling up together and lets a challenge folder be copied out whole. The
repository's root [`assets/`](assets/README.md) folder is reserved for files that
genuinely need to be shared between modules.

**Paths.** Relative URLs only — no leading `/` and no hard-coded domain — so the
repository works when opened from disk, served locally, or deployed to a GitHub
Pages subdirectory.

**Briefs.** Every challenge brief opens with a difficulty, a time estimate and a
*What You Will Practice* list, and never dictates which element to use for each
piece of content. Deciding that is the exercise.

---

## Reading the challenges

1. Open the module you are studying, and pick the next challenge in order.
2. Read the whole brief, including the accessibility requirements.
3. Build your own solution, from the brief alone, in your own folder.
4. Only when you have finished, open the reference page, compare structure with
   structure, and then read its source.

> Students should first read the challenge requirements, build their own
> solution, and only then compare it with the reference implementation.

Each module's guide sets out its own rules, testing steps and submission
process:

- The [HTML module](html/README.md) is solved with **HTML only** — no CSS, no
  JavaScript, no frameworks. Pages render in the browser's default styling on
  purpose.
- The [CSS module](css/README.md) is solved with **HTML and pure CSS** — an
  external stylesheet, no JavaScript, no framework and no preprocessor. Its
  challenges follow the CSS curriculum in order, and none of them needs a
  concept from a later one.

---

## Deploying

In **Settings → Pages**, choose "Deploy from a branch", branch `master`, folder
`/ (root)`. Within a minute:

| Page | URL |
| ---- | --- |
| Diploma directory | `https://USERNAME.github.io/REPOSITORY/` |
| HTML module | `https://USERNAME.github.io/REPOSITORY/html/` |
| CSS module | `https://USERNAME.github.io/REPOSITORY/css/` |
| One challenge | `https://USERNAME.github.io/REPOSITORY/css/medium/01-recycling-guide/` |

Later modules follow automatically: `/javascript/`, `/typescript/`, `/react/`
and so on.

Challenge briefs are Markdown, so read them on GitHub itself — GitHub Pages
serves `README.md` as a plain file rather than rendering it.

No module in this repository needs a build step or a package manager to be read.
If a later module needs one to *run* (React, Next.js), that module's guide will
say so, and the requirement will stay inside that module's folder.

---

## A note on the content

Everything in these challenges is invented for teaching: the companies, the
people, the prices, the quotations. Nothing is real, and nothing should be read
as advice.

The images are simple SVG placeholders generated for this repository; `alt` text
is written as though the final photographs were in place, because writing that
`alt` text is part of the exercise.

---

## Licence

Briefs, reference implementations and generated assets in this repository are
free to use and adapt for teaching. The sample video in
`html/advanced/02-online-course/assets/video/` comes from [MDN shared
assets](https://github.com/mdn/shared-assets) and is published under [CC0
1.0](https://creativecommons.org/publicdomain/zero/1.0/).

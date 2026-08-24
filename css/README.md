# CSS Module — Challenges

The CSS module of the [Frontend Diploma Challenges](../README.md). Twelve
real interfaces to build, in the order the curriculum introduces the concepts
needed to build them.

Everything here is **HTML and pure CSS**. No JavaScript, no framework, no
preprocessor, no UI library.

**Live pages:** `https://USERNAME.github.io/REPOSITORY/css/`

---

## What this module is for

The HTML module taught you to build a document. This module teaches you to
decide how it looks — and, more importantly, to decide *which CSS concept a
problem actually calls for*.

Each challenge gives you:

- A **brief** (`README.md`) opening with *What You Will Practice*, so you know
  the exact scope before you start
- A difficulty, an estimated time and a **design reference image**
- Visual, layout, styling, interaction, responsive and accessibility
  requirements — described as outcomes, not as CSS declarations
- Constraints, a testing checklist, and optional bonus work
- A **complete reference implementation**: `index.html` plus `styles.css`
- Its own `assets/` folder

The briefs never name the property you should use. "Arrange the logo and the
navigation at opposite ends of the bar" is the requirement; choosing
`justify-content: space-between` is your job.

---

## Prerequisites

- The [HTML module](../html/README.md), or equivalent: you should be able to
  write a semantic document with landmarks, headings, lists, forms and tables
  without looking things up.
- A browser with developer tools. Nothing else — no build step, no package
  manager, no account.

The reference pages' HTML is written to the standard the HTML module set. If a
challenge's markup looks unfamiliar, read it before you style it.

---

## The pure-CSS rule

In your solutions:

- ✅ One **external stylesheet** per challenge, linked with a relative path
- ❌ No `<style>` element and no `style` attribute
- ❌ No JavaScript, no `<script>`, no event attributes
- ❌ No Tailwind, Bootstrap or any CSS framework
- ❌ No Sass, Less or any preprocessor
- ❌ No CDN links of any kind — every asset is local
- ❌ No `!important` unless a brief explicitly asks you to demonstrate it

Two conventions the reference implementations follow, which you may adopt or
argue with:

- **No `box-shadow` and no gradients.** Neither appears in this module's
  curriculum, so depth is built from colour, border, spacing and scale. It is a
  useful constraint: shadows hide a lot of imprecise spacing.
- **Decoration lives in CSS.** A photograph that carries no information belongs
  in a stylesheet, not in an `<img>` tag.

---

## Curriculum progression

**Nothing in a challenge requires a concept from a later challenge.** That rule
is enforced, not aspirational — the reference stylesheets are checked against it.

| Stage | Concepts | Challenges |
| ----- | -------- | ---------- |
| 1 | Syntax, adding CSS, selectors, colour, backgrounds, borders | Medium 01–02 |
| 2 | Dimensions, units, spacing, box model, `box-sizing` | Medium 03–04 |
| 3 | Cascade, inheritance, specificity, combinators, attribute selectors, pseudo-classes | Hard 01 |
| 4 | Display, normal flow, visibility, overflow, positioning, `z-index` | Hard 02 |
| 5 | Flexbox | Hard 03–04 |
| 6 | CSS Grid | Advanced 01 |
| 7 | Responsive design, media queries, fluid units, responsive media | Advanced 02 |
| 8 | Pseudo-elements, custom properties, transitions, transforms, animations | Advanced 03–04 |

Two consequences worth knowing before you start:

- **The Medium challenges have no layout system at all.** No `display`, no
  float, no Flexbox, no Grid. Their pages are one column, in normal flow. That is
  not a simplification — it is what CSS gives you before you learn the layout
  tools, and feeling its limits is the point.
- **Hard 03 is the first challenge with Flexbox, and Advanced 01 the first with
  Grid.** Everything before them is solved with what came before them.

---

## Folder structure

```text
css/
├── index.html                    ← module directory, links to all twelve
├── README.md                     ← this file
│
├── medium/
│   ├── 01-recycling-guide/
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

Each challenge folder:

```text
01-recycling-guide/
├── index.html                    ← reference implementation
├── styles.css                    ← reference stylesheet
├── README.md                     ← the brief
└── assets/
    ├── design/design-reference.svg   ← the wireframe you build from
    └── images/                       ← only what this challenge uses
```

---

## Running it locally

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
cd REPOSITORY
open css/index.html          # macOS
# xdg-open css/index.html    # Linux
# start css/index.html       # Windows
```

Every page works opened directly from the file system — no server needed. If you
prefer one, any static server will do:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/css/
```

---

## Working with developer tools

This module is where developer tools stop being optional. For each challenge:

1. **Inspect** an element and read its box model diagram — content, padding,
   border, margin. Most early CSS bugs are visible there in five seconds.
2. **Read the Styles panel top to bottom.** It shows every rule that matched,
   in cascade order, with the losing declarations struck through. That panel is
   the cascade, made visible.
3. **Toggle a declaration** on and off rather than editing your file and
   reloading.
4. **Use the layout overlays** for Flexbox and Grid: they draw the tracks,
   the gaps and the line numbers.
5. **Emulate** a narrow viewport for the responsive challenges, and check
   `prefers-reduced-motion` under rendering emulation for Advanced 03.
6. **Check contrast** in the colour picker before you decide a palette works.

---

## Comparing against the reference

The reference is one competent answer, not the only one. When you compare:

- Compare **structure first**, then values. Did you group the same things? Did
  you name components the way you would want to maintain?
- Expect your values to differ. Padding of `1.4rem` against `1.5rem` is not a
  mistake.
- If the reference is shorter than yours, find out why: usually it means one
  rule is doing the work of four.
- If yours is shorter, check that it still holds up when the content grows.
- Read the reference's comments — they explain the decisions, not the syntax.

Do not open the reference stylesheet before your own version works. The value of
the exercise is entirely in the deciding.

---

## Submitting your solutions

Mirror the repository's hierarchy — technology, difficulty, challenge:

```text
solutions/
└── css/
    └── medium/
        └── 01-recycling-guide/
            ├── index.html
            └── styles.css
```

1. Fork the repository, or create your own from it.
2. Branch per challenge: `git checkout -b solution/css-medium-01`.
3. Never edit a reference `index.html` or `styles.css`.
4. Commit with a message that says what you built and what was hard:
   `css medium 03: box model, unsure whether the note should be centred by
   margin or by text-align`.
5. Open a pull request and answer three questions in its description:
   - Which requirement took the longest, and what did you try first?
   - Which CSS property did you learn something new about?
   - What differs between your solution and the reference, and which do you
     think is better?

Your instructor reviews the CSS, not the pixels. A stylesheet somebody else
could maintain beats a pixel-perfect one nobody can.

---

## Accessibility expectations

These apply to every challenge, and they are graded:

- **Focus states.** Every hover effect has a matching focus effect, and no
  element ever loses its focus indicator without gaining a better one.
- **Contrast.** 4.5:1 for body text, 3:1 for large text and meaningful borders.
- **Never colour alone.** A status, a required field or a selected option must
  be readable in greyscale.
- **Reflow.** No horizontal scrolling at 320px wide or at 400% zoom.
- **Text size.** The page must work when the reader's base font size is larger
  than yours; that is why sizes are in `rem` rather than `px`.
- **Motion.** Anything that moves must respect `prefers-reduced-motion`.
- **Order.** Visual order must not contradict document order. `order`,
  `grid-row` and `grid-column` can produce a tab sequence that jumps around the
  screen — check with the keyboard.

---

## Recommended order

Straight through, 01 to 04 in each band, in this order: Medium, Hard, Advanced.

If you are short of time, the four that cover the most ground are Medium 03 (box
model), Hard 03 (Flexbox), Advanced 02 (responsive) and Advanced 04 (the
capstone) — but the capstone assumes all eleven before it, so it is the one to do
last regardless.

---

## A note on the content

Every organisation, product, price and person in this module is invented for
teaching. The images are simple SVG placeholders generated for this repository,
including each challenge's design reference wireframe.

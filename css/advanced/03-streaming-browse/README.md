# Nocturne — Streaming Browse Interface

Difficulty: Advanced

Estimated Time: 130–150 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Pseudo-elements
  - `::before` and `::after`
  - The `content` property
  - Decorative overlays, badges, indicators and underlines drawn without adding
    a single element to the HTML
  - Knowing when a pseudo-element is the wrong answer, because the thing is
    content

- Custom properties
  - Declaring tokens on `:root`
  - `var()`, and `var()` with a fallback
  - Colour, spacing, radius and typography tokens
  - Local variables scoped to one component, and re-declaring a token on one
    section to re-theme it without touching any other rule

- Transitions
  - `transition-property`, `transition-duration`, `transition-timing-function`,
    `transition-delay` and the shorthand
  - Which properties are worth animating, and which cost you a repaint

- Transforms
  - `translate()`, `scale()`, `rotate()`
  - Combining transforms in one declaration
  - `transform-origin`

- Animations
  - `@keyframes`
  - `animation-name`, `-duration`, `-delay`, `-timing-function`,
    `-iteration-count`, `-direction`, `-fill-mode` and the shorthand
  - Motion that means something, next to motion that is just movement

- Everything before it
  - Grid, Flexbox, responsive design, positioning, states and selectors

- Accessibility
  - `prefers-reduced-motion`
  - Hover effects that are matched by focus effects
  - Contrast on a dark interface
  - Motion that never conveys information on its own

---

# Challenge

Nocturne is a streaming service. This is the browse screen: a billboard for the
show they are pushing this week, rails of artwork below it, and the state a
member cares about — how far through something they are, what is new, what is
live now.

Two things make this challenge different from everything before it. First, every
colour, radius and spacing step in your stylesheet must come from a token, so
that re-theming one section is a two-line change rather than a rewrite. Second,
this is the first time you may move things — and the discipline is that every
movement has to earn its place, and every one of them has to be switchable off.

---

# Design Reference

![Wireframe of a dark interface: a translucent top bar, a billboard with artwork behind a dark veil and a pulsing live indicator, two rails of cards where one card is shown lifted and brightened with a title strip sliding up, a themed panel in a different accent colour, a shimmering skeleton row, and a muted footer.](./assets/design/design-reference.svg)

**Tokens** — declare these once and use them everywhere:

| Token | Value |
| ----- | ----- |
| Page background | `#0d0f14` |
| Panel background | `#1a1e27` |
| Text | `#f2f4f8` |
| Muted text | `#8a93a6` |
| Accent | `#7b5cf0` |
| Second accent (themed panel only) | `#23c1c9` |
| Radius, small / large | `6px` / `14px` |
| Spacing steps | four, of your choosing |

**Supplied images** — `billboard-tidal.svg` (1600 × 800), ten artwork files
`art-01-…` to `art-10-…` (480 × 660), and `nocturne-logo.svg`, in
`./assets/images/`.

---

# Requirements

## Tokens

- Every colour, radius and spacing value in the stylesheet comes from a custom
  property. A literal hex value outside your token block is a defect.
- At least one component defines a *local* token that only its own rules use.
- One section re-themes itself by re-declaring a token on its own selector, with
  no other rule changed. The obvious candidate is the accent colour.
- At least one `var()` call includes a fallback, with a comment explaining when
  a fallback would actually be used.

## Top bar

- Sits over the billboard rather than above it, and lets the artwork show
  through.
- Contains the logo, navigation and a profile link.
- Stays at the top of the window when the page scrolls.

## Billboard

- The artwork fills the billboard.
- A dark veil sits over the artwork so the text on it reaches contrast. **The
  veil must be drawn with a pseudo-element**, not with an extra element and not
  by darkening the source image.
- Holds an eyebrow line, the title, a meta row, a short description and two
  buttons.
- A "live now" indicator sits in the meta row: a small dot that pulses gently,
  with the word "Live" beside it. The word carries the meaning; the dot is
  decoration.

## Rails

Two rails: "Continue watching" and "New this week".

- Each rail heading has a short accent bar before it, drawn with a
  pseudo-element.
- Cards sit in a row that reflows to fewer columns as the window narrows.
- Each card shows artwork, a title and a duration.
- Cards in the first rail show how far through the member is, as a thin bar
  along the bottom of the artwork.
- One card in the second rail carries a "New" badge drawn with a pseudo-element
  and rotated slightly.

## Card interaction

On hover **and** on keyboard focus, every card must:

- lift slightly and scale up a little,
- brighten its artwork,
- slide its title strip up so the meta line that was tucked below the edge
  comes into view — the title itself stays visible at rest,

and all of it must ease in and out rather than snapping. The resting state and
the active state must both be legible.

## Themed panel

- A "Because you watched" panel that uses the second accent everywhere its
  siblings use the first, achieved by re-declaring one token.

## Skeleton row

- Three placeholder blocks with a gentle shimmer that loops, representing
  content still loading.
- The shimmer must stop entirely when the reader has asked for reduced motion.

## Reduced motion

- A `prefers-reduced-motion: reduce` block must remove or neutralise every
  animation and transition on the page — without removing any *information*.
  The hover and focus states must still be clearly visible, just not animated.

---

# Content Requirements

Real-shaped catalogue content: show titles, episode counts, durations, ratings
and progress. Use the reference content or write your own. No Lorem ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- Decorative layers must be pseudo-elements. If a thing would be read aloud
  usefully by a screen reader, it is content and belongs in the HTML instead.
- No `box-shadow`. Depth comes from colour, border and scale.
- Animate `transform` and `opacity` in preference to properties that change
  layout, and be able to say why.
- No infinite animation that is large, fast or high-contrast.

---

# Accessibility Requirements

- Every hover effect has a matching focus effect, and focus is visible against
  the dark background.
- Text over the billboard reaches 4.5:1 *after* your veil is applied. Check it.
- The "live" state is conveyed by the word, not only by the pulsing dot.
- Progress is conveyed by a number or a label as well as by the bar.
- `prefers-reduced-motion: reduce` removes motion without removing meaning.
- Nothing flashes more than three times a second.
- Card titles are real headings and real links, not `content` strings.

---

# Bonus Challenges

1. Add a second theme by re-declaring your tokens under a class on `<body>`, and
   confirm no component rule needs to change.
2. Give the billboard buttons a transition on a border rather than a background
   and describe the difference in a comment.
3. Stagger the rail cards' entrance with `animation-delay`, keeping the whole
   sequence under half a second.
4. Draw the "New" badge's pointed corner with a second pseudo-element.
5. Replace one of your pseudo-element decorations with a real element and write
   down what you lost and what you gained.

---

# Testing Checklist

- [ ] No hex value appears outside the token block.
- [ ] Re-theming the panel is a one-declaration change.
- [ ] The veil is a pseudo-element and the billboard text passes contrast.
- [ ] Tabbing to a card produces the same effect as hovering it.
- [ ] The shimmer and the pulse both stop under reduced motion.
- [ ] The interface still works with every animation removed.
- [ ] Cards reflow from five columns to one without a horizontal scrollbar.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works.

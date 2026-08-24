# Capstone — Signal Product Landing Page

Difficulty: Advanced

Estimated Time: 150–180 Minutes

---

# What You Will Practice

This is the CSS capstone. It uses the whole module, and it is the one challenge
where nothing is off the table. You will practice:

- Semantic HTML from the HTML module, styled without being altered
- An external stylesheet organised well enough that somebody else could work in
  it
- Custom properties as a design system: colour, spacing, radius, type
- CSS Grid for the page's two-dimensional structure
- Flexbox inside components
- Responsive design, mobile first, with a small number of honest breakpoints
- Fluid sizing: `clamp()`, `min()`, `max()`, `calc()`
- Responsive media: `aspect-ratio`, `object-fit`, `max-width: 100%`
- Pseudo-elements for decoration
- Transitions and transforms for state
- One purposeful `@keyframes` animation
- `prefers-reduced-motion`
- Accessibility throughout: focus, contrast, order, reflow

---

# Challenge

Signal is a product-analytics tool. You are building their landing page: the
page a sceptical engineering manager lands on from a search result and decides,
in about eleven seconds, whether to keep reading.

Everything in this module has been building to a page like this one. It has a
sticky header that changes shape on small screens, a hero that scales smoothly
rather than in steps, a statistics strip, a feature grid where one cell is
larger than the rest, a pricing row with a highlighted plan, a testimonial, a
logo wall, and a footer that collapses from four columns to one.

Build it as a system, not as a page: tokens first, components second, page
third. The measure of success is that a colleague could add a fourth pricing
plan or a seventh feature without writing a new rule.

---

# Design Reference

![Wireframe: a sticky header with logo, centred links and a call-to-action; a hero split between fluid heading text and a product screenshot; a four-figure statistics strip; a feature grid where the first cell spans two columns and one card carries an animated live indicator; three pricing cards with the middle one highlighted and ribboned; a testimonial beside a wrapping logo wall; and a four-column footer.](./assets/design/design-reference.svg)

**Tokens**

| Token | Value |
| ----- | ----- |
| Ink (text, dark sections) | `#101828` |
| Indigo (primary accent) | `#3f4fd6` |
| Teal (secondary accent) | `#0f9d8f` |
| Amber (highlight, ribbon) | `#f2a03d` |
| Slate (muted text) | `#667085` |
| Surface / tint | `#ffffff` / `#f6f7fb` |
| Radius, small / large | `8px` / `16px` |
| Spacing | a scale of five steps |

**Supplied images** — `signal-logo.svg`, `product-dashboard.svg`,
`product-mobile.svg`, `portrait-dana-oyelaran.svg`, six `client-*.svg` and six
`icon-*.svg`, all in `./assets/images/`.

---

# Requirements

## Foundations

- Every colour, spacing step, radius and type size comes from a custom property
  declared once.
- Mobile-first: base rules are the small-screen rules; every media query is
  `min-width`; no more than three breakpoints.
- Grid governs the page and the multi-column sections; Flexbox governs the
  insides of components.

## Header

- Small screens: logo above a stacked link list and the call to action.
- From the first breakpoint: one row, logo at the left, links centred, call to
  action at the right.
- Sticky at every width, and it must never hide a focused element.

## Hero

- Two parts: text and product screenshot, stacked on small screens and side by
  side from the second breakpoint.
- The heading scales smoothly with the window between a readable minimum and a
  sensible maximum.
- A soft decorative shape sits behind the heading, drawn with a pseudo-element.
- Two calls to action side by side, wrapping when there is no room.
- The screenshot keeps its proportions at every width.

## Statistics strip

- Four figures: one column on a phone, two on a small tablet, four on a laptop.
- Each figure has a large number and a label; the label is what carries the
  meaning.

## Feature grid

Six features.

- A grid where the first feature spans two columns from the second breakpoint
  and everything else flows around it.
- Each card: icon, heading, two lines of text.
- Cards lift slightly on hover **and** on keyboard focus, with an eased
  transition.
- One card describes the live alerting feature and carries a small animated
  indicator — this is the page's one animation. It must convey nothing on its
  own, and it must stop under reduced motion.

## Pricing

- Three plans in a row that wraps to one column on small screens.
- The middle plan is highlighted, sits slightly higher, and carries a ribbon
  drawn with a pseudo-element.
- Every plan's button sits on the bottom edge of its card, aligned across the
  row.

## Testimonial and logo wall

- A quotation in a dark panel with a large decorative quotation mark drawn with
  a pseudo-element, plus a portrait, a name and a role.
- Beside it, six client logos in a wrapping row, greyed at rest.

## Footer

- Four link columns, collapsing to two and then one.
- A sign-up field and button that sit on one line until there is no room, then
  stack.
- A bottom line with the copyright and legal links at opposite ends.

---

# Content Requirements

Real-shaped product content: what the tool does, four believable statistics, six
features, three plans with prices and limits, a named testimonial with a role,
and honest small print. Use the reference content or write your own. No Lorem
ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- No `box-shadow` and no gradients: this module builds depth from colour,
  border, scale and spacing.
- Exactly one `@keyframes` animation on the page. If you want a second one,
  justify it in a comment.
- No content may be hidden to make a layout fit.
- All paths relative; the page must work opened from a file and served from a
  GitHub Pages subdirectory.

---

# Accessibility Requirements

- Every interactive element has a visible focus style at every breakpoint.
- Contrast: 4.5:1 for body text, 3:1 for large text, checked on the dark panel
  and on the highlighted plan.
- The page reflows to 320px and to 400% zoom with no loss of content and no
  horizontal scrolling.
- Visual order matches document order at every breakpoint.
- The animated indicator is decoration; the state it hints at is written in
  words.
- `prefers-reduced-motion: reduce` neutralises the animation and the
  transitions without removing any state.
- Headings form a correct outline; do not choose a heading level for its size.

---

# Bonus Challenges

1. Add a dark theme by re-declaring the tokens under a `prefers-color-scheme`
   query, changing no component rule.
2. Add a fourth pricing plan and confirm no layout rule changes.
3. Add a comparison table below pricing that scrolls sideways on a phone without
   breaking the page.
4. Replace the hero's decorative shape with an SVG background and describe the
   trade-off in a comment.
5. Audit your own stylesheet: find any literal colour or spacing value that
   escaped the token block, and any rule that is never used.

---

# Testing Checklist

- [ ] No literal colour or spacing value outside the token block.
- [ ] Every media query is `min-width`, and there are no more than three.
- [ ] The hero heading scales smoothly with no jump at a breakpoint.
- [ ] The first feature spans two columns above the second breakpoint.
- [ ] Pricing buttons line up across all three cards.
- [ ] Hover and focus produce the same visual result on cards and buttons.
- [ ] Reduced motion stops the indicator and all transitions.
- [ ] 320px and 400% zoom: no horizontal scrolling, nothing lost.
- [ ] Tab through the whole page: focus is always visible and never hidden by
      the sticky header.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works. When you have
finished this challenge you have used every part of the CSS module in one page —
which is exactly what the next modules will assume you can do.

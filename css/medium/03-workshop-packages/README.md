# Cogwheel Cycle Workshop — Service Packages

Difficulty: Medium

Estimated Time: 75–90 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- The box model
  - Content, padding, border and margin, and how they add up
  - `box-sizing`, `content-box` and `border-box`
  - Why one universal `box-sizing` rule is usually the first line of a
    stylesheet
  - Margin collapsing between stacked blocks
  - One deliberate, useful negative margin

- Dimensions
  - `width` and `height`
  - `max-width` to stop a column becoming unreadable
  - `min-height` to give a band presence
  - `min-width` and `max-width` on a constrained element

- Units, chosen on purpose
  - `px` where a value must not scale
  - `rem` for a spacing scale
  - `em` for padding that scales with its own component
  - `%` for widths relative to a parent
  - `vh` for a band measured against the window

- Centring
  - A block centred with automatic side margins
  - The difference between centring a box and centring its text

- Reinforced from challenges 01 and 02
  - Selectors, colour, borders, radius, backgrounds, typography

- Accessibility
  - Layouts that survive when the reader increases the text size
  - Spacing that keeps related things together and unrelated things apart

---

# Challenge

Cogwheel is a two-person bicycle workshop. They sell three service packages, and
they lose customers at exactly one point: the page where those packages are
described. Everything runs together, so nobody can see where one package ends
and the next begins.

This challenge is about the invisible half of CSS — the boxes. There is very
little colour work to do here. What there is to do is decide how wide things
are, how much room they have inside them, and how much air sits between them,
and then apply those decisions consistently enough that the page looks designed
rather than assembled.

You still have no layout system. Everything is a block in normal flow.

---

# Design Reference

![Wireframe: a dark header band, a centred intro column, three service package boxes stacked with equal gaps, a narrower centred booking note, an opening hours panel, a location panel, and a footer band. Annotations note that every block shares the same centred column and the same inner padding.](./assets/design/design-reference.svg)

**Palette**

| Role | Colour |
| ---- | ------ |
| Charcoal (bands, highlighted package) | `#232326` |
| Off-white (page and panel background) | `#f6f4f1` |
| Steel (secondary text) | `#5b6672` |
| Signal (accents, prices) | `#c2410c` |
| Line (borders) | `#d6d2cc` |

**Spacing**

Pick a small scale — four or five steps — and use only those steps. The gap
between two packages and the padding inside a package should be recognisably
from the same system.

**Supplied images** — `cogwheel-logo.svg` (320 × 76) and `workshop-bench.svg`
(900 × 520), both in `./assets/images/`.

---

# Requirements

## The measuring rules

- Set `box-sizing` once, at the top of the stylesheet, so that a width you write
  is the width you get. Leave a comment saying what it changes.
- Every block of page content sits inside the same centred column, with the same
  gutters on both sides at every window width.
- That column has a maximum width chosen for reading comfort, not for the size
  of your screen.

## Header band

- Full width, dark, with the logo and a tagline.
- Given presence by a minimum height measured against the window, not by an
  invented pixel height.

## Service packages

Three packages: tune-up, full service, and overhaul.

- All three are the same shape: same inner padding on all four sides, same
  corner rounding, same border treatment, same gap above and below.
- Each has a thick coloured edge on its left side.
- Inside each package, the price is visually separated from the list of what is
  included — by space, not by a line.
- The third package is highlighted with inverted colours. Its box must stay
  exactly the same size as the other two: only the colours change.
- Give the packages' inner padding a unit that scales with the package's own
  text, so that raising the package font size widens the padding with it.

## The price strip

Inside each package, the price sits in a strip that runs the full width of the
package's box, edge to edge, ignoring the package's own padding. Achieve that
without changing the package's padding.

## Booking note

- Narrower than the packages, and centred in the column by its own margins.
- Tinted background, no border.

## Opening hours

- A list of days and times inside a bordered panel.
- Rows separated by a hairline and by space, with the day in a stronger weight
  than the hours beside it.
- Aligning the hours to the right edge of the panel needs a layout tool you do
  not have yet — solve it with weight, colour and spacing instead.

## Where to find us

- The workshop photograph is capped at a maximum width and never overflows its
  panel, however wide the window.
- The address sits underneath.

## Footer band

- Full width, dark, small quiet text.

---

# Content Requirements

Use the reference page's content — three real-shaped service packages with
prices, turnaround times and what is included — or write your own of the same
kind. No Lorem ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- No layout system: no `display`, `float`, `position`, Flexbox or Grid.
- No media queries, pseudo-classes, pseudo-elements, custom properties,
  transitions or animations yet.
- No `box-shadow` and no gradients.
- No fixed heights on anything containing text.
- Do not use a `<table>` for the opening hours unless you would defend it as
  tabular data.

---

# Accessibility Requirements

- Set your page font size in a way that respects the reader's browser setting.
  A reader who has chosen larger text must get larger text.
- Increase the browser's zoom to 200%: nothing may overlap, be clipped, or force
  horizontal scrolling.
- The highlighted package must be distinguishable from the others by something
  other than colour — its heading text can say so.
- Contrast at least 4.5:1 for body text, including inside the inverted package.
- Keep the underline on links in body text.

---

# Bonus Challenges

1. Add a fourth package and prove your system works: it should need no new
   spacing decisions.
2. Set `box-sizing: content-box` on one package temporarily and write down, in a
   comment, exactly how many pixels wider it became and why.
3. Make the workshop photograph sit at 100% width up to its natural size and
   never beyond it.
4. Replace every `rem` in your spacing with `em` and describe in a comment what
   broke.

---

# Testing Checklist

- [ ] All three packages are exactly the same width and have identical padding.
- [ ] The gap between packages is one value from your scale, not a value per
      package.
- [ ] The price strip runs to the edges of its package box.
- [ ] The booking note is narrower than the packages and optically centred.
- [ ] At 200% browser zoom nothing overlaps and there is no horizontal
      scrollbar.
- [ ] Setting the browser's default font size to 24px enlarges the page rather
      than breaking it.
- [ ] The photograph never exceeds its panel.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works.

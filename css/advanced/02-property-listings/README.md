# Fairwater Property Listings

Difficulty: Advanced

Estimated Time: 130–150 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Responsive fundamentals
  - The viewport and the viewport meta tag
  - Fluid layouts against fixed ones
  - Mobile-first: writing the small-screen rules first and adding to them
  - Choosing breakpoints from where the content breaks, not from device names

- Media queries
  - `min-width` queries, and why they suit a mobile-first stylesheet
  - Changing layout, spacing and typography at a breakpoint
  - Keeping the number of breakpoints small on purpose

- Modern sizing
  - `%`, `rem`, `vw`, `vh` and `dvh`
  - `calc()`
  - `min()` and `max()`
  - `clamp()` for typography and spacing that scale without stepping

- Responsive media
  - `max-width: 100%` as the baseline
  - `object-fit` and `object-position`
  - `aspect-ratio` so a card's image keeps its shape at every width

- Responsive layout
  - Flexbox and Grid that change shape across breakpoints
  - A navigation that adapts
  - A filter column that becomes a stacked panel
  - Preventing horizontal overflow

- Reinforced
  - Grid, Flexbox, positioning, selectors and states from every earlier band

- Accessibility
  - Zoom and reflow to 320px without loss of content
  - Touch targets big enough on small screens
  - Content order that stays sensible at every width

---

# Challenge

Fairwater is an estate agent in a market town. Two thirds of their traffic is on
a phone, and their listings page was designed on a 27-inch monitor: the filters
sit in a 260px column that becomes 40px wide, the photographs squash, and the
price wraps onto three lines.

Rebuild it mobile-first. Start with the smallest screen you can and add layout
as the window earns it. The rule for this challenge is that no requirement is
met by hiding content — a phone gets everything a laptop gets, arranged
differently.

---

# Design Reference

![Wireframe showing the same page at three widths: small screens are one column with a stacked search panel and full-width cards; medium screens put the navigation in a row and the cards in two columns; large screens move the filters into a sticky side column with three cards per row.](./assets/design/design-reference.svg)

**Palette**

| Role | Colour |
| ---- | ------ |
| Green (header, footer, headings) | `#143b32` |
| Bone (page background, panels) | `#f7f5f0` |
| Brass (buttons, prices) | `#b8873b` |
| Slate (secondary text) | `#46504e` |
| Brick (alerts, "under offer") | `#a34b3a` |

**Breakpoints** — two, and you should be able to defend both:

| Width | What changes |
| ----- | ------------ |
| about 40rem | Navigation becomes a row; cards go to two columns; search fields sit side by side |
| about 62rem | Filters become a sticky column beside the results; cards go to three columns |

**Supplied images** — six properties, `property-01-…` to `property-06-…`
(800 × 560), plus `fairwater-logo.svg`, in `./assets/images/`.

---

# Requirements

## The base, before any media query

- Everything readable and usable at 320px wide with no horizontal scrolling.
- One column: header, search, filters, results, pagination, footer.
- Navigation links stacked, each an easy tap target.
- Cards full width, image on top, details underneath.

## Typography

- The page heading scales smoothly between the smallest and largest windows
  rather than jumping at a breakpoint. It must never become smaller than a
  readable minimum or larger than a sensible maximum.
- Body text stays at a fixed comfortable size; do not make body copy fluid.

## Images

- Every card image keeps exactly the same shape at every window width, whatever
  the card's width — a property photograph must never squash.
- Images fill their area and crop rather than distort.
- Choose which part of the image survives the crop.

## Search panel

- Fields stacked on small screens; on medium screens the location field takes
  the free space with the price and bedrooms fields beside it, and the button
  ends the row.
- Every field keeps its label at every width.

## Filters

- On small and medium screens, a panel above the results.
- On large screens, a column beside the results that stays in view as the
  results scroll.
- The filters must not be hidden on small screens.

## Results

- One column, then two, then three, with one gap value expressed once.
- A results count line above them, with a sort control that stays usable at
  every width.
- Each card carries a status tag — "New", "Under offer", "Chain free" — that
  reads without colour.
- A card's price, address and key facts must not wrap awkwardly at any width
  between 320px and 1600px.

## Pagination

- Centred, wrapping, with targets large enough to tap on a phone.

## Footer

- Four link columns on large screens, two on medium, one on small.
- A note line that never overflows.

---

# Content Requirements

Six real-shaped property listings with prices, addresses, bedrooms, bathrooms,
tenure and status; genuine filter groups; realistic small print. Use the
reference content or write your own. No Lorem ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- **Mobile first**: your base rules must be the small-screen rules, and every
  media query must be `min-width`. No `max-width` queries in this challenge.
- At most three breakpoints. Two is the target.
- No pseudo-elements, custom properties, transitions or animations yet — they
  are the next challenge.
- No `box-shadow` and no gradients.
- Nothing may be hidden with `display: none` to make a layout fit.

---

# Accessibility Requirements

- At 320px wide and at 400% zoom, all content and functionality remains
  available without horizontal scrolling.
- Tap targets are at least 44 × 44 CSS pixels on small screens.
- The visual order matches the document order at every breakpoint.
- Status tags say what they mean in words.
- Form fields keep visible labels at all widths; a placeholder is not a label.
- Focus styles remain visible over every background used.

---

# Bonus Challenges

1. Make the search button full width on small screens and inline from the first
   breakpoint, without duplicating its styles.
2. Add a "map view" panel that occupies the full viewport height using a unit
   that copes with a phone's disappearing address bar.
3. Give the card grid a minimum column width so it drops to two columns before
   the breakpoint if the browser window is unusually narrow.
4. Express the page's side padding as a single fluid value used everywhere.

---

# Testing Checklist

- [ ] No horizontal scrollbar at any width from 1600px down to 320px.
- [ ] The heading grows smoothly with the window, with no jump at a breakpoint.
- [ ] Card images have identical proportions at every width.
- [ ] Filters are reachable on a phone.
- [ ] The filter column sticks only on large screens.
- [ ] Zoom to 400% at 1280px wide: the page reflows to one column and nothing is
      lost.
- [ ] Every media query in the file is `min-width`.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works.

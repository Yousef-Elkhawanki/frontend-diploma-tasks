# Halftone Print Catalogue

Difficulty: Advanced

Estimated Time: 120–140 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Grid fundamentals
  - Grid containers and grid items, rows, columns, tracks, lines and cells
  - `display: grid`
  - `grid-template-columns` and `grid-template-rows`
  - The `fr` unit, mixed with fixed and percentage tracks
  - `gap`, `row-gap`, `column-gap`
  - `repeat()`

- Placement
  - `grid-column` and `grid-row`
  - `span`
  - Placing one item across several columns and rows while the rest flow

- Explicit and implicit grids
  - What the browser creates when items land outside the tracks you declared
  - `grid-auto-rows` and `grid-auto-columns`
  - `minmax()`
  - `auto-fit` against `auto-fill`, and how a grid can reflow with no media
    query at all

- Alignment in two dimensions
  - `justify-items`, `align-items`, `place-items`
  - `justify-content`, `align-content`
  - How grid alignment differs from flex alignment

- Grid and Flexbox together
  - Grid for the page and the walls, Flexbox inside each card

- Accessibility
  - Visual placement that does not contradict document order
  - Cards that stay legible when reflowed to one column

---

# Challenge

Halftone sells screen prints from a workshop in Sheffield. Their catalogue is
the whole business, and it currently reflows into a single tall column on every
screen wider than a phone, which wastes two thirds of a laptop display.

This challenge is your first two-dimensional layout. The catalogue has a
featured print that occupies a block of the grid, a wall of prints that fits as
many columns as the window can hold, and a lower section where a narrow notes
column sits beside a wide editorial column.

Media queries are the *next* challenge, and you may not use one here. Everything
must reflow through the grid's own sizing — which is a genuinely useful lesson:
a well-built grid needs far fewer breakpoints than you expect.

---

# Design Reference

![Wireframe: a header row holding a logo, navigation and a basket; a grid where a featured print spans two columns and two rows with four smaller prints beside it; a wall of eight cards that fits as many columns as the window allows; a lower section with a narrow sidebar beside a wide editorial column; and a footer of link columns.](./assets/design/design-reference.svg)

**Palette**

| Role | Colour |
| ---- | ------ |
| Ink (header, footer, text) | `#191919` |
| Paper (page background) | `#faf8f5` |
| Olive (featured print, accents) | `#5c6b3f` |
| Clay (prices, basket) | `#a4553a` |
| Line (borders) | `#ded7cb` |

**Supplied images** — `featured-viaduct.svg` (1000 × 700), eight prints
`print-01-…` to `print-08-…` (640 × 800), and `halftone-logo.svg`, all in
`./assets/images/`.

---

# Requirements

## Page header

- Logo, navigation and basket on one row, arranged with a grid rather than with
  Flexbox — this is a good place to feel the difference between the two.
- The navigation takes the free space; the logo and basket take only what they
  need.

## Featured print

- The featured print occupies a block two columns wide and two rows tall of a
  four-column grid.
- Four smaller prints fill the remaining cells beside it, in document order.
- On a narrow window the whole arrangement becomes one column with no media
  query. Decide what the featured item should do there and make it deliberate.
- The featured block's caption sits at the bottom of its cell, not floating in
  the middle of it.

## The print wall

- Eight cards.
- The wall fits as many columns as the window allows, each column at least a
  readable minimum width, growing to share the leftover space.
- Every card in a row is the same height regardless of how long its title is,
  and the price sits on the bottom edge of every card.
- One gap value governs both directions.
- Adding a ninth print must require no change to the CSS.

## Notes and editorial

- A narrow "printing and framing" column beside a wide editorial column, in a
  ratio of roughly one to two.
- Both columns' content starts at the top, and the section must become one
  column on a narrow window without a media query.

## Footer

- Four link columns laid out on a grid, collapsing to fewer columns as the
  window narrows, again with no media query.

---

# Content Requirements

Real-shaped catalogue content: print titles, editions, paper stock, sizes and
prices; a workshop editorial; framing and delivery notes. Use the reference
content or write your own. No Lorem ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- **No media queries.** Every reflow must come from the grid's own sizing.
- No pseudo-elements, custom properties, transitions or animations yet.
- No `box-shadow` and no gradients.
- Flexbox is allowed *inside* a card or a small component. The page's
  two-dimensional structure must be Grid.
- No fixed heights on cards.

---

# Accessibility Requirements

- Grid placement must not reorder content in a way that contradicts the document
  order a screen reader follows. If you place an item out of order, be able to
  justify it.
- Every card's link text identifies the print; "view" repeated eight times does
  not.
- Card images keep their proportions when the column width changes.
- Text stays at least 4.5:1 against every background, including over the olive
  featured block.
- At 200% zoom the grid must reflow rather than clip.

---

# Bonus Challenges

1. Rebuild the print wall with `auto-fill` instead of `auto-fit` and describe in
   a comment what changes when there are only two prints.
2. Make the second row of the featured block hold two half-height prints using
   the implicit grid.
3. Add a sold-out overlay to one card using the positioning skills from Hard 02.
4. Give the wall a "masonry-ish" feel by letting one card span two rows, and
   explain what that does to the cards after it.

---

# Testing Checklist

- [ ] The featured print spans two columns and two rows on a wide window.
- [ ] The wall adds and removes columns as the window resizes, with no media
      query anywhere in the file.
- [ ] Every card's price sits on its bottom edge and lines up across the row.
- [ ] Adding a ninth card needs no CSS change.
- [ ] The notes and editorial columns are roughly 1:2 and stack when narrow.
- [ ] No horizontal scrollbar from 1600px down to 320px.
- [ ] Tab order still matches the reading order.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works.

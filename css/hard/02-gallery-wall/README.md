# Kilnworks Gallery Wall

Difficulty: Hard

Estimated Time: 100–120 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Normal flow and `display`
  - How block and inline boxes behave before you change anything
  - `display: block`, `inline`, `inline-block`
  - Laying a wall of tiles out with `inline-block` — the layout tool that
    existed before Flexbox, and the reason Flexbox was invented
  - `display: none` and when it is the wrong answer

- Visibility and overflow
  - `visibility: hidden` against `display: none`
  - `overflow: hidden`, `auto` and `scroll`
  - A panel that scrolls inside itself instead of stretching the page
  - Clipping an image to a tile

- Positioning
  - `static`, `relative`, `absolute`, `fixed` and `sticky`
  - `top`, `right`, `bottom`, `left` and `inset`
  - Containing blocks: which ancestor an absolutely positioned box is measured
    against, and how you choose it

- Layering
  - `z-index`, stacking order, and what creates a stacking context
  - Deliberate overlap between two elements

- Reinforced
  - Selectors and states from Hard 01, plus the whole Medium band

- Accessibility
  - Content hidden visually but kept for screen readers, done correctly
  - A sticky bar that never traps or covers what a keyboard user is focused on
  - Overlays that keep their contrast

---

# Challenge

Kilnworks is a ceramics gallery. Their exhibition page lists twenty-eight works,
and at the moment it is twenty-eight stacked blocks: one screen per pot.

Rebuild it as a wall. Tiles sit beside each other and wrap; each tile carries a
caption strip across its foot and a status badge in its corner; one work is
featured and deliberately breaks the grid by overlapping its neighbours; a
filter bar follows you down the page; and the full catalogue list is a panel
that scrolls inside itself rather than adding two metres to the page.

Flexbox is the next challenge, not this one. Everything here is done with
`display`, `position`, `overflow` and `z-index` — which is exactly how this was
built for fifteen years, and knowing it is what makes Flexbox feel like a relief.

---

# Design Reference

![Wireframe: a dark header band, a sticky filter bar underneath it, two rows of four tiles with caption strips and corner badges, one tile taller and overlapping its neighbours, a scrolling catalogue panel, a curator note with a tag overlapping the portrait, and a footer band.](./assets/design/design-reference.svg)

**Palette**

| Role | Colour |
| ---- | ------ |
| Black (bands, tile captions) | `#101014` |
| White (page background) | `#fbfbfd` |
| Sand (tile background, borders) | `#d8cfc0` |
| Terracotta (badges, accents) | `#b4562f` |
| Slate (sticky bar, quiet text) | `#3c4149` |

**Supplied images** — eight works, `work-01-…` to `work-08-…` (520 × 620), plus
`curator-portrait.svg` (280 × 280), all in `./assets/images/`.

---

# Requirements

## The wall

- Tiles sit side by side and wrap onto new rows when the window narrows, down to
  one tile per row on a phone-width window.
- Each tile has a fixed width; heights may differ.
- Tiles align to their tops, not their baselines. (This is the classic
  `inline-block` trap. Find the property that fixes it.)
- The gaps between tiles must be even, and must not be created by whitespace in
  the HTML. Prove it by reformatting the HTML and confirming nothing moves.

## Each tile

- The work's photograph fills the tile's picture area and is clipped to it, with
  no distortion and no overflow.
- A caption strip sits across the bottom of the picture area, over the image,
  with the title and the medium. It must stay readable over any of the eight
  images.
- A status badge sits in the top-right corner of the tile, overlapping the
  picture, saying "Sold", "Reserved" or "Available". It is positioned against
  its own tile, not against the page — make sure you have chosen the containing
  block deliberately.
- The price sits under the picture area.

## The featured work

- One tile is larger than the others and overlaps its neighbouring tiles
  slightly.
- It must sit above them, and its badge above everything on the tile.
- Deciding what "above" means here is a stacking question, not a guess: be able
  to say why your `z-index` values work.

## Filter bar

- Sits directly under the page header, and sticks to the top of the window once
  the page scrolls past it.
- Stays above the tiles as they pass under it.
- Must not cover the content a keyboard user has just focused: check by tabbing
  through the wall with the bar stuck.

## Catalogue panel

- Lists all twenty-eight works.
- Has a fixed height of roughly a screen and scrolls inside itself; the page
  itself must not grow.
- The panel's own heading must stay visible while its list scrolls.

## Curator note

- A portrait with a "Curator" tag that overlaps its lower edge.
- The tag is positioned against the portrait, and the portrait must be the
  element that establishes that.

## One hidden thing, done twice

The page contains a "Now showing" banner in the HTML that this design does not
display.

- Hide it in a way that keeps it in the accessibility tree and reserves no
  space, and explain in a comment why the two obvious properties — `display:
  none` and `visibility: hidden` — are both wrong for that job.

---

# Content Requirements

Twenty-eight real-shaped ceramics works with titles, media, dimensions, prices
and availability; a real curator's note; genuine exhibition dates and admission
information. Use the reference content or write your own. No Lorem ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- **No Flexbox and no Grid.** They arrive in the next challenges; this one is
  about what came before them.
- No media queries, pseudo-elements, custom properties, transitions or
  animations yet.
- No `box-shadow` and no gradients.
- Do not use a negative `z-index` to solve an overlap; understand the stacking
  order instead.
- Relative paths only.

---

# Accessibility Requirements

- The sticky bar must not hide the focused element when tabbing. If it does,
  give the page a way to compensate.
- Hidden content is either hidden from everyone or visible to everyone: never
  visible to screen readers but focusable and off-screen with no indication.
- The caption strip over each image must reach 4.5:1 against the image behind
  it. The tile backgrounds are supplied light, so a solid or heavily tinted
  strip is expected.
- Badges must state their meaning in words, not by colour alone.
- The scrolling panel must be reachable and scrollable by keyboard.
- Do not set a fixed height on any tile's text.

---

# Bonus Challenges

1. Add a "back to top" control fixed to the bottom-right corner of the window,
   and make sure it never covers the last tile's badge.
2. Give the featured tile a caption that overhangs the tile's left edge without
   causing horizontal scrolling.
3. Add a second sticky element inside the catalogue panel — its own column
   headings — and work out why it sticks to the panel and not to the window.
4. Replace `inline-block` with `display: inline` on the tiles and write down in
   a comment every single thing that breaks.

---

# Testing Checklist

- [ ] Tiles wrap cleanly at every window width from 1400px down to 320px.
- [ ] Tile tops align; nothing sits on a baseline.
- [ ] Reformatting the HTML (removing newlines between tiles) changes nothing.
- [ ] Badges stay in their own tile's corner when the page is scrolled and
      zoomed.
- [ ] The featured tile overlaps its neighbours and is fully clickable.
- [ ] The filter bar sticks, stays above the tiles, and does not swallow focus.
- [ ] The catalogue panel scrolls internally; the page does not grow.
- [ ] Tabbing through the page never leaves the focused element hidden.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works.

# Fell Ridge Trail

Difficulty: Medium

Estimated Time: 75–90 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Backgrounds, in depth
  - `background-color`
  - `background-image`
  - `background-repeat`, including deliberate tiling
  - `background-position`, with keywords and with lengths
  - `background-size`, including `cover` and `contain`
  - `background-attachment`, and what `fixed` does to a full-width band
  - The `background` shorthand, and when writing it out is clearer

- Borders and shape
  - `border` shorthand and single-side borders
  - `border-radius` for rounded panels
  - A fully circular shape and a pill shape from `border-radius` alone

- Colour
  - `rgba()` for text that sits on a photograph
  - Keeping contrast when text is over an image

- Reinforced from challenge 01
  - Element, class and ID selectors, grouping, multiple classes
  - Comments, `margin`, `padding`, typography basics

- Accessibility
  - Text over photography that still reaches contrast requirements
  - Background images that carry no information the text does not also carry
  - Nothing that depends on hovering or on colour alone

---

# Challenge

Fell Ridge is a nine-mile walk in the Pennines. The national park authority wants
one page for it: what the walk is, how hard it is, what you pass, and what to
take.

Photography is the whole point of the page — the walk sells itself — so this
challenge is about doing something *with* images rather than just placing them.
Two of the photographic bands must stay still while the page scrolls over them,
which is a background problem, not a layout problem.

You still have no layout tools. The page is one column: full-width bands
alternating with a narrower column of text. All of your work is in colour,
backgrounds, borders and spacing.

---

# Design Reference

![Wireframe: a tall hero band with a photograph behind centred text, a narrower intro column, three stacked fact panels each with a round badge on the left, a second full-width photographic band with a quotation, two stage panels with a tiled pattern background, a practical information box, and a footer band.](./assets/design/design-reference.svg)

**Palette**

| Role | Colour |
| ---- | ------ |
| Forest (bands, headings) | `#1d3b2a` |
| Deep (second band, footer) | `#0f1f17` |
| Mist (page and panel background) | `#f2f5f1` |
| Stone (borders, quiet text) | `#7d8a80` |
| Sun (accents, the button) | `#e0a33e` |

**Supplied images** — in `./assets/images/`

| File | What it is |
| ---- | ---------- |
| `hero-fell-ridge.svg` | Wide landscape for the hero band. Already darkened, so white text on it reaches contrast. |
| `band-summit-cairn.svg` | Wide landscape for the quotation band, also darkened. |
| `pattern-contours.svg` | An 80 × 80 tile of contour lines, meant to repeat. |
| `badge-distance.svg`, `badge-ascent.svg`, `badge-time.svg` | Round 72 px badges for the three fact panels. |

---

# Requirements

## Hero band

- Full width of the window, tall enough to feel like a photograph rather than a
  strip — roughly a third to a half of a laptop screen.
- The landscape image covers the whole band at any window width, is not
  distorted, and is not tiled.
- The interesting part of the photograph stays visible as the window narrows:
  choose which part of the image the band should hold on to.
- **The photograph must not move when the page scrolls.** The text scrolls over
  a stationary image.
- Holds the trail name, a one-line summary, and a pill-shaped link to the route
  description further down the page.

## Fact panels

Three panels: distance, ascent, and time on foot.

- Each panel is a rounded box on the pale background, with a thin border.
- Each carries its round badge image on the left-hand side of the panel,
  vertically centred, at its natural size, not repeated, and not stretched.
- The panel's text must never run underneath its badge, at any window width or
  text length.

## The quotation band

- A second full-width photographic band, shorter than the hero.
- The photograph is also held still while the page scrolls, so that scrolling
  from the fact panels to the stages passes over a fixed image.
- Contains a quotation from a ranger and their name.

## Stage sections

Two sections describing the two halves of the walk.

- Both use the contour tile as a repeating background behind their text.
- The tile must read as a texture, not as a picture: it repeats, it is small,
  and the text stays comfortably readable over it.
- Give the two sections different background positions so the texture does not
  look mechanically identical.

## Practical information

- A bordered box with generous inner padding and rounded corners, on the plain
  background.
- A short list of what to take, and a warning about the weather.

## Footer band

- Full width, dark, small quiet text.

---

# Content Requirements

The reference page's content is a real-shaped walk description: route, distance,
ascent, terrain, stages, parking, and safety. Keep it, or write content of the
same kind. No Lorem ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- No layout system: no `display`, `float`, `position`, Flexbox or Grid. The
  bands are block elements in normal flow.
- No media queries, pseudo-classes, pseudo-elements, custom properties,
  transitions or animations yet.
- No `box-shadow` and no gradients. If a photograph needs to be darker, it is
  supplied darker.
- Do not add an image to the HTML that is decorative — a decorative photograph
  belongs in the stylesheet.
- Relative paths only. Note that a path inside a stylesheet is resolved from
  the stylesheet's own location, not from the page's.

---

# Accessibility Requirements

- Text over both photographic bands must reach 4.5:1 contrast (3:1 for the large
  hero title). The supplied images are pre-darkened to make this achievable.
- The photographs are decorative: the page must still make complete sense with
  every background image switched off.
- Any image that *does* carry information stays in the HTML with real `alt`
  text.
- The pill link must be recognisable as a link from its text, not only from its
  shape.
- Do not set a fixed height on a text-bearing box.

---

# Bonus Challenges

1. Give the hero a background colour in the same family as the photograph, so
   that on a slow connection the band never flashes white.
2. Add a fourth fact panel — "terrain" — with a badge of your own making, drawn
   as an SVG.
3. Make the contour texture sit only along the top edge of a section rather than
   across the whole of it.
4. Try `contain` instead of `cover` on the hero and write two sentences in your
   stylesheet's comments about what changed and why.

---

# Testing Checklist

- [ ] Scroll the page slowly: two bands hold their photograph still, and the
      rest of the page scrolls normally.
- [ ] Resize the window from wide to narrow — nothing is stretched, squashed or
      accidentally tiled.
- [ ] Add three more sentences to a fact panel: the text never slides under the
      badge.
- [ ] Switch off background images in the browser: the page is still complete
      and readable.
- [ ] Contrast checked on both photographic bands.
- [ ] No horizontal scrollbar at any width.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works. Note that on
some touch devices a fixed background falls back to scrolling with the page —
that is the browser's decision, not a mistake in your CSS.

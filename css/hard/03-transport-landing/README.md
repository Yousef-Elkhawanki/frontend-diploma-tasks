# Loop — City Transport App Landing Page

Difficulty: Hard

Estimated Time: 100–120 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Flexbox containers
  - `display: flex` and `inline-flex`
  - The main axis and the cross axis, and what changes when you swap them
  - `flex-direction`
  - `justify-content` and `align-items`
  - `flex-wrap` and `align-content`
  - `gap`, `row-gap` and `column-gap`

- Flex items
  - `flex-grow`, `flex-shrink`, `flex-basis` and the `flex` shorthand
  - `align-self` for the one item that breaks the row
  - `order`, and why changing visual order without changing the HTML is
    something to use carefully

- Realistic Flexbox patterns
  - A navigation bar with a logo at one end and links at the other
  - A hero split into two halves
  - A row of cards that are all the same height, whatever their content
  - Media objects: an icon beside a block of text, tops aligned
  - A footer of columns that wrap on narrow windows

- Reinforced
  - Positioning and stacking from Hard 02, the selector work from Hard 01, and
    the whole Medium band

- Accessibility
  - Visual order matching document order
  - Focus states on every interactive element
  - Layouts that survive text being enlarged

---

# Challenge

Loop is a city transport app: live departures, tickets, and step-free route
planning. The marketing page they have is a single column that works on a phone
and looks abandoned on a laptop.

This is the challenge where you get a layout system. Everything you fought with
in the gallery wall — even gaps, equal heights, vertical centring, aligning two
things at opposite ends of a bar — is one property away now.

The test is not whether you can make Flexbox work. It is whether you can stop
using it where it does not belong.

---

# Design Reference

![Wireframe: a navigation bar with the logo on the left and links plus a button on the right, a hero split into a text half and an image half, a centred section heading above three equal-height feature cards, two media rows with an icon on one side and text on the other, and a footer of four columns.](./assets/design/design-reference.svg)

**Palette**

| Role | Colour |
| ---- | ------ |
| Indigo (navigation, hero image half) | `#23306b` |
| Ink (footer, headings) | `#12172b` |
| Sky (hero text half, tinted rows) | `#eef2fb` |
| Teal (primary buttons, one icon) | `#157a72` |
| Coral (second icon, accents) | `#e2603f` |

**Supplied images** — `loop-logo.svg`, `hero-app-screens.svg`, three
`icon-*.svg` at 96 px, and two `feature-*.svg`, all in `./assets/images/`.

---

# Requirements

## Navigation bar

- Logo at the left-hand end, links in the middle or at the right, and a
  call-to-action button at the far right.
- Everything on one line, vertically centred against each other, with even
  spacing between the links.
- The bar keeps working when a link is added or removed — no fixed widths, no
  hand-tuned margins between individual links.
- On a narrow window the bar must wrap rather than overflow.

## Hero

- Two halves: text on one side, the app screenshot on the other.
- The text half's content is vertically centred against the image half.
- The two buttons in the text half sit side by side, with a gap, and wrap onto
  two lines when there is no room.
- On a narrow window the halves stack, text first. Do this without a media
  query — the wrapping behaviour of a flex container can do it for you.

## Feature cards

Three cards: live departures, tickets, step-free routes.

- All three are the same height even though their text lengths differ.
- Each card's button sits on the bottom edge of the card, aligned with the
  buttons in the other cards, regardless of how much text is above it.
- Cards wrap onto new lines on narrow windows and share one gap value.
- Each card has an icon above its heading.

## Media rows

Two rows explaining the journey planner and the ticket wallet.

- Each row is an icon or image beside a block of text, with their tops aligned,
  not their centres.
- The second row is the mirror image of the first — image on the opposite side —
  **without changing the order of the elements in the HTML**. Use the property
  designed for that, and note in a comment why doing this to whole blocks of
  content is a decision that needs care.

## Statistics strip

- Four figures in a row, evenly distributed across the full width.
- They wrap to two lines on a narrow window, and the leftover items stay
  centred rather than stranded at one end.

## Footer

- Four columns of links, spread across the width, wrapping on narrow windows.
- Inside each column the links are stacked with an even gap.
- A bottom line with the copyright, pushed to one side, and the legal links
  pushed to the other.

---

# Content Requirements

Real-shaped product content: what the app does, what it costs, which cities it
covers, accessibility features, and how to get it. Use the reference content or
write your own. No Lorem ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- **No Grid.** Grid is the next band; every two-dimensional-looking arrangement
  here must be built from one-dimensional flex containers, and noticing where
  that is awkward is part of the lesson.
- No media queries yet: the page must adapt through wrapping and flexible sizes
  alone.
- No pseudo-elements, custom properties, transitions or animations yet.
- No `box-shadow` and no gradients.
- No fixed heights on anything containing text.

---

# Accessibility Requirements

- Every link and button has a visible focus style.
- Reordering with `order` must not make the tab order illogical. Check by
  tabbing: if focus jumps around the screen, reconsider.
- Enlarge text to 200%: rows must wrap rather than clip or overlap.
- Buttons that are actions are `<button>`; things that navigate are links.
- Contrast: white text on the indigo and teal, dark text on the sky tint.
- No horizontal scrollbar at any width from 1600px down to 320px.

---

# Bonus Challenges

1. Make the navigation links stack under the logo below a certain width, still
   without a media query.
2. Give one feature card a "most used" ribbon using positioning from Hard 02.
3. Rebuild the statistics strip with `space-around`, then `space-evenly`, and
   describe the difference in a comment.
4. Add a fourth feature card and confirm nothing needed adjusting.
5. Make the hero image half fixed at a third of the width while the text half
   takes the rest, using only the `flex` shorthand.

---

# Testing Checklist

- [ ] Navigation stays on one line on a laptop and wraps sensibly on a phone.
- [ ] Hero halves stack on narrow windows, text first, with no media query.
- [ ] All three feature cards are exactly the same height, and their buttons
      line up.
- [ ] Deleting one navigation link changes nothing about the spacing of the
      others.
- [ ] The mirrored media row is mirrored by CSS, not by moving HTML.
- [ ] Tab order still follows the document, and every stop is visible.
- [ ] No horizontal scrollbar from 1600px to 320px.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works.

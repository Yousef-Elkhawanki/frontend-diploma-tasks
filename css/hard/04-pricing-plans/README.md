# Meridian Field Kit — Pricing

Difficulty: Hard

Estimated Time: 110–130 Minutes

---

# What You Will Practice

This challenge brings the whole Hard band together. You will practice:

- Flexbox under pressure
  - Equal-height cards where one card is deliberately taller
  - `align-items`, `align-self` and `align-content` doing different jobs
  - A wrapping row whose last line stays centred
  - `flex-grow`, `flex-shrink` and `flex-basis` chosen rather than guessed
  - Pinning an element to the bottom of a flex column

- Positioning and layering, combined with Flexbox
  - A ribbon that overlaps the top edge of a card
  - A corner flag clipped to its card
  - A raised card drawn above its neighbours
  - A sticky header that stays above everything as the page scrolls
  - Stacking contexts, and how a `z-index` can be trapped inside one

- Selector and state work from Hard 01
  - Structural pseudo-classes for the row that alternates
  - Hover and focus states on every interactive element

- Accessibility
  - A sticky bar that does not swallow the focused element
  - A "most popular" claim that is text, not just a colour
  - Contrast inside the highlighted card

---

# Challenge

Meridian sells a field-survey kit as three subscription plans. Their current
pricing page loses people at the same point every time: the three plans are the
same size, the recommended one is recommended in six-point grey, and the add-ons
below it are a bulleted list.

Rebuild the page so that the middle plan is unmistakably the one they mean —
raised, badged and slightly larger — while every plan card still lines up with
the others, and the whole thing still works when a plan is added or removed.

Everything you need is from this band: Flexbox for the arrangement, positioning
for the badges and the sticky bar, and stacking for what sits above what.

---

# Design Reference

![Wireframe: a sticky header with a logo, links and a trial button; a centred page heading; a two-option billing toggle; three plan cards with the middle one raised, bordered and carrying a ribbon that overlaps its top edge; a wrapping row of five add-ons; a questions section; and a footer of links.](./assets/design/design-reference.svg)

**Palette**

| Role | Colour |
| ---- | ------ |
| Violet (highlight, accents) | `#4c3a8f` |
| Ink (header, footer, text) | `#1b1729` |
| Cloud (page tint, panels) | `#f6f5fb` |
| Mint (primary buttons, included ticks) | `#17795e` |
| Amber (add-on markers, corner flag) | `#d98324` |

**Supplied images** — `meridian-logo.svg`, `icon-included.svg` and
`icon-addon.svg` in `./assets/images/`.

---

# Requirements

## Sticky header

- Logo on the left, links in the centre, trial button on the right, all
  vertically centred, wrapping on narrow windows.
- Sticks to the top of the window for the whole page and stays above every card,
  including the raised one.
- Must not hide a focused element when tabbing.

## Billing toggle

- Two options, monthly and yearly, sitting side by side inside a rounded track,
  centred on the page.
- They are links, not buttons, since this reference page has no scripting — the
  current one is marked as current in the markup and must look chosen.

## Plan cards

Three plans: Field, Survey and Atlas.

- The three cards sit in one row, wrapping to one column on narrow windows.
- All cards are the same height. The middle one is deliberately taller and wider
  and must stay vertically centred against the others, not stretched to match
  them.
- Inside every card: a name, a price block, a short description, a list of
  what is included, and a button that sits on the bottom edge of the card,
  aligned across all three cards.
- The middle card carries a "Most popular" ribbon that overlaps its top edge —
  half on the card, half above it — and where the cards meet on a narrow window
  the raised one must be drawn above its neighbours.
- The third card carries a small corner flag that is clipped to the card's
  rounded corner rather than sticking out of it.
- Adding a fourth plan must not require any new positioning rules.

## Add-ons

- Five add-ons in a wrapping row.
- On a line that is not full, the remaining items stay centred rather than
  stranded at the left.
- Each add-on is a small panel with a marker, a name, a price and one line of
  description.

## Questions

- Rows of a question and its answer, with the question narrower than the answer
  and their tops aligned.
- Alternate rows are tinted, selected by position rather than by a class.

## Footer

- Link groups spread across the width, wrapping, with a bottom line holding the
  copyright at one end and legal links at the other.

---

# Content Requirements

Three real-shaped plans with prices, limits and included features; five add-ons;
five genuine pricing questions. Use the reference content or write your own. No
Lorem ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- **No Grid** and **no media queries** — the page must adapt by wrapping.
- No pseudo-elements, custom properties, transitions or animations yet. The
  ribbon and the flag are real elements in the HTML.
- No `box-shadow` and no gradients: the raised card is raised by size, border,
  colour and stacking, not by a shadow.
- No fixed heights on cards.

---

# Accessibility Requirements

- "Most popular" must be readable text inside the ribbon, not a coloured shape.
- The highlighted card's text must reach 4.5:1 against its tinted background.
- Every link and button has a visible focus style, including inside the sticky
  header.
- Tab through the page with the header stuck: nothing focused may end up hidden
  underneath it.
- The chosen billing option must be distinguishable without colour.
- At 200% text size, cards must wrap rather than clip, and the ribbon must not
  cover the plan name.

---

# Bonus Challenges

1. Add a fourth plan and confirm the layout and the badges still work untouched.
2. Make the ribbon sit on the card's top-left corner at an angle — using
   positioning only, since transforms are not in this band yet.
3. Give the add-on row a "see all" panel that always sits last, whatever the
   wrapping.
4. Work out why giving the sticky header a `z-index` of 1 is enough, but giving
   the raised card a `z-index` of 999 might still not put it above the header.

---

# Testing Checklist

- [ ] All three cards' buttons sit on one line across the row.
- [ ] The middle card is taller and centred, not stretched.
- [ ] The ribbon overlaps the card's top edge and stays attached when the page
      is zoomed to 200%.
- [ ] The corner flag is clipped by the card's rounded corner.
- [ ] The add-on row's last line is centred.
- [ ] The header stays above every card while scrolling.
- [ ] Tabbing never leaves focus hidden behind the header.
- [ ] No horizontal scrollbar from 1600px to 320px.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works.

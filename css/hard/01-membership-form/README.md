# Brackenfield Library — Membership Form

Difficulty: Hard

Estimated Time: 90–120 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- How CSS decides
  - The cascade: source order and conflicting declarations
  - Browser defaults, and which of them you should keep
  - Specificity: element, class, attribute, pseudo-class and ID selectors
  - Solving a conflict by being specific or by being later — not by
    `!important`

- Inheritance
  - Which properties inherit and which do not
  - Why form controls ignore your page font until you tell them not to
  - `inherit`, `initial` and `unset`

- Selectors that describe, rather than label
  - Attribute selectors: `[type="email"]`, `[required]`, `[disabled]`
  - Child (`>`), adjacent sibling (`+`) and general sibling (`~`) combinators
  - `:hover`, `:focus`, `:first-child`, `:last-child`, `:nth-child()`, `:not()`

- Interactive states
  - A hover state and a keyboard focus state that are both visible
  - `outline` and `outline-offset`, and why removing an outline without
    replacing it is a bug

- Reinforced from the Medium band
  - Colour, borders, radius, box model, spacing scale, centred column

- Accessibility
  - Focus visibility as a requirement, not a decoration
  - Field states that never rely on colour alone
  - Respecting the browser's default behaviour where it is already correct

---

# Challenge

Brackenfield Library has a membership form. It works — it is well-built,
labelled, semantic HTML — and it looks like a tax return.

Your job is to style it, and the interesting constraint is this: you may not add
a single class to the HTML. Every rule you write must find its target through
the structure and attributes that are already there. That is what selectors are
for, and a form is where it pays off: `required`, `disabled` and `type` are
already in the markup, describing exactly the things you want to style.

You still have no layout tools. Fields are stacked, full width, in normal flow.
What you are building is a *system of states*: resting, hovered, focused,
required and unavailable.

---

# Design Reference

![Wireframe: a navy header band, an intro with a required-field note, three bordered fieldset panels containing stacked fields with labels above and hints below, plus separate examples of a focused field, a required field, and a disabled field, then two action buttons and a footer band.](./assets/design/design-reference.svg)

**Palette**

| Role | Colour |
| ---- | ------ |
| Navy (bands, headings) | `#1d3557` |
| Paper (page background) | `#f8f9fb` |
| Blue (accent, focus, primary button) | `#2a6fb0` |
| Line (borders) | `#c9d3e0` |
| Muted (hints, secondary text) | `#5a6472` |

**States** — every field must be distinguishable in all five of these:

| State | What changes |
| ----- | ------------ |
| Resting | Thin border, white background |
| Hovered | Border darkens |
| Focused | Accent border **and** a clearly visible outline offset from the box |
| Required | The field itself is marked, from the attribute — not from a class |
| Unavailable | Muted background and text, and it must read as unavailable to somebody who cannot see colour |

---

# Requirements

## The rule you must not break

- **Do not add, remove or change a single attribute in the HTML**, other than
  linking your stylesheet. If you cannot reach an element, you have not found
  the right selector yet.

## Inherited typography

- The page's font must apply to the whole form, including inputs, selects,
  textareas and buttons. Find out why it does not by default, and fix it with
  the keyword designed for the job.
- The textarea must use the same font as the rest of the form, not a monospace
  one.

## Fieldsets

- Each fieldset is a panel: white, thin border, rounded corners, generous
  padding, and clear space between panels.
- The browser gives `fieldset` its own default padding, border and margin.
  Reset what you do not want using a keyword rather than a magic zero, and leave
  a comment saying which keyword you chose and why.
- The legend reads as a panel heading, and inherits its colour from the panel
  rather than being told a colour of its own.

## Fields

- Labels sit above their controls, in a stronger weight than the hint below.
- The hint that follows a control is quieter and smaller than the label. Select
  it by its position relative to the control, not by a class.
- Text-like inputs (text, email, telephone, date) share one appearance. Reach
  them by their type, and be able to explain why one grouped selector is better
  here than one rule per field.
- The checkbox and radio inputs must **not** pick up the text-input appearance.
  Exclude them with a selector rather than by overriding afterwards.

## Rows

- The radio and checkbox rows sit in a list. Every other row carries a faint
  tint, chosen by position.
- The first row and the last row of each list lose the border they would
  otherwise share with the panel edge.
- Hovering a row lifts its tint. A keyboard user gets an equally strong signal
  from the control's own focus style, which must be at least as visible as the
  hover tint.

## Required and unavailable fields

- Every required field is marked visually, driven by the `required` attribute.
  Note that CSS cannot style a label from the input that follows it, so the
  marker belongs on the field.
- The marker must be understandable without colour — a difference in shape or
  weight, not only a hue — and the page already says in words what it means.
- The one unavailable field is muted and clearly not editable, again driven by
  its attribute.

## Buttons

- A primary button (filled, accent) and a secondary button (outlined).
- Both change on hover and on keyboard focus, and the two changes may be
  different but must both be obvious.
- Neither may lose its focus indicator.

## Specificity discipline

- Somewhere in this stylesheet you will have two rules that both want to style
  the same element. Resolve it with selector specificity or with source order,
  and write a comment explaining which you used.
- `!important` must not appear anywhere in your stylesheet.

---

# Content Requirements

Use the reference page's form: a real library membership application with
personal details, address, membership type, contact preferences and a
declaration. No Lorem ipsum.

---

# Constraints

- **HTML + pure CSS only.** No JavaScript, framework, or preprocessor.
- One external stylesheet, linked with a relative path.
- No `<style>` element and no `style` attribute.
- **No new classes or IDs in the HTML.** Style what is already there.
- No layout system yet: no `display`, `float`, `position`, Flexbox or Grid.
- No media queries, pseudo-elements, custom properties, transitions or
  animations yet.
- No `box-shadow` and no gradients.
- No `!important`.

---

# Accessibility Requirements

- Every interactive element has a focus style that is visible against its
  background. If you replace the browser's outline, replace it with something at
  least as visible.
- Focus and hover are separate states. A page that only responds to hover is
  unusable from a keyboard.
- Required and unavailable states must be conveyed by more than colour.
- Do not lower the contrast of hint text below 4.5:1 just because it is
  secondary.
- Do not disable browser zoom or fix any field's height.
- Check the whole form using only the keyboard: every field must be reachable
  and its state obvious at every step.

---

# Bonus Challenges

1. Style the form's error state using only attributes the HTML already has.
2. Make the fieldset legends numbered, without touching the HTML and without
   pseudo-elements — think about what the browser already numbers for you.
3. Add a print-friendly rule set that removes the panel backgrounds. (Media
   queries are for the Advanced band; a `print` stylesheet linked with a `media`
   attribute is a different technique — try that instead.)
4. Write down, for three of your rules, their specificity as three numbers, and
   check whether any later rule needed to beat them.

---

# Testing Checklist

- [ ] The HTML is byte-for-byte the original except for the stylesheet link.
- [ ] Tab through the entire form: every stop has an obvious focus style.
- [ ] Every other row is tinted, and it is still correct after a row is deleted.
- [ ] Checkbox and radio controls do not look like text inputs.
- [ ] The unavailable field is understandable in greyscale.
- [ ] The textarea and the inputs use the page font.
- [ ] No `!important` in the stylesheet.

---

# Expected Result

Open the provided reference page to see the intended result.

Read the reference stylesheet only after your own version works.

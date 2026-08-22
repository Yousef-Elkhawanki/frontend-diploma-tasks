# Product Details Page

Difficulty: Medium

Estimated Time: 75–90 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Semantic page structure
  - `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`
  - Breadcrumb navigation

- Your first form
  - `<form>`
  - `<label>` connected to its control with `for` and `id`
  - `<input type="number">` with `min`, `max`, `step` and `value`
  - `<input type="radio">` with a shared `name`, and `checked`
  - `<input type="checkbox">`
  - `<select>` with `<option>`, and `selected`
  - `<fieldset>` and `<legend>` to group choices
  - `<button type="submit">`
  - The `required` and `disabled` attributes

- Tables
  - A specification table
  - `<caption>`, `<thead>`, `<tbody>`
  - `<th scope="row">` for row headers

- Progressive disclosure
  - `<details>` and `<summary>`

- Images
  - A small gallery of `<figure>` elements
  - `alt` text that describes each view of the product

- Measurements and ratings
  - `<meter>` with `min`, `max` and `value`
  - `<time>` for review dates

- Text detail
  - `<small>` for legal small print
  - `<abbr>`, `<strong>`, `<em>`
  - `<del>` and `<ins>` for a reduced price

- Lists
  - `<ul>` for features, `<dl>` for what is in the box

- Accessibility
  - Every control has a label
  - Radio groups are grouped and named
  - A button that submits, and a link that navigates — knowing which is which

---

# Challenge

An online audio shop, Northlight Audio, sells one flagship product: the Aurora
One headphones. Their current product page is a single image with a phone number
under it.

Your job is to build the product page they should have had: everything a buyer
needs in order to decide, plus the form that starts the purchase.

Build the page using HTML only.

There is no server and no JavaScript, so the form will not really submit
anything. Build it as though it would.

A visitor should be able to:

- See the product from more than one angle
- Read what it is and why they would want it
- Compare the full technical specifications
- Read what other buyers thought
- Choose a colour, a size of ear pad, a warranty option and a quantity
- Answer their own questions without contacting support

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Page Header

Include:

- The shop name
- Shop navigation (Headphones, Speakers, Cables, Support)
- A breadcrumb trail: shop home, then Headphones, then this product

## Product Overview

Include:

- The product name
- A one-line description
- The current price, and the price it was reduced from, marked up so it is clear
  which one is no longer valid
- The average customer rating, shown as a measurement within a range, plus the
  number of ratings it is based on
- Stock status
- Three product photographs, each with a caption, showing different views
- A short list of the four features that matter most

## Buying Options

Build a form that lets a buyer choose:

- Colour: graphite, sand or deep blue (exactly one)
- Ear pad size: small, medium or large (exactly one, medium pre-selected)
- Extended warranty: two years or three years (optional, chosen from a list)
- Engraving text: optional, at most 16 characters
- Quantity: a whole number from 1 to 5, starting at 1
- Gift wrapping: yes or no
- A submit control that adds the configured product to the basket

Two of the colours are in stock and one is not. Make the unavailable one
visibly unavailable and impossible to choose.

Every choice must be labelled, and the choices that belong together must be
grouped together.

## Specifications

A table of technical specifications with at least eight rows, covering driver
size, frequency response, impedance, battery life, charging time, weight,
connectivity and included cable.

Each row's label is a heading for that row.

## In the Box

List what ships with the product, as term-and-description pairs.

## Questions Buyers Ask

At least four questions, each one collapsed by default so the reader can open
only the ones they care about.

## Reviews

At least three reviews. Each review is self-contained and must have:

- A title
- The reviewer's name
- The date, machine-readable
- The rating given
- The review text
- Whether the reviewer bought the product

## Delivery and Returns

Include:

- Delivery options and prices
- The returns window
- The legal small print about the reduced price

## Footer

Include:

- A copyright line
- A link back to the HTML challenge index, which is two levels up from the
  challenge folder

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Shop: Northlight Audio
- Product: Aurora One over-ear headphones, £249 reduced from £299
- Rating: 4.4 out of 5, from 318 ratings
- Photographs: `headphones-aurora-front.svg`, `headphones-aurora-folded.svg`,
  `headphones-aurora-case.svg` in `./assets/images/`

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The form has no server, so give it no `action`, or point it at itself. Do not
  invent a fake `onsubmit`.
- The specification table is tabular data. Do not use tables anywhere else.
- Do not use the `border` attribute on the table.
- Do not use `<br>` or `<hr>` for spacing.
- Use relative paths so the page works on GitHub Pages.

---

# Accessibility Requirements

- Exactly one `<h1>`: the product name.
- Every form control has a `<label>`. A placeholder is not a label.
- Radio buttons that belong to one question share one `name` and sit inside a
  group with a legend that asks the question.
- The unavailable colour must be announced as unavailable, not just greyed out —
  and remember that you cannot use CSS to grey anything out here anyway.
- The specification table has a caption and row headers with `scope`.
- "Add to basket" performs an action, so it is a button. "Read our returns
  policy" goes somewhere, so it is a link. Do not mix them up.
- Every photograph's `alt` text says which view it shows.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a comparison table against two other models in the range.
2. Add a "notify me when back in stock" form with an email field.
3. Add a related-products area beside the main content.
4. Add a review submission form with a rating, a title and a body.
5. Add `<meta>` tags describing the product for social media previews.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

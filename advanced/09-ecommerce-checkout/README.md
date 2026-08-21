# E-Commerce Product & Checkout

Difficulty: Advanced

Estimated Time: 120–150 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Full document architecture
  - Deciding the document's outline before writing any markup
  - `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`
  - Three separate navigation areas on one page, each distinguishable
  - A checkout that is one long form without becoming one long list

- Metadata and SEO
  - `<title>` written for a search result, not for you
  - `<meta name="description">`
  - `<link rel="canonical">`
  - Open Graph metadata for link previews
  - `<html lang>` and per-phrase `lang`

- Machine-readable values
  - `<data value>` for a price, a stock count and a rating
  - `<time datetime>` for review dates and delivery estimates

- A checkout form
  - Nested `<fieldset>` — a group of controls inside a larger group
  - `<input type="month">` for a card expiry date
  - `inputmode` alongside `type`, and why they are not the same attribute
  - `pattern` with a human explanation of the same rule
  - `autocomplete` tokens for shipping and billing addresses, and for payment
    fields
  - `<select>` with `<optgroup>`, `<textarea>`, radio groups, checkbox groups
  - `required`, `minlength`, `maxlength`, `min`, `max`, `step`, `readonly`
  - `<button type="submit">` against a link — knowing which is which

- Tables
  - An order summary with subtotal, delivery, tax and total in `<tfoot>`
  - A specification table
  - `colspan`, `<th scope>`, `<caption>`

- Embedded content
  - `<iframe>` embedding a size guide document, with a `title`
  - `<details>` and `<summary>` for policies and questions

- Accessibility beyond the basics
  - A skip link
  - Hint text associated with its field using `aria-describedby`, and knowing
    why HTML alone cannot do this
  - Announcing out-of-stock options without relying on colour
  - Review content that reads sensibly out of order

---

# Challenge

Northlight Furniture sells the Lumen desk chair. Today their product page ends
with a telephone number, and the "checkout" is an email address. They want the
whole journey on one page: the product, the decision, and the order.

This is an advanced challenge. The requirements below describe what a customer
must be able to do — they do not tell you which elements to use, and in several
places there is more than one defensible answer. Be ready to justify yours.

Build the page using HTML only. There is no server, so nothing will really be
ordered.

A customer should be able to:

- Find the chair from the shop's navigation and know where they are
- See the chair, its price, its stock position and its rating
- Choose a frame size, a fabric and the optional extras
- Check the size guide without leaving the page
- Read the specifications and the reviews
- Work through a checkout: contact details, delivery address, delivery speed,
  billing address, payment, and confirmation
- Understand the total before committing to it
- Find the returns policy, the warranty and how to get help

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Document Head

Include:

- A title that would make sense as a search result
- A description
- The canonical address of this page
- Metadata that produces a useful preview when the page is shared

## Skip Link and Page Header

Include:

- A skip link
- The shop name
- Shop navigation (Chairs, Desks, Lighting, Storage, Help)
- A breadcrumb trail: shop, then Chairs, then Desk chairs, then this product
- A link to the basket showing how many items are in it

## Product

Include:

- The product name and a one-line description
- Three photographs with captions, each showing something different
- The price, in a form a machine can read as well as a human
- The stock position, machine-readable
- The average rating out of five and the number of ratings
- The four or five things that make this chair different
- Delivery estimate, as a date range

## Configure Your Chair

The customer must be able to choose:

- Frame size: A, B or C — with C temporarily unavailable
- Fabric: five options, one of which costs more
- Castors or glides
- Assembly service, optional
- Quantity, from 1 to 4

The size guide is a separate document that must be readable on this page:
`../../assets/embeds/lumen-chair-size-guide.html`

## Specifications

A specification table with at least ten rows.

## Reviews

At least three reviews, each self-contained, with a rating, a date, the
reviewer, whether the purchase was verified, and — for at least one review — the
shop's reply.

Include a summary of the rating distribution. Decide whether that is a table or
a list, and be able to say why.

## Checkout

One form, worked through in stages:

1. **Contact** — email address, telephone number, and whether they want order
   updates by text message
2. **Delivery address** — recipient name, street address in two lines, town,
   postcode, county, country
3. **Delivery** — standard, named-day or collection from the Leeds workshop; a
   date field for named-day delivery; delivery notes in free text
4. **Billing** — a choice between "same as delivery" and a different address,
   where the different address is a group of controls inside the billing group
5. **Payment** — cardholder name, card number, expiry as a month and year,
   security code
6. **Confirmation** — a discount code, an order reference that the customer
   cannot edit, agreement to the terms, and an optional marketing consent

The postcode and the card number both have a format. Enforce each format in the
markup, and explain each one to the customer in words.

Every field the browser can fill in for the customer should be marked so that it
can.

## Order Summary

A table showing the chair, the fabric supplement, the assembly service,
delivery, tax and the total. The total must be part of the table.

## Help, Returns and Warranty

At least five things a customer asks before ordering, each openable on its own,
including returns, warranty, spare parts, assembly and what happens to the old
chair.

## Related Products

At least three, each with a name, a price and a link. This content is related to
the page but is not part of the product or the order.

## Footer

Include:

- Company details and registration number
- Footer navigation
- Payment and delivery information
- A link back to the challenge index at the root of the repository

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Shop: Northlight Furniture, Leeds
- Product: Lumen desk chair, £389, 4.6 from 212 ratings
- Photographs: `chair-lumen-front.svg`, `chair-lumen-side.svg`,
  `chair-lumen-armrest.svg` in `../../assets/images/`

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The specification table and the order summary are tabular data. Layout must
  never be done with a table.
- ARIA is allowed only where HTML cannot express the relationship — associating
  hint text with a field is the one case on this page. Do not add roles that
  duplicate what the element already means.
- Do not use `<br>` or `<hr>` for spacing.
- Use relative paths for local files so the page works on GitHub Pages.

---

# Accessibility Requirements

- A skip link, first in the tab order.
- Exactly one `<h1>`.
- Every one of your navigation areas is distinguishable from the others.
- Every control has a label. Every group has a legend. The nested billing
  address group has its own legend inside its parent group.
- The unavailable frame size is announced as unavailable in text, and cannot be
  selected.
- Hint text under a field is programmatically associated with that field.
- "Place order" is a button. "Read the returns policy" is a link.
- The order summary table's total is reachable from its row header.
- Review dates are machine-readable.
- Photograph `alt` text distinguishes the three views without repeating the
  caption.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a comparison table against two other chairs in the range.
2. Add a "notify me" form for the unavailable frame size.
3. Add a gift message field and think about where it belongs in the checkout.
4. Add structured questions and answers from customers, with dates.
5. Add a second currency to the price and mark up both machine-readably.
6. Add a delivery slot table for the next seven days.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

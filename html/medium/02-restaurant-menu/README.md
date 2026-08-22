# Restaurant Menu & Reservation Information

Difficulty: Medium

Estimated Time: 60–75 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Semantic page structure
  - `<header>`
  - `<nav>`
  - `<main>`
  - `<section>` nested inside `<section>`
  - `<footer>`

- Grouping related content
  - Menu categories as sections inside one menu area
  - Deciding when a heading level should go down instead of across

- Text content
  - Heading hierarchy (`<h1>` → `<h2>` → `<h3>`)
  - `<strong>` and `<em>`
  - `<small>` for genuinely small print
  - `<abbr>` with `title`

- Lists
  - `<ul>` for unordered items
  - `<dl>` for name and description pairs (dish and its description)

- Tables
  - A first data table
  - `<caption>`
  - `<thead>` and `<tbody>`
  - `<th>` with `scope`

- Quotations
  - `<blockquote>`
  - `<cite>`

- Dates and times
  - `<time>` with `datetime`

- Contact information
  - `<address>`

- Images
  - `<figure>` and `<figcaption>`
  - Descriptive `alt` text

- Links
  - Internal links using `id`
  - External link opening in a new tab
  - `mailto:` and `tel:` links

- Accessibility
  - Table header cells with a scope
  - Abbreviations expanded for the reader
  - Meaningful alt text

---

# Challenge

A family-run Levantine restaurant, The Olive Branch, has one page on the
internet: a photograph of a paper menu, posted on social media in 2021. Prices
have changed twice since then and the page is unreadable on a phone.

They have asked you for a real menu page. There is no online booking system and
they do not want one — they want the phone to ring.

Build the page using HTML only.

A visitor should be able to:

- See what kind of restaurant this is
- Read the full menu, grouped by course, with prices
- Understand the allergen and dietary markings
- Find the opening hours for every day of the week
- Read what other guests have said
- Find the restaurant, call it, or email it

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Page Header

Include:

- The restaurant name
- One line describing the food and the place
- Navigation links to each area of the page

## Introduction

Include:

- A photograph of the dining room, with a caption
- Two paragraphs about the restaurant
- The year it opened, marked up so a machine can read the date as well as a human

## The Menu

The menu has four courses:

- Mezze
- Grills
- Vegetarian
- Desserts

Each course must contain at least three dishes, and every dish must show:

- The dish name
- A short description of what is in it
- The price

Each dish name and its description belong together — choose markup that says so.

Somewhere in the menu area, explain the dietary markings used on the dishes.
At least two of the markings should be short forms whose full meaning is
available to the reader without asking a waiter.

Prices are in Jordanian dinars and include service. Put that where a reader
expects small print to be, and mark it up as small print.

## Opening Hours

Show the opening hours for all seven days in a table.

The table must have:

- A caption
- A separate header row
- Header cells for each day
- Kitchen closing time as well as door closing time

Tuesday is a closing day.

## What Guests Say

Include at least two guest quotations. Each one must credit its source.

## Reservations and Finding Us

Include:

- The reservation policy, in prose (they take bookings by phone only)
- The full address as a block of contact information
- A clickable phone number
- A clickable email address
- A link to the restaurant's location on a map service, opening in a new tab

## Footer

Include:

- A copyright line
- A link back to the HTML challenge index, which is two levels up from the
  challenge folder

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Restaurant: The Olive Branch, opened 2004
- Address: 14 Rainbow Street, Jabal Amman, Amman 11181, Jordan
- Phone: +962 6 461 2200
- Email: table@olivebranch.example
- Dishes: muhammara, moutabal, fattoush, mixed grill, lamb kofta, shish taouk,
  makloubeh, mujadara, stuffed vine leaves, pistachio baklava, knafeh, ashta
  with honey
- Images: `dining-room-olive-branch.svg`, `dish-mezze-platter.svg`,
  `dish-lamb-kofta.svg`, `dish-baklava.svg` in `./assets/images/`

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The opening hours table is real tabular data, so a table is correct. Do not
  use a table for anything else on this page.
- Do not use the `border` attribute on the table.
- No deprecated elements such as `<center>` or `<font>`.
- Do not use `<br>` or `<hr>` for spacing. (A line break inside an address block
  is a different thing, and is allowed.)
- Use relative paths so the page works on GitHub Pages.

---

# Accessibility Requirements

- Exactly one `<h1>`.
- The menu courses are below the menu heading in importance, and the dishes are
  below the courses. Your heading levels should show that.
- Every header cell in the table has `scope`.
- The table has a caption that says what the table contains.
- Abbreviated dietary markings expand to their full meaning in the markup.
- Photographs of food describe the dish, not the photograph.
- The map link says where it goes and warns that it opens in a new tab.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a children's menu as a fifth course, and decide whether it belongs inside
   the menu area or beside it.
2. Add a set menu for groups, priced per person, with the courses it includes.
3. Add a second table listing the wine list by region, vintage and price.
4. Add a private dining area section with capacity information.
5. Add public holiday opening hours and mark up each date with `<time>`.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

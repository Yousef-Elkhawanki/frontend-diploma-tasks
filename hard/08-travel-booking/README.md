# Travel Booking Information Page

Difficulty: Hard

Estimated Time: 90–120 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- A search-and-book form
  - `<input type="date">` with `min` and `max` for arrival and departure
  - `<input type="number">` for guests and rooms
  - `<datalist>` offering suggestions to a text input, without replacing it
  - `<select>` and `<optgroup>` for room types and boards
  - Grouped radio buttons and checkboxes for extras
  - `<textarea>` for special requests
  - `required`, `min`, `max`, `step`, `maxlength`, `autocomplete`, `list`
  - `<button type="submit">`

- A priced data table
  - Rows for each cost line, a `<tfoot>` that totals them
  - `colspan` for a note that spans the table
  - `<caption>`, `<thead>`, `<tbody>`, `<th scope>`

- Embedded content from another site
  - `<iframe>` with a `title` and `loading="lazy"`
  - Why an embedded map always needs a text alternative next to it

- Language marked up correctly
  - `lang` on individual phrases in another language
  - `<abbr>` for units and codes

- Semantic structure
  - `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`
  - `<figure>` and `<figcaption>` for a small gallery
  - `<details>` and `<summary>` for policies people rarely read
  - `<dl>` for the facts of a package
  - `<time>` for dates and for durations
  - `<address>` for the hotel and for the agency

- Links
  - Internal, external in a new tab, email, telephone
  - A download link for the itinerary

- Accessibility
  - A skip link
  - Every control labelled, every group given a legend
  - A date range whose limits are explained in text as well as in attributes
  - An embedded map that is not the only way to find the address

---

# Challenge

Tejo Travel sells one thing well: a four-night city package in Lisbon. Their
booking page is currently a PDF brochure and a telephone number, and they lose
most enquiries between the two.

You have been asked to build the package page: what the trip is, what is
included, what it costs, and the form that starts a booking.

Build the page using HTML only. There is no server, so the form cannot really
submit — build it as though a server were waiting for it.

A visitor should be able to:

- Understand what the package includes and what it does not
- See the hotel, the location and the neighbourhood
- Read the day-by-day itinerary, and take it with them
- See exactly how the price is made up, including taxes and extras
- Check availability and start a booking for their own dates and party
- Read the cancellation and baggage policies without being buried in them
- Find and contact the agency, and find the hotel on a map

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Skip Link and Page Header

Include:

- A skip link
- The agency name
- Site navigation (Destinations, City breaks, Offers, Help)
- Navigation to the areas of this page

## The Package

Include:

- The package name and destination
- A one-sentence summary
- Duration and the season it is available
- Three photographs with captions: the city, the hotel room and local transport
- Two or three paragraphs about the trip
- The facts of the package as term-and-description pairs: nights, board, flights,
  transfers, guide, group size, minimum age

At least two Portuguese words or phrases must appear in the text, marked up so
that a screen reader pronounces them in Portuguese rather than English.

## What Is Included and What Is Not

Two clearly separated lists. A reader must be able to see instantly which is
which.

## Day by Day

The itinerary for all four days, in order. Each day needs a heading, the plan,
and the walking distance involved.

Also provide the itinerary as a file the visitor can download:
`../../assets/downloads/lisbon-3-day-itinerary.txt`

## Price Breakdown

A table that shows how the advertised price is reached: the base price per
person, the single-room supplement, the city tax, the optional extras and the
total. The total belongs in the table.

Prices are per person in euros and the currency should be stated once, not on
every row.

## Check Availability and Book

Build the booking form. It must collect, in sensible groups:

- Departure airport, as a text field that offers suggestions but also accepts
  anything typed
- Arrival date and departure date, both restricted to the season the package runs
- Number of adults, from 1 to 6
- Number of children, from 0 to 4
- Number of rooms, from 1 to 3
- Room type
- Board
- Optional extras: airport transfer, fado evening, Sintra day trip, travel
  insurance
- Special requests, in free text
- Lead traveller's name, email and telephone
- Agreement to the booking conditions — required
- A control to submit the enquiry

## Where You Will Stay

Include:

- The hotel name, its address as a block of contact information, and its
  telephone number
- An embedded map of the hotel's location
- Directions from the airport and from the nearest metro station, in text — the
  map must not be the only way to get this information

## Policies

At least four policies, each one openable on its own: cancellation, baggage,
children, and what happens if a flight is delayed.

## The Agency

Include:

- The agency's address, telephone number and email
- Its licence number
- Opening hours for the telephone line

## Footer

Include:

- Which season this page prices
- Links to booking conditions and the privacy notice
- A link back to the challenge index at the root of the repository

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Agency: Tejo Travel, Lisbon
- Package: Alfama & Belém, four nights
- Hotel: Hotel Tejo, Rua dos Remédios 118, Alfama
- Season: 1 March to 31 October 2027
- Photographs: `lisbon-alfama-view.svg`, `hotel-room-tejo.svg`,
  `tram-28-lisbon.svg` in `../../assets/images/`

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The price breakdown is real tabular data. Nothing else on this page may be a
  table.
- The embedded map must not be the only source of the address.
- Do not use `<br>` or `<hr>` for spacing.
- Use relative paths for local files. The map is the only external embed.

---

# Accessibility Requirements

- A skip link, first in the tab order.
- Exactly one `<h1>`.
- Every form control has its own label; every group of controls has a legend.
- The date fields state their allowed range in text, not only in `min` and `max`.
- The `<datalist>` is a set of suggestions, not a substitute for a label, and the
  field still accepts an airport that is not in the list.
- The iframe has a `title` describing what it shows.
- Foreign-language phrases carry a `lang` attribute.
- Photograph `alt` text describes the place, not the composition.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a departure-date and price calendar table for the whole season.
2. Add a comparison table of the three hotels the agency uses in Lisbon.
3. Add a guest reviews area with attributed quotations and dates.
4. Add a second package as a sibling article and rethink the heading hierarchy.
5. Add a newsletter form with an email field and a topic selection.
6. Add flight-time information as a table with departure and arrival times.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

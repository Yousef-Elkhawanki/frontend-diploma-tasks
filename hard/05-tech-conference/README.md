# Technology Conference & Registration

Difficulty: Hard

Estimated Time: 90–120 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Full page architecture
  - `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`
  - More than one navigation area, each distinguishable from the others
  - Sections nested inside sections

- A complex data table
  - `<caption>`, `<thead>`, `<tbody>`, `<tfoot>`
  - `colspan` for a session that fills every track
  - `rowspan` for a session that lasts two slots
  - `<th scope="col">` and `<th scope="row">`
  - Two tables on one page, each with a different shape

- An advanced form
  - `<fieldset>` and `<legend>` for every group of related controls
  - `<input>` types: `text`, `email`, `tel`, `url`, `date`, `number`, `radio`,
    `checkbox`
  - `<select>` with `<optgroup>` and `<option>`
  - `<textarea>` with `rows` and `maxlength`
  - `<button type="submit">` and `<button type="reset">`
  - Attributes: `required`, `pattern`, `placeholder`, `min`, `max`, `minlength`,
    `maxlength`, `autocomplete`, `checked`, `selected`, `multiple`

- Dates, times and places
  - `<time>` for a date, for a time, and for a duration
  - `<address>` for the venue and the organisers

- Progressive disclosure
  - `<details>` and `<summary>` for questions and for session abstracts

- Media and figures
  - `<figure>` and `<figcaption>` for speaker photographs and the venue

- Links
  - Internal links to sections
  - External links opening in a new tab
  - A download link to a calendar file
  - Email and telephone links

- Accessibility
  - A skip link as the first focusable element on the page
  - Labels connected to every control
  - Grouped radio buttons and checkboxes
  - Table headers with a scope, including in a table with merged cells
  - Heading hierarchy across a long, multi-part page

---

# Challenge

The Northern Web Conference runs for two days in Gothenburg every October. Until
now, everything has been organised through a spreadsheet emailed to attendees and
a form built by somebody's cousin, which lost eleven registrations last year.

The organisers have asked you for the conference website: one page that explains
the event, publishes the programme, introduces the speakers, sets out the ticket
prices, and takes registrations.

Build the page using HTML only. There is no server, so the form cannot really
submit — build it as though a server were waiting for it.

A visitor should be able to:

- Understand what the conference is, when it runs and where
- Read the two-day programme and see which sessions clash
- Read about the speakers and their sessions
- Compare ticket types and prices
- Register, including their workshop choice and any access requirements
- Add the programme to their own calendar
- Get their questions answered without emailing anybody

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Skip Link

The first thing a keyboard user reaches must be a link that jumps past the
navigation to the main content.

## Page Header

Include:

- The conference name and year
- A one-sentence description
- The dates, marked up so a machine can read them
- The city and venue
- Navigation to every area of the page

## About the Conference

Include:

- Two or three paragraphs about what the conference is for and who attends
- A photograph of the venue with a caption
- Key facts as term-and-description pairs: format, languages, attendance,
  recording policy, code of conduct

## Programme

Publish the full two-day programme as a schedule.

The schedule runs across three rooms — Main Hall, Workshop Room B and the Studio
— and must show:

- The time of every session
- What is on in each room
- Sessions that take place in all three rooms at once, such as the keynote and
  lunch
- At least one workshop that runs across two consecutive time slots
- A note underneath the schedule about doors, breaks and recordings

Both conference days must be published. Make it obvious which day is which.

Each session should show its speaker where it has one, and a reader should be
able to open an abstract for at least four sessions without leaving the page.

## Speakers

At least four speakers. For each one:

- Photograph
- Name
- Job title and organisation
- The city they travel from
- A short biography
- Their session title, linking to that session in the programme
- A link to their own website or profile, opening in a new tab

## Tickets

A table comparing at least three ticket types, showing for each:

- Price
- Whether workshops are included
- Whether the recordings are included
- Whether lunch is included
- How many are left

Include the price with tax and a total row or note at the foot of the table.

Student and community tickets exist and are cheaper — say who qualifies.

## Registration

Build the registration form. It must collect, in sensible groups:

- Full name
- Email address
- Telephone number in an international format
- Job title
- Organisation
- Website or profile URL (optional)
- Ticket type
- Arrival date, which must fall on or between the two conference days
- Workshop choice, from a list grouped by day
- Number of extra evening-event places, from 0 to 3
- Dietary requirements (any number of them)
- Access requirements, in free text
- How they heard about the conference
- Agreement to the code of conduct, which is required
- Optional consent to be emailed about next year's conference
- A control to submit the registration, and a control to clear the form

## Questions

At least five questions that a reader can open one at a time.

## Practical Information

Include:

- The venue address as a block of contact information
- Travel information from the airport and the central station
- A link that downloads the programme as a calendar file:
  `../../assets/downloads/webdev-conf-2026-schedule.ics`
- The organisers' contact email and telephone number

## Footer

Include:

- The organising company
- Links to the code of conduct, the privacy notice and last year's site
- A link back to the challenge index at the root of the repository

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Conference: Northern Web Conference 2026
- Dates: 8 and 9 October 2026
- Venue: Harbour Centre, Lindholmsallén 12, 417 55 Gothenburg, Sweden
- Speakers: Nadia Rahman, Tomas Lindqvist, Aisha Bello, Daniel Kim
- Photographs: `speaker-*.svg` and `venue-harbour-centre.svg` in
  `../../assets/images/`
- Tickets: Community 1 200 SEK, Standard 3 900 SEK, Standard plus workshops
  5 400 SEK

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The schedule and the ticket comparison are real tabular data. Nothing else on
  this page may be a table.
- Do not use the `border` attribute.
- Do not use `<br>` or `<hr>` for spacing.
- Give the form a `method` and either no `action` or an `action` pointing at the
  page itself.
- Every relative path must work when the site is served from a subdirectory on
  GitHub Pages.

---

# Accessibility Requirements

- The skip link is the first focusable element and points at your main content.
- Exactly one `<h1>`.
- Every navigation area is labelled so that a screen reader user hears the
  difference between "main", "on this page" and "footer".
- Every input, select and textarea has its own `<label>` connected with
  `for`/`id`. Placeholders are hints, never labels.
- Radio groups and checkbox groups sit inside a `<fieldset>` whose `<legend>`
  asks the question.
- In the schedule, a cell that spans rooms or slots still has to be findable
  from its row and column headers.
- Validation is expressed with HTML attributes, not with instructions in
  brackets. If a field must match a pattern, tell the user what the pattern is in
  text as well.
- Speaker photographs describe the person; the venue photograph describes the
  building.
- The calendar download link says what the file is.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a third day of pre-conference workshops and extend the schedule.
2. Add a sponsors area with tiers, and think about whether tiers are a list or a
   table.
3. Add a call for proposals form with a talk title, abstract and duration.
4. Add a hotel comparison table with distance from the venue and nightly price.
5. Add a live-caption and interpretation policy section.
6. Add metadata so that sharing the page produces a useful preview.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

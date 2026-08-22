# Job Vacancy & Application Form

Difficulty: Hard

Estimated Time: 90–120 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Page architecture for a single, self-contained document
  - `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`
  - A job advertisement as one self-contained article

- Form controls you have not used yet
  - `<input type="file">` with `accept` and `multiple`
  - `<input type="url">`
  - `<input type="number">` with `min`, `max` and `step`
  - `<select multiple>`
  - `readonly` and `disabled` — and the difference between them
  - `<textarea>` with `rows`, `maxlength` and `required`
  - `<fieldset>`, `<legend>`, `<button>`

- Validation expressed in HTML
  - `required`, `minlength`, `maxlength`, `pattern`, `min`, `max`, `step`
  - `autocomplete` values that help a browser fill a form correctly

- A table with grouped rows
  - `rowspan` to group several rows under one category
  - `<caption>`, `<thead>`, `<tbody>`, `<th scope>`

- Structured facts
  - `<dl>` for the facts of a job: salary, contract, location, closing date
  - `<ol>` for a hiring process that happens in order
  - `<ul>` for requirements that have no order

- Dates and contact details
  - `<time>` with `datetime` for the closing date and the start date
  - `<address>` for the employer

- Progressive disclosure
  - `<details>` and `<summary>`

- Links
  - A download link to the full job description
  - An email link with a subject line
  - Internal links, and external links opening in a new tab

- Accessibility
  - A skip link
  - Labels, groups and legends for every control
  - Telling a user what a file upload will accept, in text as well as in markup
  - Heading hierarchy inside an article

---

# Challenge

Northwind Studio is hiring a front-end engineer. Their careers page currently
says "email us your CV", which is why they receive four applications a month and
none of them from the people they want.

You have been asked to build the vacancy page: the advertisement, the practical
facts, the honest description of the work, and the application form itself.

Build the page using HTML only. There is no server, so the form cannot really
submit — build it as though a server were waiting for it.

An applicant should be able to:

- Decide in one minute whether this job is worth reading about
- Find the salary, the contract type and the closing date without hunting
- Understand what the work actually involves day to day
- See what is essential and what is merely desirable
- Understand the hiring process before starting it
- Apply, including uploading files and answering the studio's questions
- Ask a question, or request an adjustment, without applying

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Skip Link and Page Header

Include:

- A link that skips the navigation and lands on the main content
- The studio name
- Navigation across the studio site (Work, Studio, Careers, Contact)

## The Vacancy

The advertisement is one self-contained document within the page. It must
include:

### Vacancy header

- The job title
- The reference number, which the applicant will need later
- A one-sentence summary of the role
- The closing date, machine-readable

### The facts

Present these as term-and-description pairs:

- Salary band
- Contract type and hours
- Location and how many days on site
- Reporting line
- Start date
- Closing date

### About the role

Two or three paragraphs. Say honestly what the job involves, including the parts
people usually leave out of adverts.

### What you will do

An unordered list of responsibilities.

### What we are looking for

Two clearly separated groups: what is essential and what is desirable. A reader
must be able to tell instantly which is which.

### Salary and benefits

A table showing the studio's engineer levels. For each level show the salary
band and the review cycle, and group the benefit rows by category so that one
category label covers several rows.

### How we hire

The stages of the process, in order, with how long each stage takes and whether
it is paid.

### Questions applicants ask

At least four, each openable on its own.

## Apply

Build the application form. It must collect, in sensible groups:

- Full name
- Email address
- Telephone number
- The vacancy reference, pre-filled and not editable by the applicant
- Portfolio or profile URL
- Years of professional experience, as a whole number from 0 to 40
- Locations the applicant could work from, where more than one may be chosen
- Earliest start date
- Notice period
- A CV file, accepting PDF or plain text only
- Up to three work samples, in one control
- A written answer to the studio's question, required, with a length limit
- Whether the applicant needs a visa sponsorship — a yes or no question
- Any adjustment they need during the process
- Consent to their data being kept for six months — required
- A control to submit, and a control to clear the form

One field in this form is filled in for the applicant and must not be changed by
them. Pick the right attribute for that, and be able to explain why the other
similar attribute would be wrong.

## Beside the Vacancy

Include:

- A photograph of the studio, with a caption
- The hiring lead's name, photograph and a sentence about them
- A link that downloads the full job description:
  `./assets/downloads/frontend-engineer-job-description.txt`
- An email link, pre-filled with a subject line quoting the reference number, for
  people who want to ask a question before applying
- The studio address

## Footer

Include:

- Equal opportunities statement
- Links to other open roles
- A link back to the HTML challenge index, which is two levels up from the
  challenge folder

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Employer: Northwind Studio, Manchester, United Kingdom
- Role: Front-End Engineer (accessibility focus), reference NWS-2026-FE-07
- Salary: £42,000 – £52,000
- Closing date: 30 September 2026
- Hiring lead: Yasmin Farouk
- Photographs: `office-northwind-studio.svg`, `portrait-hiring-lead.svg` in
  `./assets/images/`

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- A form that uploads files needs the right `method` and the right
  `enctype`. Set them, even though nothing will receive the upload.
- The salary and benefits table is real tabular data. Nothing else on this page
  may be a table.
- Do not use `<br>` or `<hr>` for spacing.
- Use relative paths so the page works on GitHub Pages.

---

# Accessibility Requirements

- A skip link, first in the tab order.
- Exactly one `<h1>`.
- Every control has a `<label>`; every group of controls has a `<legend>`.
- The file inputs tell the applicant what file types and how many files are
  accepted, in visible text as well as in the markup.
- The essential and desirable requirements are separated structurally, not only
  by wording.
- The table's row groupings remain understandable when read cell by cell.
- The email link says who it reaches and what it is for.
- Every date a human reads is also machine-readable.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a second vacancy on the same page and decide what that means for your
   heading hierarchy.
2. Add an equal opportunities monitoring form as a separate, optional group.
3. Add a "life at the studio" section with two employee quotations, attributed.
4. Add a table comparing this role with the senior role above it.
5. Add a benefits calculator table showing the value of the package at each
   level.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

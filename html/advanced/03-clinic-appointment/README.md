# Clinic Appointment Booking

Difficulty: Advanced

Estimated Time: 120–150 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- A high-stakes form
  - `<input type="time">` with `min`, `max` and `step`
  - `<input type="date">` with `min` and `max`, and `autocomplete="bday"`
  - `<input type="text">` with `pattern` for a patient number
  - `<input type="tel">` with `pattern` and `inputmode`
  - Nested `<fieldset>` for a group inside a group
  - Radio groups, checkbox groups, `<select>` with `<optgroup>`
  - `<textarea>` with `maxlength`
  - `required`, `readonly`, `autocomplete`, `aria-describedby` for hint text
  - Two submit paths in one form, and why that is a design decision

- Tables that carry a real timetable
  - Clinician availability by day and session, with `rowspan` grouping
  - `colspan` for a note that spans the table
  - `<caption>`, `<thead>`, `<tbody>`, `<tfoot>`, `<th scope>`

- Content in more than one language
  - `lang` on individual names and phrases
  - Why `lang` matters to a screen reader reading a name aloud

- Definitions and structured facts
  - `<dfn>` for a term being defined
  - `<dl>` for facts, `<ol>` for what to do in order, `<ul>` for what to bring

- Embedded content
  - `<iframe>` with a `title` for the clinic's location
  - Directions in text, because a map is not an accessible address

- Everything you have already learned
  - Skip link, landmarks, multiple navigation areas, `<details>`, `<time>`,
    `<address>`, `<figure>`, metadata, download links

- Accessibility where it matters most
  - An urgent-care warning that is impossible to miss and does not rely on colour
  - Hint text associated with the field it describes
  - A form that can be completed with a keyboard alone
  - Plain language for instructions

---

# Challenge

Riverside Family Clinic has four clinicians, three thousand patients and one
telephone line that is engaged every morning between eight and nine.

They want a page that lets a patient book a routine appointment online, find out
when their clinician is available, and — this is the part that matters most —
work out immediately when they should *not* be using this page at all, because
they need urgent care.

This is an advanced challenge. A booking form for healthcare is the sort of form
where a confusing label has consequences. Decide your structure first, keep the
language plain, and make the urgent-care route impossible to miss.

Build the page using HTML only.

A patient should be able to:

- Tell within seconds whether this page is the right place for their problem
- Find the urgent and emergency routes without scrolling past a form
- See which clinician works which sessions
- Book a routine appointment, in person, by video or by telephone
- Say what they need in order to attend: an interpreter, step-free access, a
  longer appointment
- Register as a new patient, or download the form to bring with them
- Find the clinic, contact it, and know when it is open

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Document Head

Include a title, a description, and the page's canonical address.

## Skip Link and Page Header

Include:

- A skip link
- The clinic name
- Site navigation (Appointments, Our clinicians, Prescriptions, Test results,
  Contact)
- Navigation to the areas of this page

## If You Need Urgent Help

This must come before anything else in the main content, and must be
impossible to miss without relying on colour or styling. Include:

- When to call the emergency number, with the number as a clickable link
- When to use the urgent care line instead of booking
- What this page is for, by contrast

## Booking a Routine Appointment

Explain how routine booking works, in plain language: how far ahead
appointments open, how long they last, what happens if the patient is late, and
how to cancel.

Define one term the reader may not know — use the element intended for the
defining instance of a term.

## Our Clinicians

At least three clinicians. For each one:

- Photograph
- Name, with correct language marking where the name is not English
- Role and specialism
- Languages they consult in
- Which patients they see

At least one clinician's name must be in a language other than English and
marked up as such.

## Availability

A table showing which clinician is available in which session, across the
working week.

It must show:

- Morning and afternoon sessions for Monday to Friday
- One clinician who works the whole day, expressed as one cell covering both
  sessions
- Sessions that are reserved rather than bookable, such as home visits and
  telephone triage
- A note at the foot about bank holidays and same-day appointments

## Book an Appointment

Build the booking form. It must collect, in sensible groups:

**About the patient**

- Full name
- Date of birth
- Patient number, which has a fixed format
- Telephone number
- Email address
- Whether the patient is booking for themselves or for somebody else, and — if
  for somebody else — that person's name and relationship, as a group inside the
  group

**The appointment**

- Appointment type: in person, video call or telephone
- Department, chosen from a grouped list
- Preferred clinician, or no preference
- Preferred date, restricted to the booking window
- Preferred time, restricted to opening hours and in fifteen-minute steps
- Whether a longer appointment is needed
- A short description of the reason for the appointment

**Access and support**

- Interpreter needed, and for which language
- Step-free access needed
- A quiet waiting area needed
- Somebody attending with the patient
- Anything else, in free text

**Confirmation**

- How the patient wants to be reminded
- Consent to the clinic contacting them about this appointment — required
- A control that requests the appointment

## New Patients

Include:

- What a new patient needs to bring, as a list
- The registration steps, in order
- A download link for the paper form:
  `./assets/downloads/riverside-clinic-new-patient-form.txt`

## Finding Us and Opening Hours

Include:

- A photograph of the entrance, with a caption that says something useful
  about access
- The clinic's address as a block of contact information, with a clickable
  telephone number and email address
- An embedded map
- Directions by bus, by car and on foot, in text
- Opening hours as a table, including which days the telephone line is
  answered late

## Questions Patients Ask

At least five, each openable on its own.

## Footer

Include:

- The clinic's regulator and registration number
- Footer navigation including a complaints route and an accessibility statement
- A link back to the HTML challenge index, which is two levels up from the
  challenge folder

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Clinic: Riverside Family Clinic, Riverside Walk, Norwich
- Clinicians: Dr Hana Suzuki (花子 鈴木), Dr Marcus Obeng, Dr Elif Demir
- Photographs: `clinic-riverside-entrance.svg`, `doctor-hana-suzuki.svg`,
  `doctor-marcus-obeng.svg`, `doctor-elif-demir.svg` in `./assets/images/`
- Booking window: 5 October to 27 November 2026
- Opening hours: 08:00 to 18:30, Monday to Friday

This is fictional content for a teaching exercise. Do not use the name, address
or registration number of a real clinic, and do not present the page as real
medical guidance.

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The availability table and the opening-hours table are real tabular data.
  Nothing else on this page may be a table.
- The urgent-care warning must work with styling switched off — you cannot make
  it red, so it has to be structurally prominent instead.
- ARIA only where HTML cannot express the relationship, such as connecting hint
  text to its field.
- Do not use `<br>` or `<hr>` for spacing.
- Use relative paths for local files so the page works on GitHub Pages.

---

# Accessibility Requirements

- A skip link, first in the tab order.
- Exactly one `<h1>`.
- The urgent-care information is the first thing in the main content and is
  reachable by the skip link.
- Every control has a label; every group has a legend; the nested group has its
  own legend.
- Hint text is programmatically associated with its field.
- The patient number and telephone formats are explained in words as well as
  enforced by `pattern`.
- Names in another language carry a `lang` attribute so they are pronounced
  correctly.
- The availability table's merged cells remain traceable to their headers.
- The map is not the only source of the address or the directions.
- Instructions use plain language: short sentences, no jargon without a
  definition.

---

# Bonus Challenges

All bonus work must stay HTML-based only.

1. Add a repeat-prescription request form as a separate group.
2. Add a table of clinic services with which clinician provides each.
3. Add a cancellation form that takes a booking reference.
4. Add a translated summary of the urgent-care advice in a second language,
   marked up with the correct `lang`.
5. Add a glossary of clinical terms using definitions and a description list.
6. Add a table of vaccination clinic dates for the season.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

# University Course Page & Weekly Schedule

Difficulty: Hard

Estimated Time: 90–120 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Embedded media
  - `<audio>` with `controls` and more than one `<source>`
  - Fallback content for a browser that cannot play the file
  - A download link for the same recording
  - `<iframe>` with a `title`, `width`, `height` and `loading`

- Two tables with different shapes
  - A weekly timetable, where the same class can fill several rooms or run over
    two slots — `colspan` and `rowspan`
  - An assessment table with a total row in `<tfoot>`
  - `<caption>`, `<thead>`, `<tbody>`, `<th scope="col">`, `<th scope="row">`

- Semantic structure for a document with many parts
  - `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`
  - Sections nested inside sections
  - Deciding when something is an `<aside>` and when it is just a `<section>`

- Progressive disclosure at scale
  - A twelve-week syllabus where each week opens on its own, using `<details>`
    and `<summary>`

- Structured facts and sequences
  - `<dl>` for the facts of a course
  - `<ol>` for required reading in reading order
  - `<ul>` for learning outcomes

- Quotations
  - `<blockquote>` with `cite`, and `<cite>`, for student feedback

- Dates, times and abbreviations
  - `<time>` with `datetime` for dates, times and durations
  - `<abbr>` for `ECTS`, `WCAG` and the course code

- Contact information
  - `<address>` for the lecturer and the department

- Links
  - Internal links, external links in a new tab, email links
  - A link to a document that is also embedded on the page

- Accessibility
  - A skip link
  - Media with a text alternative available on the page
  - An iframe that announces what it contains
  - Timetable cells that remain findable through their headers

---

# Challenge

Willowbrook University publishes each course as a page in the online prospectus.
The current page for COMP-204 is a wall of unstyled text pasted out of a Word
document; students routinely turn up to the wrong room because the timetable is
a screenshot.

You have been asked to rebuild it. The page has to serve three audiences at
once: a prospective student deciding whether to take the course, an enrolled
student checking where they need to be on Tuesday, and a member of staff checking
the assessment weighting.

Build the page using HTML only.

A visitor should be able to:

- Understand what the course covers, who teaches it and what it is worth
- Check the weekly timetable, including which classes are in which room
- Read the week-by-week syllabus without scrolling past all twelve weeks
- See how the course is assessed and what each part is worth
- Listen to a sample lecture recording, or read what is in it
- Open the official syllabus document without leaving the page
- Find the reading list, the prerequisites and how to contact the lecturer

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Skip Link and Page Header

Include:

- A skip link to the main content
- The university and department name
- Prospectus navigation (Courses, Departments, Admissions, Library)
- Navigation to the areas of this page

## Course Overview

Include:

- The course code and title
- The semester and academic year
- Two or three paragraphs describing the course
- A photograph of the teaching space, with a caption
- The facts of the course as term-and-description pairs: credits, level,
  language of instruction, contact hours per week, mode of delivery, and the
  examination period

The credit unit is an abbreviation. Make its full meaning available.

## Learning Outcomes

What a student will be able to do at the end. Order does not matter here.

## Weekly Timetable

Publish the timetable for a normal teaching week.

It must show:

- Each teaching slot's time
- The day of the week
- What kind of session it is, and where
- One session that occupies two consecutive time slots
- One session that runs in more than one room at the same time
- A note underneath about reading weeks and room changes

## Syllabus, Week by Week

All twelve teaching weeks. A reader must be able to open one week at a time.

Each week needs a topic, what is being read or practised, and whether anything
is due.

## Assessment

A table of assessment components showing, for each one, what it is, what it is
worth, and when it is due. The weights must add up, and the total must be
visible as part of the table.

Below the table, explain the pass mark and the resit policy.

## Sample Lecture

Include:

- A recorded excerpt from a lecture, playable on the page in more than one file
  format
- Something useful for a visitor whose browser cannot play it
- A way to download the recording
- A written summary of what the excerpt covers

Recording files:

- `../../assets/audio/comp204-lecture-04-excerpt.m4a`
- `../../assets/audio/comp204-lecture-04-excerpt.wav`

## Official Syllabus Document

Embed the department's syllabus document on the page, and also link to it so a
student can open it in a tab of its own.

Document: `../../assets/embeds/comp204-syllabus.html`

## Reading List

Required reading, in the order students should read it, and recommended reading
where order does not matter. At least two entries link to an external source.

## Prerequisites and Support

This content relates to the course but is not part of the course description
itself. Include:

- Which courses a student must have passed first
- What to do if they have not
- Study support and the accessibility service, with contact details

## What Students Say

At least two quotations from previous students, each credited to a cohort year.

## Contact

Include:

- The lecturer's name, room, office hours and email
- The department's postal address and telephone number

## Footer

Include:

- Which academic year this page describes and when it was last revised
- Links to the course catalogue and the regulations
- A link back to the challenge index at the root of the repository

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Course: COMP-204 Web Document Structure, autumn semester 2026
- Credits: 6 ECTS, level 2 undergraduate
- Lecturer: Prof. Elena Vasquez, room 4.12, Ada Building
- Department: Department of Computing, Willowbrook University
- Photograph: `../../assets/images/campus-computing-lab.svg`
- Portrait: `../../assets/images/portrait-prof-elena-vasquez.svg`
- Assessment: weekly exercises 20%, structure audit 25%, group project 25%,
  written examination 30%

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The timetable and the assessment breakdown are real tabular data. Nothing else
  on this page may be a table.
- The audio element must offer both provided formats and let the browser choose.
- Do not autoplay the audio.
- Do not use `<br>` or `<hr>` for spacing.
- Use relative paths so the page works on GitHub Pages.

---

# Accessibility Requirements

- A skip link, first in the tab order.
- Exactly one `<h1>`.
- The audio player is not the only way to get the information — the page also
  says what is in the recording.
- The `<iframe>` has a `title` that says what document it contains.
- Every timetable cell can be traced to a day and a time through header cells.
- The assessment total is in the table, not only in a sentence after it.
- Abbreviations are expanded on first use.
- Heading levels descend one step at a time, even twelve weeks deep.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add an examination timetable table for the assessment period.
2. Add a second iframe embedding the department's map or floor plan.
3. Add a coursework submission form with a file upload and a declaration.
4. Add a glossary of course terminology as a description list.
5. Add per-week learning outcomes inside each week's disclosure.
6. Add metadata that would help this page appear correctly in a course search.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

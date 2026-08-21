# Personal Portfolio & CV

Difficulty: Medium

Estimated Time: 45–60 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Document setup
  - `<!DOCTYPE html>`
  - `<html lang>`
  - `<meta charset>`
  - `<meta name="viewport">`
  - `<title>`
  - `<meta name="description">`

- Semantic page structure
  - `<header>`
  - `<nav>`
  - `<main>`
  - `<section>`
  - `<footer>`

- Text content
  - Heading hierarchy (`<h1>` → `<h2>` → `<h3>`)
  - Paragraphs
  - `<strong>`
  - `<em>`

- Navigation and links
  - Internal links to sections using `id`
  - External links
  - `target="_blank"` and `rel="noopener"`
  - Email links (`mailto:`)
  - Telephone links (`tel:`)
  - Download links (`download`)

- Images
  - `<img>` with `alt`, `width` and `height`
  - `<figure>`
  - `<figcaption>`

- Lists
  - `<ul>`
  - `<ol>`
  - `<dl>` with `<dt>` and `<dd>`

- Contact information
  - `<address>`

- Accessibility
  - Meaningful alt text
  - Correct heading hierarchy
  - Descriptive link text

---

# Challenge

You have been asked to build the personal website of a front-end developer who
is looking for her next role.

Right now she sends a PDF CV as an email attachment, and recruiters keep asking
her for "a link". Your job is to build that link: one HTML page that a recruiter
can skim in two minutes and that works on a phone, on a laptop, and with a
screen reader.

Build the page using HTML only.

A visitor to the page should be able to:

- Understand who she is and what she does within the first screen
- Jump straight to the part of the page they care about
- See her recent work experience
- Look at three projects she has built, and visit them
- Understand what she is good at
- Contact her by email or phone, or download her CV

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Page Header

Include:

- Her name
- One short line describing what she does
- Her city
- Navigation links that jump to each area of the page

## About

Include:

- A photograph with a caption
- Two or three paragraphs of introduction
- At least one phrase given genuine emphasis, and at least one phrase marked as
  important — think about which is which

## Experience

Show at least two roles.

Each role should have:

- Job title
- Company and city
- Period worked
- Two or three achievements

The reader should be able to scan the roles in order, most recent first.

## Projects

Show exactly three projects.

Each project should have:

- A screenshot with a caption
- Project name
- What problem it solves
- The technologies used
- A link to the live project

The live project links point to other websites, so they should open in a new tab
and be safe to do so.

## Skills

Group her skills so that a reader can see the *category* and the *skills inside
that category* — for example languages, testing, and tooling. The relationship
between a category and its skills should be visible in the markup, not only in
the text.

Also list the human languages she speaks.

## Contact

Include:

- Her contact details as a proper block of contact information
- A clickable email address
- A clickable phone number
- A link that downloads her CV file: `../../assets/downloads/sara-haddad-cv.txt`

## Footer

Include:

- A copyright line
- A link back to the challenge index at the root of the repository

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

You may use the content below, or invent your own of the same quality.

- Name: Sara Haddad
- Role: Front-End Developer
- City: Amman, Jordan
- Email: sara.haddad@example.com
- Phone: +962 7 9012 3456
- Roles: Cedar Digital (2023–present), Bayt Labs (2021–2023)
- Projects: TaskFlow, Lexicon, CityRoutes
- Photograph: `../../assets/images/portrait-sara-haddad.svg`
- Project screenshots: `project-taskflow.svg`, `project-lexicon.svg`,
  `project-cityroutes.svg` in `../../assets/images/`

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- No deprecated elements such as `<center>` or `<font>`.
- Do not use `<br>` or `<hr>` to create spacing.
- Do not use tables for layout.
- Use relative paths for images and downloads so the page works on GitHub Pages.
- Indent your markup consistently, and let the browser's default styling show
  the structure you built.

---

# Accessibility Requirements

- Exactly one `<h1>`, describing the page.
- Do not skip heading levels.
- Every image has an `alt` attribute. The portrait and the screenshots carry
  information, so describe what they show — never write `alt="image"`.
- Link text makes sense read on its own. "Visit the TaskFlow project" is a link;
  "click here" is not.
- The `lang` attribute on `<html>` is set correctly.
- The page must be usable with the keyboard alone. Everything clickable on this
  page is already a link, so this comes for free if you use links.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a short list of talks or articles she has published, each linking to the
   original source.
2. Add a "currently learning" area and think about whether it belongs in About
   or in Skills.
3. Add `<meta name="author">` and a favicon link.
4. Add a testimonial from a former colleague, marked up as a quotation with its
   source attributed.
5. Reduce your markup: find every `<div>` in your solution and either replace it
   with a semantic element or delete it.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

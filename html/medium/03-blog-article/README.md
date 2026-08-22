# Blog Article Page

Difficulty: Medium

Estimated Time: 60–75 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Semantic page structure
  - `<header>` for the site and `<header>` inside an `<article>`
  - `<nav>` used more than once on a page
  - `<main>`
  - `<article>` as a self-contained piece of content
  - `<section>` for the parts of a long text
  - `<aside>` for content related to, but separate from, the article
  - `<footer>` for the site and `<footer>` inside an `<article>`

- Publishing metadata
  - `<time>` with `datetime`
  - Author information
  - Reading time
  - `<meta name="description">`

- Long-form text
  - Heading hierarchy across a long document
  - A table of contents built from internal links
  - `<strong>`, `<em>`, `<abbr>`

- Quotations
  - `<blockquote>` with `cite` attribute
  - `<cite>` for the name of a work
  - `<q>` for a short inline quotation

- Technical writing
  - `<code>` for inline code
  - `<pre>` wrapping `<code>` for a code block
  - `<kbd>` for keys the reader should press

- Figures
  - `<figure>` and `<figcaption>` for a diagram
  - Deciding what the `alt` text of a diagram should say

- Lists
  - Ordered, unordered and nested lists

- Links
  - Breadcrumb navigation
  - Internal links to headings using `id`
  - External links that open in a new tab
  - Links between related articles

- Accessibility
  - One `h1` per document
  - No skipped heading levels
  - A diagram whose meaning is available as text

---

# Challenge

You write for a small development blog called *The Markup Notebook*. Your editor
has handed you a finished draft and asked you to publish it.

Publishing means more than pasting the words in. The page has to tell a reader —
and a search engine, and a screen reader — what this document is, who wrote it,
when, what it is about, and what to read next.

Build the page using HTML only.

A reader should be able to:

- See immediately what the article is about and when it was written
- Jump to any part of a long article
- Follow the argument, including a diagram, a quotation and a code example
- Learn who wrote it
- Find related articles without leaving the page

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Site Header

Include:

- The name of the blog
- The blog's main navigation (Home, Articles, Topics, About)

## Breadcrumb Trail

Show where this page sits: the blog home, then the topic, then this article.
This is a second, separate navigation area on the page — think about how a
screen reader user will tell your two navigation areas apart.

## The Article

The article is a self-contained document. It must contain:

### Article header

- The article title
- A one-sentence summary
- The publication date, marked up so a machine can read it
- The author's name
- An estimated reading time
- The topic it belongs to

### Table of contents

Links to each main part of the article.

### Article body

At least four main parts. Between them, the article must include:

- A diagram with a caption, plus enough text that a reader who cannot see the
  diagram gets the same information
- One block quotation from another writer, credited, with a link to the source
- One short quotation inside a sentence
- One code block showing markup, and at least two mentions of an element name
  inside a sentence
- One instruction telling the reader which keys to press
- One ordered list where the order matters, and one unordered list where it does
  not
- At least one nested list

### Article footer

- The author, with one or two sentences about them and their photograph
- The date the article was last updated
- The tags for this article

## Related Reading

Beside the article, include at least three related articles. Each entry needs a
title, a one-line description and a link. This content belongs *with* the
article but is not *part of* it.

## Newsletter Note

A short paragraph inviting readers to subscribe, with an email link. No form on
this page.

## Site Footer

Include:

- A copyright line
- Links to the blog's archive and feed
- A link back to the HTML challenge index, which is two levels up from the
  challenge folder

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Blog: The Markup Notebook
- Article title: "Your headings are not font sizes"
- Author: Omar Fathy, front-end engineer and workshop teacher
- Published: 12 May 2026, updated 2 June 2026
- Topic: Document structure
- Diagram: `./assets/images/article-semantic-structure.svg`
- Author photograph: `./assets/images/portrait-omar-fathy.svg`

The article argues that heading levels describe the structure of a document, not
the size of the text, and that choosing a heading by how big it looks produces
pages nobody can navigate.

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The code example must survive as written — do not let the browser collapse its
  whitespace, and make sure the angle brackets inside it display as characters
  rather than being parsed as markup.
- No tables on this page. Nothing here is tabular data.
- Do not use `<br>` or `<hr>` for spacing.
- Use relative paths so the page works on GitHub Pages.

---

# Accessibility Requirements

- One `<h1>`: the article title. Ask yourself whether the blog name should also
  be an `h1`, and be able to defend your answer.
- Heading levels step down one at a time. A part of the article is not the same
  level as the article title.
- The diagram's `alt` text carries its information. If the diagram shows a
  relationship, describe the relationship, not the shapes.
- Your two navigation areas are distinguishable from each other.
- Abbreviations such as HTML and WCAG are expanded on first use.
- Link text stands on its own out of context.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a "further reading" list of external specifications and documentation.
2. Add a correction note explaining what changed in the update, and mark up the
   corrected sentence as inserted and the old one as deleted.
3. Add a second diagram comparing a good and a bad heading outline.
4. Add `<link rel="canonical">` and author metadata to the document head.
5. Add a comments section where each comment is its own self-contained item with
   an author and a timestamp.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

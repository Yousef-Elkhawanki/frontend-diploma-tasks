# News & Magazine Homepage

Difficulty: Advanced

Estimated Time: 120–150 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Designing a document outline for a page with no single subject
  - A homepage is a collection of independent things — deciding what the `<h1>`
    of such a page even is
  - `<article>` for content that would still make sense republished elsewhere
  - `<section>` for the parts of this page that only make sense here
  - Nested articles: a story inside a group of stories
  - `<aside>` for content related to the page rather than to one story

- Multiple navigation areas
  - Primary navigation, section navigation, footer navigation
  - Making each one distinguishable to a screen reader user

- Search
  - `<search>` wrapping a search form
  - `<input type="search">` with `autocomplete` and a real label
  - Why `role="search"` is unnecessary once you use the right element

- Headings and taglines
  - `<hgroup>` for a headline with a standfirst that belongs to it
  - Keeping a strict heading hierarchy across twelve independent stories

- Publishing metadata
  - `<time datetime>` for publication and update times, including times with
    time zones
  - Bylines, sections, and reading times
  - `<meta name="description">`, `<link rel="canonical">`
  - `<link rel="alternate">` with `hreflang` for another language edition
  - `<link rel="alternate" type="application/rss+xml">` for a feed
  - Open Graph metadata

- Data tables on a news page
  - A weather table for the week
  - A market summary table with a footer row
  - `<caption>`, `<thead>`, `<tbody>`, `<tfoot>`, `colspan`, `<th scope>`

- Editorial text
  - `<blockquote>` and `<cite>` for a pulled quotation
  - `<figure>` and `<figcaption>` with a photograph credit
  - `<dl>` for a key-facts panel
  - `<abbr>`, `<strong>`, `<em>`, `<small>`

- Forms without a server
  - A newsletter sign-up with an email field and topic choices
  - A tip-off form with a file upload

- Accessibility
  - A skip link
  - Twelve headlines that all make sense read out of context
  - Photograph `alt` text that adds information rather than repeating the caption
  - Link text that is unique — five "Read more" links are five identical links

---

# Challenge

*The Norwich Chronicle* is a city news site: eight journalists, one editor, and a
homepage that is currently a single column of headlines with the date next to
each one.

You have been asked to rebuild the homepage. A homepage is the hardest kind of
page to structure, because it has no single subject — it is a collection of
independent stories, plus the furniture around them.

This is the final challenge. The requirements below say what must be on the page;
almost every structural decision is yours. Expect to change your mind about the
outline once while you build it.

Build the page using HTML only.

A reader should be able to:

- Scan today's news and understand what is important
- Read the top story's summary and open the full article
- Move between sections of the paper
- Search the archive
- Read the opinion column, the local sport result and the culture piece
- Check the week's weather and the market summary
- Find out what is most read and what is happening in the city this week
- Sign up to the newsletter, or send the newsroom a tip
- Find who publishes the paper, and how to complain

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Document Head

Include:

- A title that works as a browser tab and as a search result
- A description
- The canonical address
- A link to the paper's RSS feed
- A link to the Welsh-language edition, declared with the right language
- Open Graph metadata

## Skip Link and Masthead

Include:

- A skip link
- The paper's name and its founding year
- Today's date, machine-readable
- The edition (city or county)
- Primary navigation: News, Politics, Business, Culture, Sport, Opinion, Weather
- A second navigation area for the reader's own things: subscribe, sign in,
  saved articles
- A search form for the archive

## Top Story

One story, given more space than the others. Include:

- The headline and a standfirst that belongs to the headline
- A photograph with a caption and a credit
- The byline, the section, the publication time and the time it was updated
- Three or four paragraphs
- A key-facts panel
- A pulled quotation with its source
- A link to the full article

## Today's Other Stories

At least five stories. Each one is independent and must have a headline, a
byline, a publication time, a section, and either a summary or a photograph.

Group them so a reader can see that they belong together, and so that a single
story could be lifted out and republished without losing its meaning.

At least two of these stories must be photographed. At least one must carry an
update time as well as a publication time.

## Opinion

One column. Include the columnist's name, their photograph, the column's title,
the publication date, and a note that it is opinion rather than reporting.

## Sport

One result and one preview. The result must include the score and the venue.

## Culture

One review. Include what is being reviewed, where, until when, and a rating.

## Weather

A table for the next five days: day, description, highest temperature, lowest
temperature and chance of rain. Include the units once, not in every cell.

## Market Summary

A table of four local indicators — for example an index, a currency pair, a fuel
price and an average house price — with the change since last week, and a note
about when the figures were taken.

## Most Read and What's On

Content that relates to the page as a whole rather than to any one story:

- The five most read stories, in order
- Five things happening in the city this week, each with a date and a venue

## Newsletter

A sign-up form: email address, which newsletters, how often, and consent.

## Send Us a Tip

A short form: what happened, contact details, an optional file, and whether the
sender wants to remain anonymous.

## Footer

Include:

- The publisher, its address and its registered number
- Footer navigation: about, ethics policy, corrections, complaints, accessibility
  statement, jobs
- A line about the paper's press regulator
- A link back to the HTML challenge index, which is two levels up from the
  challenge folder

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Paper: The Norwich Chronicle, founded 1897
- Date: Friday 21 August 2026
- Photographs: `news-tram-extension.svg`, `news-harvest-drought.svg`,
  `news-school-robotics.svg`, `news-museum-reopening.svg`,
  `news-market-chart.svg`, `columnist-priya-nair.svg` in `./assets/images/`

Write realistic local news: a transport scheme, a drought affecting a harvest, a
school competition, a museum reopening, a planning decision, a hospital waiting
list. Invent the names of people and organisations; do not attribute quotations
to real people.

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The weather and the market summary are real tabular data. The story grid is
  not — do not lay it out with a table.
- Every story headline must be a link, and no two link texts on the page may be
  identical unless they genuinely go to the same place.
- ARIA only where HTML cannot express the relationship. In particular, do not put
  `role="search"` on the search form once you have used the element designed for
  it.
- Do not use `<br>` or `<hr>` for spacing.
- Use relative paths for local files so the page works on GitHub Pages.

---

# Accessibility Requirements

- A skip link, first in the tab order.
- Exactly one `<h1>`, and be able to defend what you chose.
- Every navigation area is distinguishable from the others.
- Heading levels never skip, including inside nested articles.
- Every photograph's `alt` text adds something the caption does not.
- Every date and time a reader sees is machine-readable.
- The search field has a real label, not just a placeholder.
- Link text is unique and meaningful out of context.
- The opinion column is identifiable as opinion in text, not only by position.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a live-coverage section where each entry is timestamped, newest first, and
   think about which list type expresses that.
2. Add a corrections and clarifications section with dated entries.
3. Add a puzzles section with a crossword clue list.
4. Add an obituaries section and consider what heading level it belongs at.
5. Add a second language edition link for each individual story.
6. Add a table of election results by ward, with turnout in the footer.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

# Online Learning Course Platform

Difficulty: Advanced

Estimated Time: 120–150 Minutes

---

# What You Will Practice

In this challenge, you will practice:

- Video and its text alternatives
  - `<video>` with `controls`, `poster`, `preload` and `width`/`height`
  - More than one `<source>`, so the browser can choose a format
  - `<track>` for captions, for captions in a second language, and for text
    descriptions — with `kind`, `srclang`, `label` and `default`
  - Fallback content for a browser that cannot play it
  - A downloadable transcript, and why the transcript is not optional

- State shown without scripting
  - `<progress>` with `value` and `max`
  - `<meter>` where a measurement, not a task, is being shown
  - Knowing the difference between the two

- Deeply structured content
  - A curriculum of modules, each containing lessons, using `<details>` and
    `<summary>` inside `<details>`
  - Heading hierarchy four levels deep, without skipping a level
  - `<article>` for content that stands alone, `<section>` for content that does
    not

- Durations and dates
  - `<time datetime="PT12M">` for a lesson length
  - `<time>` for release dates and deadlines

- A quiz form
  - One `<fieldset>` per question, with the question as its `<legend>`
  - Radio groups for single answers, checkbox groups for multiple answers
  - `<textarea>` with `minlength` and `maxlength` for a written answer
  - `<output>`-free, script-free result expectations — the form submits, nothing
    is calculated on the page

- Everything you have already learned
  - Landmarks, multiple navigation areas, breadcrumbs, description lists,
    quotations, metadata

- Accessibility
  - A skip link
  - Media with captions, descriptions and a transcript
  - A curriculum that can be navigated with a keyboard alone
  - Progress information that is not colour-dependent

---

# Challenge

Meridian Learn is a small online course platform. Their current course pages are
a video embed and a wall of text, and their support inbox is full of the same
three questions: how long is this, what do I need first, and where is the
transcript.

You have been asked to build the course page for *Accessible Web Media*: the
course description, the curriculum, the lesson the student is currently on, the
end-of-module quiz, and everything the support inbox keeps being asked.

This is an advanced challenge. Decide the document's outline before you write
any markup — this page has more nesting than anything you have built so far, and
a wrong decision early will show.

Build the page using HTML only.

A student should be able to:

- Understand what the course teaches, who teaches it, and what it costs
- See how far through the course they are
- Watch the current lesson, with captions, in their language if it is available
- Read the lesson transcript, or download it
- Work through the whole curriculum, module by module, lesson by lesson
- Take the end-of-module quiz
- Check the prerequisites, the certificate rules and the refund policy

---

# Requirements

Your page must contain the following areas. You decide which HTML elements are
correct for each one.

## Document Head

Include a title, a description, the page's canonical address, and metadata that
produces a sensible preview when a student shares the course.

## Skip Link and Page Header

Include:

- A skip link
- The platform name
- Platform navigation (Courses, My learning, Certificates, Help)
- A breadcrumb trail: platform, then Web development, then this course
- The signed-in student's name

## Course Overview

Include:

- The course title and a one-sentence summary
- The course cover image with a caption
- The instructor's name and a link to her profile
- Total length, number of modules, number of lessons, level and language
- The date the course was last updated
- How far the current student has got, shown as progress through a known total
- The average student rating, as a measurement
- Two or three paragraphs about the course
- What the student will be able to do at the end

## Current Lesson

The student is on module 2, lesson 3: *Captions, transcripts and audio
description*.

Include:

- The lesson title, its position in the course and its length
- The video, playable on the page, offering both provided formats
- Captions in English, captions in Arabic, and an English text-description track
- A poster image shown before the video plays
- Something useful for a student whose browser cannot play the video
- The full transcript on the page, or a clearly linked download of it
- Two or three paragraphs of lesson notes
- What to do next

Files:

- `../../assets/video/lesson-03-timelapse.mp4`
- `../../assets/video/lesson-03-timelapse.webm`
- `../../assets/images/video-poster-lesson-03.svg`
- `../../assets/captions/lesson-03-timelapse-en.vtt`
- `../../assets/captions/lesson-03-timelapse-ar.vtt`
- `../../assets/captions/lesson-03-timelapse-descriptions.vtt`
- `../../assets/downloads/lesson-03-transcript.txt`

The sample clip is silent on purpose. Your captions and your notes must handle
that honestly — a silent clip still needs a caption track, and a student who
cannot see it still needs to know what happens.

## Curriculum

Four modules, each containing three or four lessons.

For every lesson show its title, its length and its type — video, reading,
exercise or quiz. Show which lessons the student has completed, which one they
are on, and which are still locked.

A student must be able to open one module without opening the others, and open a
lesson's detail without leaving the module.

## End-of-Module Quiz

Five questions covering module 2:

1. One question with a single correct answer, chosen from four
2. One question where more than one answer is correct
3. One question that asks the student to choose the correct element from a list
4. One question with a true or false answer
5. One question that requires a written answer of at least 100 characters

Include the pass mark, how many attempts are allowed, and a submit control.

## Your Progress and Certificate

Include:

- Lessons completed against the total
- Quiz average, as a measurement
- The certificate rules: what has to be finished, what the pass mark is, and
  when the certificate is issued

## Instructor

Include her photograph, role, a short biography, what else she teaches, and a
link to her profile.

## Questions Students Ask

At least five, each openable on its own, including prerequisites, pace, the
certificate, refunds and whether the course covers a framework.

## Related Courses

At least three, each with a title, length, level and link. This content relates
to the page but is not part of the course.

## Footer

Include:

- Platform details
- Footer navigation, including an accessibility statement
- A link back to the challenge index at the root of the repository

---

# Content Requirements

Use realistic content. Do not use Lorem ipsum.

Suggested content:

- Platform: Meridian Learn
- Course: Accessible Web Media, 4 modules, 14 lessons, 5 hours 40 minutes
- Instructor: Lina Moreau, accessibility engineer
- Student: Adem Yilmaz, 7 of 14 lessons complete
- Images: `course-cover-media-accessibility.svg`, `portrait-lina-moreau.svg`,
  `video-poster-lesson-03.svg` in `../../assets/images/`

---

# Technical Rules

- HTML only. No CSS file, no `<style>` element, no `style` attribute.
- No JavaScript and no `<script>` element.
- No CSS framework.
- The video must not autoplay and must not loop.
- Captions must come from the provided WebVTT files, not from text on the page
  pretending to be captions.
- The progress indicator must use the element designed for progress, not a table
  or an image.
- Any table on this page must be real tabular data.
- Do not use `<br>` or `<hr>` for spacing.
- Use relative paths so the page works on GitHub Pages.

---

# Accessibility Requirements

- A skip link, first in the tab order.
- Exactly one `<h1>`.
- The video has captions by default, and the caption tracks are labelled with
  the language they are in.
- The transcript is available as text on the page or as a clearly described
  download — never only inside the video.
- Locked lessons are announced as locked in text.
- The curriculum's nesting is expressed by heading levels as well as by
  disclosure widgets.
- Every quiz question is a group with the question as its legend.
- Progress is understandable without seeing a bar.

---

# Bonus Challenges

All bonus work must stay HTML-only.

1. Add a discussion thread under the lesson, with each post self-contained.
2. Add a downloadable exercise file and a submission form for it.
3. Add a course schedule table with recommended weekly pace.
4. Add a second language's caption track and label it correctly.
5. Add a glossary of media accessibility terms as a description list.
6. Add a table comparing captions, subtitles, transcripts and audio description.

---

# Expected Result

Open the provided reference page to understand the expected content and page
structure.

Do not inspect the reference source code before completing your solution.

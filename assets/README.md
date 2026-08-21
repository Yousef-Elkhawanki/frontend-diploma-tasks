# Assets

Shared media used by the reference implementations. Every challenge links to
these files with relative paths, so the repository works when it is opened from
disk and when it is served from GitHub Pages.

## `images/`

Simple SVG placeholder graphics generated for this repository. Each file
carries a visible label so you can tell which photograph it stands in for, and
each one has an internal `<title>` and `<desc>`.

The reference pages write `alt` text as though the final photograph were in
place — that is deliberate. Describing the intended photograph is the skill you
are practising, and it is what you will do on a real project where the design
lands before the photography does.

Nothing in these files affects the pages that use them: an SVG is an image,
exactly like a JPEG or a PNG, so the HTML-only rule still holds.

## `audio/`

`comp204-lecture-04-excerpt.m4a` and `.wav` — a short synthesised lecture
excerpt, provided in two formats so that challenge 07 can practise offering
more than one `<source>` to the browser.

## `video/`

`lesson-03-timelapse.mp4` and `.webm` — a five second silent time-lapse of a
flower opening, 960 × 540. Used in challenge 10.

Source: [MDN shared assets](https://github.com/mdn/shared-assets), published
under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) (public
domain dedication). Included here so the challenge works offline.

## `captions/`

WebVTT tracks for the video: English captions, Arabic captions and an English
text-description track. The clip is silent on purpose — a silent clip is the
clearest way to show that captions carry information, not just dialogue.

## `downloads/`

Plain text and calendar files used to practise `<a download>` and links to
non-HTML resources. They are text files so that every asset in this repository
stays readable and reviewable.

## `embeds/`

Small standalone HTML documents that other pages embed with `<iframe>`. They
follow the same HTML-only rule as the challenges themselves.

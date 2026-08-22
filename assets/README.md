# Shared assets

This folder is for files that **more than one module** needs — a diploma-wide
logo, a data set reused by a CSS challenge and a JavaScript challenge, a font
licence, that kind of thing.

It is intentionally almost empty right now. Everything the HTML module uses
belongs to exactly one challenge, so it lives with that challenge instead:

```text
html/medium/01-personal-portfolio/
├── index.html
├── README.md
└── assets/
    ├── images/
    └── downloads/
```

## Which folder does an asset go in?

| Question | Answer |
| -------- | ------ |
| Is it used by exactly one challenge? | Keep it in that challenge's own `assets/`. |
| Is it used by several challenges in one module? | Put it in that module's own shared folder, for example `html/assets/`. |
| Is it used by more than one module? | Put it here, in the repository root `assets/`. |

Keeping challenge media inside the challenge means a challenge folder can be
copied, handed out or opened on its own, and unrelated media never piles up in
one directory.

## Conventions for anything added here

- Lowercase kebab-case filenames: `diploma-logo.svg`, not `Diploma Logo.svg`.
- Group by type in subfolders: `images/`, `audio/`, `video/`, `downloads/`.
- Reference it with a relative path from the page that uses it, for example
  `../../../assets/images/diploma-logo.svg`.
- Record the source and licence of anything not made for this repository, in this
  file, next to the entry for that file.

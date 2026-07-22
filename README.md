# alicebrocheux.github.io

Personal academic website, built on [LenPaul/academic](https://github.com/LenPaul/academic)
(a Jekyll theme), adapted to: **About** (home) → **Research** → **Teaching** → **CV**.
Served by GitHub Pages from `main` at https://alicebrocheux.github.io.

## Structure

```
index.md               About / bio (home page) — layout: about
research.md             Research page (intro text + publications list) — layout: research
teaching.md              Teaching page (course list) — layout: teaching
cv.md                     CV page — layout: cv

_config.yml               Site title/description
_data/settings.yml        Nav menu, footer social icons, list of courses taught
_data/publications.yml    Publications list, shown on the Research page
_data/cv/                 Education and Positions entries, shown on the CV page

_layouts/                 Page templates (about, research, teaching, cv, page, default)
_includes/                Shared header/footer/head snippets
_sass/, assets/css/       Styling (Bootstrap-based)
assets/img/               Photos — profile-placeholder.svg stands in for your photo
assets/cv/                Put your cv.pdf here — the CV page's "Download PDF" button
                           already links to assets/cv/cv.pdf
publications/             Put PDF copies of papers here if you want to self-host them
```

## Where to fill things in

Every editable spot is marked with an `<!-- EDIT: ... -->` comment or a
`[bracketed placeholder]`. In particular:

- **`_config.yml`** — your name and title/position.
- **`index.md`** — your title/position and bio paragraph (shown on the home/About page).
- **`research.md`** — description of your research; the publications list
  below it comes from `_data/publications.yml` (duplicate a `list` entry per
  publication there).
- **`teaching.md`** — optional intro text; the course list comes from the
  `teaching` key in `_data/settings.yml` (duplicate an entry per course).
- **`_data/cv/education.yml`** and **`_data/cv/academic-experience.yml`** —
  one entry per degree / position.
- **`_data/settings.yml`** — footer social links (GitHub/email by default;
  add more rows for LinkedIn, Twitter/X, ORCID, etc. — `icon` is any
  [Font Awesome brand name](https://fontawesome.com/search?o=r&f=brands)).
- **`assets/img/profile-placeholder.svg`** — replace with a real photo (e.g.
  `assets/img/profile.jpg`) and update the `src` in `_layouts/about.html`.
- **`assets/cv/cv.pdf`** — drop your CV PDF here; the download button on the
  CV page already points to it.

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`.

## Deploying

Push to `main` — GitHub Pages builds and serves this repo automatically at
`https://alicebrocheux.github.io` (enable it once under *Settings → Pages*
if it isn't already active).

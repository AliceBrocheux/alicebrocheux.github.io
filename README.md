# alicebrocheux.github.io

Personal academic website. Plain HTML/CSS, no build step — served directly by
GitHub Pages from `main`, live at https://alicebrocheux.github.io.

## Structure

```
index.html            About / bio (home page)
publications.html     Publications list
cv.html                CV page + PDF download link
assets/
  css/style.css       All styling — colors/fonts are CSS variables at the top
  img/                 Photos (avatar-placeholder.svg is a stand-in for your photo)
  cv/                  Put your cv.pdf here — cv.html already links to assets/cv/cv.pdf
```

## Where to fill things in

Every editable spot is marked with an HTML comment `<!-- EDIT: ... -->` and,
where there's no real content yet, visible `[bracketed placeholder text]`
styled in italics so it's obvious what's still a stub when you preview the page.

- **`index.html`** — your name, title/institution, bio paragraph, research
  description, research interests, social links (email/GitHub/Scholar/LinkedIn/X).
- **`publications.html`** — three sections (peer-reviewed / working papers /
  reports). Duplicate a `<li class="pub-entry">` block per publication, delete
  a whole `<section>` if you have nothing for that category yet.
- **`cv.html`** — structured sections (Education, Positions, Grants, Teaching,
  Skills) plus a "Download PDF" button. Drop your file at `assets/cv/cv.pdf`
  and the button works with no further changes.
- **`assets/css/style.css`** — top of the file has CSS variables (`--color-accent`,
  fonts, max width) that control the whole site's look from one place.

Nav links and footer are duplicated across the three pages (no templating,
by design, to keep this dependency-free) — if you rename a page or add a new
one, update the `<nav>` block in all three files.

## Local preview

Open `index.html` directly in a browser, or run a tiny local server:

```bash
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Deploying

Push to `main` — GitHub Pages serves this repo automatically at
`https://alicebrocheux.github.io` (enable it once under *Settings → Pages*
if it isn't already active).

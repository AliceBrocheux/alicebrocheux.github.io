# alicebrocheux.github.io

My academic website. Live at https://alicebrocheux.github.io.

## How to update it

You never need git, a terminal, or to understand how the site is built.
To change anything:

1. On github.com, open the file you want to change (list below).
2. Click the pencil icon (top right of the file) to edit it.
3. Type your changes directly — it's just plain text.
4. Scroll down, click **"Commit changes"**.
5. Wait about a minute — the live site updates itself automatically.

That's it. You can also just ask Claude to make the change for you in a
chat — describe what you want changed and it'll edit the file and publish it.

## The files you'll actually edit

The site is bilingual — English pages at the root, French pages in `fr/`.
Same 4 pages, just doubled:

| File | What it controls |
|---|---|
| `index.md` | Home page (English): your title/position and bio |
| `research.md` | Research page (English): description + publications list |
| `teaching.md` | Teaching page (English): list of courses |
| `cv.md` | CV page (English): education, positions, skills |
| `fr/index.md` | Home page (French) |
| `fr/research.md` | Research page (French) |
| `fr/teaching.md` | Teaching page (French) |
| `fr/cv.md` | CV page (French) |

Each one is plain text/Markdown — headings start with `#`, list items start
with `-`. No code to understand. The French pages started as blank templates
(not machine-translated) — write them yourself, or ask Claude to translate
your English content as a starting draft.

A language toggle (EN/FR) in the top nav switches between the matching page
in each language automatically — no need to maintain that link yourself.

To change your **name**, edit `_config.yml` (one line, `title: "..."`).

To change your **photo**, upload a new image to `assets/img/` (there's a
"Add file" button on github.com), then edit `_layouts/about.html` so the
`src=` on the `<img>` tag points at your new filename instead of
`profile-placeholder.svg`.

To add your **CV as a PDF**, upload it to `assets/cv/` named exactly `cv.pdf`
— the "Download PDF" button on the CV page already links there.

Everything else in this repo (`_layouts/`, `_includes/`, `assets/css/`,
`assets/libs/`) is styling/plumbing you shouldn't need to touch.

## Deploying

Every commit to `main` rebuilds the live site automatically via GitHub
Pages — there's no separate deploy step.

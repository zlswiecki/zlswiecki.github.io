# zachariswiecki.com

Personal academic site, built with [Quarto](https://quarto.org) and deployed to
GitHub Pages.

---

## Before you publish — three things

1. **Add a headshot** at `assets/photo.jpg` (roughly 4:5, ~600px wide), then in
   `index.qmd` replace the `.photo-placeholder` block with `![](assets/photo.jpg)`.
2. **Add your CV PDF** at `assets/Swiecki_CV.pdf`. The CV page links to it.
   (Export your final `Swiecki_CV_*.docx` to PDF — and check it doesn't include
   your referees' phone numbers, which the current docx does. They are
   deliberately not on the website.)
3. **Check the flagged items** in `NOTES.md`.

## Running it locally

```bash
quarto preview     # live reload at localhost:4200
quarto render      # build into _site/
```

If you have RStudio, Quarto is already bundled — `quarto` also works from the
RStudio terminal, and `.qmd` files get a Render button.

## Where the content lives

| File | What it is |
|---|---|
| `index.qmd` | Home page — positioning statement, the inference chain, current work |
| `research.qmd` | The research program, one section per link in the chain, plus funded projects |
| `publications.qmd` | Page shell — search box, filter buttons, the filtering script |
| `publications.yml` | **The publication list itself.** This is the only file you edit to add a paper |
| `_pubs.ejs` | Template that turns each YAML entry into HTML |
| `teaching.qmd` | Teaching approach, courses, supervision, workshops |
| `cv.qmd` | Web CV — appointments, education, awards, service, talks |
| `styles.scss` / `dark.scss` | All the styling. Palette variables are at the top of each |
| `_quarto.yml` | Site config — nav, theme, metadata |

## Adding a publication

Open `publications.yml` and add a block anywhere in the file. Sorting is
automatic.

```yaml
- title: "The title of the paper"
  author: "Lastname, A., & Swiecki, Z."
  year: 2026
  venue: "Journal of Learning Analytics, 13(1), 1–20"
  type: journal          # journal | chapter | conference | software | thesis
  url: "https://doi.org/..."   # optional
  award: "Best Paper Award"    # optional
```

Write your own name exactly as `Swiecki, Z.` — the page bolds that string
automatically.

## Deploying to GitHub Pages

**One-time setup:**

1. Create a public repo — `zachariswiecki.github.io` is the tidiest name.
2. Push this folder to it:

   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin git@github.com:<your-username>/zachariswiecki.github.io.git
   git push -u origin main
   ```

3. In the repo: **Settings → Pages → Build and deployment → Source: GitHub
   Actions**.

That's it. `.github/workflows/publish.yml` renders and deploys on every push to
`main`. The first run takes a couple of minutes; after that the site is live at
`https://<your-username>.github.io`.

**Then point the domain.** You already own `zachariswiecki.com` (currently
served by WordPress.com), so the URL on your CV does not have to change — only
what sits behind it.

1. Confirm the new site looks right on the `github.io` URL first.
2. At whoever holds the DNS for `zachariswiecki.com`, set:

   | Type | Name | Value |
   |---|---|---|
   | A | `@` | `185.199.108.153` |
   | A | `@` | `185.199.109.153` |
   | A | `@` | `185.199.110.153` |
   | A | `@` | `185.199.111.153` |
   | CNAME | `www` | `<your-username>.github.io` |

3. In **Settings → Pages → Custom domain**, enter `zachariswiecki.com` and tick
   **Enforce HTTPS** once the certificate is issued (usually under an hour).

The `CNAME` file in this repo already contains the domain, so GitHub keeps the
setting across deploys.

> **If the domain is *registered* through WordPress.com** rather than just
> pointed there: don't cancel the plan until DNS is switched and working, or you
> can lose control of the domain. Change the DNS records first, confirm the site
> resolves, then cancel.

## Cutting the WordPress site over

The old site has Home, Curriculum Vitae, Selected Publications and Projects.
Everything on it is superseded here except the three project write-ups
(Visualizing Team Performance, Themes of Thrones, Epistemic Network Analysis).
If you want any of those, copy the text across before you cancel the plan —
WordPress.com content is not exported by DNS changes.

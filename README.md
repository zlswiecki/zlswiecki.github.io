# zachariswiecki.com

Personal academic site, built with [Quarto](https://quarto.org) and deployed to
GitHub Pages.

---

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
| `index.qmd` | Home page — lede, what you work on, the three cards, background |
| `research.qmd` | Capture, code, model, test — plus the funded-projects list |
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

1. Create a public repo — `zlswiecki.github.io` is the name to use — it must match your username.
2. Point Terminal at this folder (`cd ` then drag the folder in from Finder),
   and push. This folder is already a git repository with its history, so there
   is nothing to initialise:

   ```bash
   git remote add origin git@github.com:zlswiecki/zlswiecki.github.io.git
   git push -u origin main
   ```

   If the push asks for a password, SSH keys aren't set up on this Mac. Either
   set one up, or use GitHub Desktop for this step instead — GitHub stopped
   accepting account passwords over HTTPS.

3. In the repo: **Settings → Pages → Build and deployment → Source: GitHub
   Actions**.

That's it. `.github/workflows/publish.yml` renders and deploys on every push to
`main`. The first run takes a couple of minutes; after that the site is live at
`https://zlswiecki.github.io`.






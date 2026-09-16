# zachariswiecki.com

Personal academic site, built with [Quarto](https://quarto.org) and deployed to
GitHub Pages.

---

## Before you publish

Both placeholders are now filled: the headshot is at `assets/photo.jpg` (with a
2x version at `assets/photo@2x.jpg`) and the CV is at `assets/Swiecki_CV.pdf`.
To swap either one, overwrite the file — the filenames are fixed, so no edit to
the pages is needed.

The remaining items to look over are in `NOTES.md`.

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

## Pointing the domain

### Where things currently stand

Checked against the public registration record, 15 Sep 2026:

| | |
|---|---|
| Registrar | **Automattic Inc.** (WordPress.com) |
| Nameservers | `NS1.WORDPRESS.COM`, `NS2`, `NS3` |
| Registered | 15 July 2019 |
| Paid through | **15 July 2027** |

So the domain was bought through WordPress.com. That is not a problem and does
not need to be changed. The key fact: **the site plan and the domain
registration are separate purchases with separate renewal dates.** Cancelling
the plan does not cancel the domain. The domain is only at risk if you delete
the whole WordPress.com account, or cancel within a refund window that refunds
the domain along with it.

WordPress.com lets you edit DNS records for domains registered with them, so you
can leave the registration exactly where it is and only change what the records
point at.

### The sequence (order matters)

1. **Push the site and confirm it on the `github.io` address.** Don't touch DNS
   until the new site is one you'd be happy for a search committee to see.

2. **Change the DNS records.** WordPress.com → **Domains** →
   `zachariswiecki.com` → **DNS records**. Replace the A records for `@`, and
   add the `www` CNAME:

   | Type | Name | Value |
   |---|---|---|
   | A | `@` | `185.199.108.153` |
   | A | `@` | `185.199.109.153` |
   | A | `@` | `185.199.110.153` |
   | A | `@` | `185.199.111.153` |
   | CNAME | `www` | `<your-username>.github.io` |

   WordPress.com may ask you to disconnect the domain from the WordPress site
   first, or offer a "point to another service" option. Either is fine.
   Propagation takes minutes to a few hours.

3. **Turn on the custom domain in GitHub.** Repo **Settings → Pages → Custom
   domain**: enter `zachariswiecki.com`, then tick **Enforce HTTPS** once the
   certificate is issued (usually under an hour). The `CNAME` file in this repo
   already holds the domain, so the setting survives deploys.

4. **Wait a week.** Nothing is lost by leaving the WordPress plan running in the
   background; the old site is simply no longer reachable at the domain.

5. **Only then, cancel the WordPress.com site plan** — and keep the domain
   renewal switched on. If the cancellation flow offers to refund or release the
   domain, decline that part.

Every step before 5 is reversible: put the old DNS records back and the
WordPress site returns.

### Later, optionally

Moving the domain to a dedicated registrar (Cloudflare sells at cost, ~$10/yr,
and doesn't upsell) is tidier long-term but has no urgency — a transfer takes
about a week and the domain is paid through July 2027. Do it when nothing is
riding on it.

## Cutting the WordPress site over

The old site has Home, Curriculum Vitae, Selected Publications and Projects.
Everything on it is superseded here except the three project write-ups
(Visualizing Team Performance, Themes of Thrones, Epistemic Network Analysis).
If you want any of those, copy the text out before cancelling the plan — DNS
changes don't export content, and cancelling the plan eventually takes the pages
with it.

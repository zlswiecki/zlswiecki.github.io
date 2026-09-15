# Things to check before this goes live

I built `publications.yml` from `Swiecki_CV_1025.docx`. A few things in the
source needed a judgement call or looked like typos. I fixed the obvious ones on
the site, but **the same errors are still in the CV docx**, which matters more
than the website does this week.

## Fixed on the site — still wrong in the CV

| Item | In the CV | On the site |
|---|---|---|
| Funding body, two ARC projects | "Australian Council for Research" | Australian Research Council |
| HARNESS / knowledge management funder | "Defense Agency Research Projects Agency" | Defense Advanced Research Projects Agency |
| Swiecki et al. 2022, *Assessment in the age of AI* | "Khosrai, H." | Khosravi, H. |
| Yang et al. 2024, Augmented Humans | "Bilinghurst", "Wulandari, Te." | Billinghurst, M.; Wulandari, T. |
| Herder et al. 2018 | "teacher's intervention in student's" | teachers' intervention in students' |
| Program committee list | "ICEQ23" | ICQE23 |
| Alfredo et al. 2024, *Human-centred LA and AI in education* | Fernandez-Nieto listed without initial | Fernandez-Nieto, G. |

## Needs your decision — I did not guess

1. **Markovetz et al. (2017)**, *IJEE* 33(6). The CV gives the page range as
   **1834–1831**, which runs backwards. I put **1834–1841** on the site as the
   likeliest reading, but I have not verified it. Please check the article.

2. **Author order, Swiecki et al. (2022)**, *Assessment in the age of artificial
   intelligence*. The CV lists Khosravi, Lodge, Chen, Martinez-Maldonado; I used
   the order I believe was published — Khosravi, Chen, Martinez-Maldonado,
   Lodge. Worth a ten-second check against the paper, since it's your own
   first-author piece.

3. **Advanced ENA and rENA workshop** is listed as *"(2026, October) … hosted by
   the Seventh International Conference on Quantitative Ethnography (ICQE25).
   Mexico City"*. The year and the conference number disagree. Workshops aren't
   on the publications page, so this only affects the CV.

4. **ICQE ordinal numbers are inconsistent** in the CV: ICQE24 is called "the
   Sixth" under Service and "the Seventh" under Workshops. ICQE25 is also called
   "the Seventh".

5. **Missing from the CV, and therefore from the site**: your in-press and
   under-review papers, and any 2026 publications. You flagged these as
   outstanding — they're the most valuable thing to add before the 18th.

6. **`assets/Swiecki_CV.pdf` does not exist yet.** The CV page links to it, so
   that link is broken until you add the file. This is the one thing that will
   look bad to a search committee, so do it before you point the domain.

## Deliberately left off

- **Your referees' names, emails and phone numbers.** They're in the CV docx,
  which is fine for an application, but publishing other people's mobile numbers
  on a public website isn't. The web CV ends at Contact.
- **SETU teaching scores.** Accurate and good, but raw internal evaluation
  numbers read oddly on a personal site. They belong in the teaching statement.
- **Invited talks, workshops, posters** beyond a selected handful — they're on
  the CV page in summary and in the PDF in full.
- **The Jacobs Foundation project** is listed under funded projects as it appears
  on your CV. Given that you're wary of it reading as part of your own funding
  record, you may want to drop it from `research.qmd` — it's the last entry.

## One CV edit this unblocks

Your CV's contact block currently gives the Monash profile page as "Website".
Once the domain is switched, that line becomes:

```
Website    zachariswiecki.com
```

which was on your outstanding-items list.

# Website copy — draft for review

Home page in voice **B** (what people actually do), research page in voice
**C** (the methods builder). Nothing here is lifted from the research
statement, teaching statement or cover letter — different audience, different
job.

**How to use this file.** Edit directly, strike things out, write "no" in the
margin. Anything in a `>` blockquote is my note to you, not copy for the site —
those come out. Once you've marked it up I'll push the changes into the `.qmd`
files and rebuild.

---

## 1. Home page — `index.qmd`

### Role line

> Sits under your name, small grey type. **Settled.**

**ARC DECRA Fellow**, Faculty of Information Technology, Monash University

> The Senior Lecturer continuing appointment stays on the CV rather than here.

### Lede

> Large serif type beside the photo. This is the sentence people actually read.
> **Settled.**

I study how we can say something meaningful about a person from activity they
didn't carry out alone. Most of what people do that's worth understanding is
done with other people, with tools, and in settings that shape the work.

> Two sentences, 36 words — about half what it was, and better for it. The
> "finished product is the least informative part" idea isn't lost; it reappears
> more concretely as *read the essay, judge the writer* in the next section.

### What I work on

> First section under the hero.

I build tools that record how work unfolds, methods for making sense of those
records, and ways of showing them back to the people involved. Most of my
current work looks at writing with AI — what people ask of these tools, what
they do with the answers, and what separates the sessions where something is
learned from the ones where something is merely produced.

The problem itself is old. What's changed is that the usual shortcut — read the
essay, judge the writer — has stopped working, which makes it impossible to put
off any longer.

> You're right, and it was my error — "none of this" lands on the nearest thing,
> which was your work. *The problem itself* can only point at the problem, and
> the implied contrast now runs the right way: old problem, new means of
> attacking it.
>
> If you want that contrast stated rather than implied:
>
> *The problem is old. What's new is that the usual shortcut — read the essay,
> judge the writer — has stopped working, and that we finally have instruments
> equal to the alternative.*
>
> Stronger claim, and it's yours to make — the instruments in question are
> largely ones you built. Slightly less modest than the rest of the page.

### The cards

> **Settled:** three cards naming what you've built, replacing the five
> Observe / Code / Model / Claim / Represent cards. Each links to its section on
> the research page.

**[Trace](research.qmd#capturing-activity)** — Software that records writing
sessions as they happen, across the tools people already use.

**[Network models](research.qmd#modelling-interaction)** — Ways of finding
structure in coded interaction, and of seeing what that structure is doing.

**[Validation](research.qmd#testing-the-methods)** — Simulation and testing that
establish what these methods can and can't support.

> Layout note: three cards across is roomier than five, so each gets a bit more
> width and the row reads better on a phone — they'll stack into three rather
> than wrapping awkwardly into two-and-three.

### ~~Currently~~ — cut

> **Dropped.** It was the highest-maintenance thing on the site and the first
> part that would have gone stale. The current projects live on the research
> page, where they're part of an argument rather than a status update.
>
> One consequence: the home page no longer mentions the ARC projects at all. The
> research page carries them with amounts and roles, so nothing is lost — but if
> you want a single line of "what I'm funded to do right now" up front, it would
> go at the end of the background paragraph instead.

### Background

I'm a learning analytics researcher at Monash University, where I hold an ARC
Discovery Early Career Researcher Award (2026–2029). I studied physics and
mathematics as an undergraduate, then did a PhD in educational psychology at the
University of Wisconsin–Madison. I've been building methods for studying
collaboration and learning ever since.

I sit on the editorial boards of the *International Journal of
Computer-Supported Collaborative Learning* and the *Journal of Quantitative
Ethnography*, and I help organise the LAK and ICQE conferences.

> "By way of" gone — it was doing decorative work. Three plain sentences now.
>
> On the label, one thing worth weighing before it's settled. **Learning
> analytics researcher** is the more accurate description of where you publish
> and what you build, and it fits a Faculty of IT home. **Learning scientist** is
> the broader disciplinary identity and the one that matches a Learning Sciences
> department.
>
> Since the site may be read by people evaluating you for exactly that kind of
> post, the narrower label does a small amount of work against you — it reads as
> a methods specialism rather than a field. Not decisive, and the site outlives
> any one application.
>
> A third option sidesteps it by describing instead of labelling:
>
> *I build methods for studying how people learn and work together, at Monash
> University, where I hold an ARC Discovery Early Career Researcher Award.*
>
> Your call — I've put your preference in above.

> **Settled.** DECRA with its dates, a one-sentence service line, no Epistemic
> Analytics Lab.
>
> "Help organise the LAK and ICQE conferences" is deliberately understated —
> you've been program co-chair of one and you chair a LAK26 track, which the CV
> spells out. On a home page the modest version reads better and the specifics
> are a click away.

---

## 2. Research page — `research.qmd`

> **Cut from ~1,040 words to ~560.** You were right that it was too detailed —
> it had drifted into being a research statement, which is the thing we set out
> to avoid. The old version explained *why* each methodological choice was
> right. That argument belongs in the papers; this page only has to say what you
> work on and what you've built, credibly enough that someone goes and reads
> one.
>
> Six sections become four — capture, code, model, test — plus a short opening
> and a closing paragraph. The three home-page cards point at capture, model and
> test. Everything cut is still on the site, in the publication list, or in the
> papers themselves.
>
> **If you'd rather remove the page entirely:** I'd advise against it. A
> research page is the most-expected thing on an academic site, and without it
> someone who wants to know what you do has 150 words and a list of 83 titles.
> But if you want it gone, the three cards become the whole story and I'd move
> the funded-projects list onto the CV page.

### Opening

Most of what people do that's worth understanding, they do with others and with
tools. That makes it hard to study — the record of what happened is scattered,
the interesting structure is in how actions relate to one another rather than in
any one of them, and the finished product hides most of it.

I build the apparatus for getting at that structure — software for capturing
activity, schemes for coding it, models for finding pattern in it, and tests for
knowing when to believe the results. Mostly I apply it to writing and
collaborative problem-solving, and lately to what happens when one of the
participants is a machine.

### Capturing activity

Studying process needs a record of it, and that record has usually been
expensive to get. *Trace* records writing sessions as they happen — what people
read, type, ask and paste — either in a self-contained web platform or through a
browser extension that follows people into the tools they already use. It has
carried studies ranging from single sessions with a few hundred students to
six-week longitudinal work, and it's increasingly taken up beyond my own
projects.

### Coding it

A record isn't useful until something decides which parts of it matter and what
they mean, and that decision is where the theory lives. I build coding schemes
that work from both ends — the categories a literature hands you and the
categories the data insists on. Lately that work has moved to language models as
coders, which raises a problem earlier methods didn't have. Their
classifications shift with the prompt and with the model version, so agreement
demonstrated once doesn't stay demonstrated, and much of what I'm doing now is
working out what has to be re-checked and how often.

### Modelling interaction

Counting coded actions one at a time throws away how they relate to each other;
treating a whole session as a single unit throws away the differences between
the people in it. Epistemic network analysis and ordered network analysis model
those relationships instead, and I'm a co-author of the software most people use
to run them as well as of the mathematics underneath. More recent work joins
them to graph neural networks — more representational power, and the harder
problem of keeping the results readable.

> Vague, and you caught it. Named now. The two failure modes are opposite ends
> of the same mistake — too atomistic loses the relations, too aggregate loses
> the individuals — and naming the second one connects this page back to the
> home page lede, which is about saying something about a *person* from joint
> activity. That link was implicit and is now actually there.

### Testing the methods

The models themselves are new enough that we don't fully know how they behave. I
test them by simulation — generating interaction data where the answer is
already known, running it through the pipeline, and seeing what comes back. It's
a way of establishing what a method can and can't support before anyone rests a
claim on it.

> You're right, and this was a casualty of the compression. The cut collapsed
> two different kinds of validity work into one paragraph: whether the *coding*
> is trustworthy, and whether the *model* behaves. They're related but they're
> about different objects, and running them together made both vague.
>
> Coding now has its own short section above, where the LLM-classifier problem
> belongs. This section is just about testing the models. Four sections rather
> than three — still 570 words against the original 1,040, and the three cards
> on the home page still point at real headings.

### What comes of it

My work suggests that writing with AI is neither good nor bad in itself; what
matters is how. What separates stronger work from weaker isn't whether someone
used a chatbot but the shape of the exchange they had with it, which the
finished text doesn't show. The next questions are scale — whether any of this
holds across disciplines and institutions rather than the courses I happen to
teach — and agents, which change the interaction enough that most of the
apparatus needs rethinking.

> The funded projects list stays at the bottom of the page, unchanged. It's a
> record, not voice.

---

## 3. Smaller bits

### Teaching page opener — `teaching.qmd`

> Current version opens on cognitive apprenticeship and the visibility of expert
> judgment. That's teaching-statement language. Plainer:

Most of what makes someone good at research is invisible. The reasoning behind
a choice of method, the moment you notice your data isn't going to support the
claim you wanted — students may not see any of it unless you make a point of
showing them. My teaching is largely an attempt to work in the open — real
decisions, real data, including the ones I get wrong. That's also why I assess
the way I do. You can't coach reasoning you can't see, so I ask for the process
as well as the product.

> One extra change while merging: the fourth sentence began "Most of my
> teaching", echoing "Most of what makes someone good" two lines above. It's now
> "My teaching is largely". Say if you'd rather have the echo back.

### Site meta description

> Search results and link previews. One sentence.

Learning analytics researcher at Monash University. I study how people work with
tools —
building software to capture activity, methods to make sense of it, and models
to find structure in it.

---

## 4. Things to decide

**Nothing open — everything below is decided.**

**Settled**

- Role line — DECRA only, one line.
- Lede — voice A, two sentences.
- "What I work on" — kept, with the old-problem framing fixed.
- Cards — three, naming Trace, the network models and the validation work.
- "Currently" — cut.
- Self-description — *learning analytics researcher*, pending the note in §1.
- Background — DECRA with dates, one service line, no Epistemic Analytics Lab.
- Colons — swapped for dashes throughout.
- Research page — cut to ~560 words, four sections, coding separated from
  testing.
- Teaching opener — one paragraph, "may not".
- Meta description — approved as drafted.
- AI up front — lede stays general; no change.
- Spelling — **British throughout**. This draft is already clean; the sweep
  needs applying to the rest of the site when I fold these changes in.
  Publication titles keep their published spelling, and *program co-chair* stays
  as the official title of the role.

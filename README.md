# Learning Demand Dashboard

A monthly market scan that ranks candidate topics for short online courses — built to bring agile practice into instructional design.

**Live dashboard:** `https://<your-username>.github.io/learning-demand-dashboard/`
*(replace with your URL once Pages is enabled — see [Setup](#setup-publishing-to-github))*

---

## The problem this addresses

Online course development at most institutions fails in a predictable way, and it fails for two compounding reasons.

### Problem 1 — Topic decisions are made without market evidence

Courses get greenlit on the strength of internal conviction: a faculty member's specialism, a department's existing capability, an executive's read of the industry, or last year's enrolment pattern. Sometimes there's a survey of current students, which asks people already inside the funnel what they want and misses everyone who never applied.

What almost never happens is a structured look at what people outside the institution are actively searching for, paying for, and failing to find.

When research does happen it's usually a one-off — commissioned at the start of a programme, never repeated. By the time the course launches, that research describes a market that has moved. In a field like AI, where the fastest-growing skill on Upwork grew 329% in a single year, a snapshot taken twelve months ago is not a weak signal. It's a wrong one.

### Problem 2 — Development takes so long the content is stale at launch

The standard model is waterfall. Analyse, design, develop every asset, then launch. A full course is commonly nine to eighteen months from approval to first cohort.

Two things go wrong across that span:

**The market moves underneath you.** Tool-dependent content is the worst case — screen recordings of a software interface can be obsolete within a quarter — but topic relevance decays too. A gap that was real at kickoff may be filled by a competitor before you ship.

**Feedback arrives only after the money is spent.** The first real signal is enrolment, and the second is completion rate. Both arrive after full production cost has been incurred. When they come back weak, the diagnosis is too late to act on: the cost is sunk, the team has moved on, and the honest conclusion — that the topic was wrong — is the most expensive one to admit.

**The two problems reinforce each other.** Weak upfront research raises the chance of picking the wrong topic. Long development guarantees you won't discover the mistake until it's unaffordable to fix.

---

## What this dashboard changes

It attacks the first problem directly and makes the second one tractable.

**Research becomes continuous instead of one-off.** The scan re-runs monthly. Each cycle is committed to version control, so the record accumulates: you can compare August against July and see which topics rose, which gaps closed, and what evidence changed. A single snapshot tells you where the market is. A run of snapshots tells you where it's going, which is the more useful question.

**Topic selection becomes auditable instead of intuitive.** Every candidate is scored against four published criteria — demand, willingness to pay, how underserved the need is, and how fast a minimum viable version could ship. The rubric is documented, the evidence is cited, and each claim carries a source-quality tag. When someone asks why this topic and not that one, the answer is a reasoned argument rather than a preference.

**The bar for "worth building" drops to something testable.** Because scope is constrained to a one-hour lesson buildable in under four weeks, being wrong costs a month rather than a year. That constraint is deliberate. It's what makes it rational to test a topic you're unsure about instead of only building the safe ones.

**Competitive position is measured, not assumed.** Each cycle reads competitor syllabi directly and records what they cover. Gaps are identified from what's demonstrably missing across the market, not from a hunch that nobody's doing it.

That last point is not theoretical. In this project's first cycle, the top-ranked topic was a use-case discovery course, chosen on the reasoning that the market teaches tools while learners can't identify where AI fits. Reading IBM's actual syllabus the same day disproved it — they already ship exactly that course, with 8,319 enrolments and a 4.7 rating. The recommendation was wrong and got caught within hours instead of after a build. The full correction is recorded in [`docs/CHANGELOG.md`](docs/CHANGELOG.md).

---

## How it works

**Input.** Each cycle gathers demand signals from primary sources — annual skills reports from Coursera and Upwork, read in full including their methodology sections — plus adoption research, regulatory timelines, and direct reads of competitor course pages.

**Processing.** Candidates are scored 1–10 on four factors against a published anchoring rubric, then combined into a weighted average. Defaults are demand 30%, willingness to pay 25%, underserved gap 25%, buildability 20%.

**Output.** A ranked shortlist, each entry carrying its demand evidence, the argument for why it's underserved, the risks to check before building, buildability notes, and source links. Plus a watchlist of candidates that were scored but didn't make the cut, so the reasoning isn't lost.

**The sliders matter more than the ranking.** The four weights are adjustable in the browser and the list reorders live. This is the feature to actually use: if you disagree with the default emphasis, change it and see whether the conclusion survives. A topic that stays at the top across several weightings is a more robust bet than one that only wins under a single configuration.

---

## What it does not do

This is a decision aid for choosing what to *test* next. It is not evidence that any topic will sell.

The sub-scores are analyst judgements anchored to cited evidence, not measurements. A gap of 8.50 versus 8.35 sits inside the scoring error. A high score justifies building a landing page with a real price and seeing whether anyone converts — nothing more. Full limitations are documented in [`docs/METHODOLOGY.md`](docs/METHODOLOGY.md), and reading them before relying on any number here is strongly advised.

---

## What's in here

```
├── index.html                          the dashboard (open in any browser)
├── data/
│   └── topics.json                     all scored data — edit this to refresh
├── docs/
│   ├── METHODOLOGY.md                  how topics are researched and scored
│   ├── competitive-analysis-2026-07.md competitor syllabus study, cycle 2026-07
│   └── CHANGELOG.md                    what changed each cycle, and why
└── .nojekyll                           tells GitHub Pages to serve files as-is
```

The dashboard reads `data/topics.json` at load. If that fetch fails — which happens when you open `index.html` directly from your hard drive rather than over a web server — it falls back to an identical copy embedded in the HTML. So it works either way, but **on GitHub Pages the live file is what renders.**

---

## Setup: publishing to GitHub

No installation or command line needed. The web interface is enough.

### First time

1. Go to [github.com/new](https://github.com/new). Name the repository `learning-demand-dashboard`. Set it to **Public** (required for free GitHub Pages). Do not add a README — you already have one.
2. On the new empty repo page, click **uploading an existing file**.
3. Drag in the entire contents of this folder. GitHub preserves the `data/` and `docs/` subfolders when you drag the folders themselves.
4. Write a commit message such as `Initial dashboard, cycle 2026-07` and click **Commit changes**.
5. Go to **Settings → Pages**. Under *Source*, choose **Deploy from a branch**. Set branch to `main` and folder to `/ (root)`. Click **Save**.
6. Wait two or three minutes. Your dashboard will be live at `https://<your-username>.github.io/learning-demand-dashboard/`.

> **On `.nojekyll`:** GitHub Pages runs files through Jekyll by default, which ignores folders beginning with an underscore and occasionally interferes with plain static sites. The empty `.nojekyll` file switches that off. It has no other effect. Note that some file managers hide dotfiles — if you don't see it when dragging, enable hidden files (macOS: `Cmd+Shift+.` in Finder).

### Each month after that

1. Open the repo on GitHub, navigate into `data/`, click `topics.json`.
2. Click the pencil icon to edit, paste in the new month's data, commit.
3. Pages redeploys automatically within a couple of minutes.

You only ever need to replace `data/topics.json`. The dashboard code doesn't change between cycles.

---

## Does this update itself?

**No, and it's worth being precise about why.**

Three separate things could be automated, and they have different answers:

| Step | Automated? | Who does it |
|---|---|---|
| Researching the new month's demand data | Can be scheduled | Claude, on a monthly schedule |
| Producing an updated `topics.json` | Can be scheduled | Claude, same run |
| **Committing that file to GitHub** | **No** | You, manually |

Everything up to producing the file is automatable. The commit is not, unless a GitHub connector is available and scoped to the session doing the work.

**The practical monthly loop:** Claude runs the scan on a schedule and hands you a fresh `topics.json`; you paste it into GitHub and commit. About two minutes of your time.

---

## Using the dashboard

**Weight sliders.** Drag to re-weight the four factors; the ranking reorders live. Weights don't need to total 100 — scores are normalised against whatever total you set.

**Expandable topic cards.** Click any topic to open its evidence, the reasoning for why it's underserved, risks to check before building, buildability notes, and source links.

**Source tiers.** Claims carry a tag: `[A]` primary source read directly, `[B]` secondary such as trade press or a law firm, `[C]` weak — SEO content with unstated methodology. Some `[C]` claims are load-bearing and flagged as such.

---

## Licence

Add one if you're publishing publicly. [MIT](https://choosealicense.com/licenses/mit/) is the usual choice. Note that the underlying source material — Coursera's and Upwork's reports — remains theirs; this repo cites it rather than reproducing it.

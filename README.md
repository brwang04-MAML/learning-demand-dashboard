# Learning Demand Dashboard

A monthly market scan that ranks candidate topics for short online courses — built to bring agile practice into instructional design.

**→ [View the live dashboard](https://brwang04-maml.github.io/learning-demand-dashboard/)**

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

**The two problems reinforce each other.** Weak upfront research raises the chance of picking the wrong topic. Long development guarantees the mistake stays hidden until it's unaffordable to fix.

---

## What this dashboard changes

It attacks the first problem directly and makes the second one tractable.

**Research becomes continuous instead of one-off.** The scan re-runs monthly, and every cycle is committed to version control, so the record accumulates. August can be compared against July to see which topics rose, which gaps closed, and what evidence changed. A single snapshot shows where the market is. A run of snapshots shows where it's going, which is the more useful question.

**Topic selection becomes auditable instead of intuitive.** Every candidate is scored against four published criteria — demand, willingness to pay, how underserved the need is, and how fast a minimum viable version could ship. The rubric is documented, the evidence is cited, and each claim carries a source-quality tag. When someone asks why this topic and not that one, the answer is a reasoned argument rather than a preference.

**The bar for "worth building" drops to something testable.** Because scope is constrained to a one-hour lesson buildable in under four weeks, being wrong costs a month rather than a year. That constraint is deliberate. It's what makes it rational to test an uncertain topic instead of only building safe ones.

**Competitive position is measured, not assumed.** Each cycle reads competitor syllabi directly and records what they cover. Gaps are identified from what's demonstrably missing across the market, not from a hunch that nobody's doing it.

That last point is not theoretical. In this project's first cycle, the top-ranked topic was a use-case discovery course, chosen on the reasoning that the market teaches tools while learners can't identify where AI fits. Reading IBM's actual syllabus the same day disproved it — they already ship exactly that course, with 8,319 enrolments and a 4.7 rating. The recommendation was wrong, and it was caught within hours rather than after a build. The full correction is recorded in [`docs/CHANGELOG.md`](docs/CHANGELOG.md).

---

## How it works

**Input.** Each cycle gathers demand signals from primary sources — annual skills reports from Coursera and Upwork, read in full including their methodology sections — plus adoption research, regulatory timelines, and direct reads of competitor course pages.

**Processing.** Candidates are scored 1–10 on four factors against a published anchoring rubric, then combined into a weighted average. Defaults are demand 30%, willingness to pay 25%, underserved gap 25%, buildability 20%.

**Output.** A ranked shortlist, each entry carrying its demand evidence, the argument for why it's underserved, the risks to check before building, buildability notes, and source links. Plus a watchlist of candidates that were scored but didn't make the cut, so the reasoning isn't lost.

**The sliders matter more than the ranking.** The four weights are adjustable in the browser and the list reorders live. This is the feature to actually use: change the emphasis and see whether the conclusion survives. A topic that stays at the top across several weightings is a more robust bet than one that only wins under a single configuration.

---

## What it does not do

This is a decision aid for choosing what to *test* next. It is not evidence that any topic will sell.

The sub-scores are analyst judgements anchored to cited evidence, not measurements. A gap of 8.50 versus 8.35 sits inside the scoring error. A high score justifies building a landing page with a real price and seeing whether anyone converts — nothing more.

Full limitations are documented in [`docs/METHODOLOGY.md`](docs/METHODOLOGY.md) and worth reading before relying on any number here.

---

## Reading the dashboard

**Weight sliders.** Drag to re-weight the four factors; the ranking reorders live. Weights need not total 100 — scores are normalised against whatever total is set.

**Topic cards.** Click any topic to expand its demand evidence, the argument for why it's underserved, risks to check before building, buildability notes, and source links.

**Source tiers.** Every claim carries a tag: `[A]` primary source read directly, `[B]` secondary such as trade press or a law firm, `[C]` weak — SEO content with unstated methodology. Some `[C]` claims are load-bearing and are flagged as such on the card.

---

## Repository contents

| Path | Contents |
|---|---|
| `index.html` | The dashboard |
| `data/topics.json` | All scored data for the current cycle |
| `docs/METHODOLOGY.md` | How topics are researched and scored, and the limitations |
| `docs/competitive-analysis-2026-07.md` | Competitor syllabus coverage matrix, cycle 2026-07 |
| `docs/CHANGELOG.md` | What changed each cycle, and why |

---

## Licence

Released under the [MIT Licence](https://choosealicense.com/licenses/mit/). The underlying source material — Coursera's and Upwork's published reports — remains theirs; this project cites it rather than reproducing it.

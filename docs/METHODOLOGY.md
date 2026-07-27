# Methodology

How topics get onto this dashboard, how they get scored, and what the numbers can and cannot support.

---

## 1. The problem this is solving

Traditional course development at institutions follows a waterfall: assume a market need, design the full curriculum, build every asset, launch. Feedback arrives only after launch, usually as low enrollment or high drop-out. The cost is already sunk and the diagnosis comes too late to act on.

The agile alternative inverts the order: gather market evidence first, ship a minimum viable lesson, collect real learner behavior, and only then invest in production polish. This dashboard is the evidence-gathering step. Its job is to answer **"which topic should we test next month?"** — not "which topic will succeed."

That distinction matters throughout what follows.

---

## 2. How the current recommendation was derived

The analysis ran in five stages. Stage 4 overturned the conclusion of stage 3, which is the most useful thing about the record.

### Stage 1 — Fix the audience before scoring anything

Willingness to pay varies by roughly an order of magnitude across buyer segments, so topic ranking is meaningless until the buyer is fixed.

| Segment | Typical price | Speed to close | Fit for a monthly test loop |
|---|---|---|---|
| Corporate L&D (B2B) | $200–$2,000/seat; deals $3k–$50k+ | Months — procurement, vendor vetting | Poor. Feedback loop far too slow |
| Small business owners / solopreneurs | $99–$497 self-paced | Days — they are the buyer | **Best.** High WTP, instant decision |
| Working professionals (B2C) | Median ~$97 | Days | Good volume, thin margin, most saturated |
| Educators / instructional designers | Lowest — they build their own | Fast, small market | Weak revenue; good free beta testers |

**Decision: small business owners as primary buyer, working professionals as a lower-priced secondary tier.** Same content, two framings, two price points.

Two findings shaped this and continue to shape pricing:

- B2B-framed content commands 2–3x B2C prices at every tier. The same lesson sells for ~$97 as self-improvement and ~$297 as "cut proposal-writing time in half." Framing is the price lever, not length. `[C]` — single weak source, load-bearing, unverified.
- Structure and accountability drive price tolerance more than information does; learners pay substantially more for cohort delivery than identical self-paced content. So the MVP should be cheap and self-paced, with cohort delivery as the later margin play. `[C]`

### Stage 2 — Demand scan

Fifteen web searches across course marketplaces, skills reports, freelance-market data, SMB adoption surveys, regulatory timelines, and saturation commentary. This produced roughly a dozen candidate topics and the market context shown on the dashboard.

### Stage 3 — First scoring pass (rev A)

Candidates scored 1–10 on four factors and ranked by weighted average. Top pick: a use-case-discovery course, on the reasoning that the market teaches tools while learners can't identify where AI fits.

**This pass had a weakness that the polish of the output concealed:** two of four columns — underserved gap and buildability — had no measurement behind them at all. No competing courses had been counted. The gap scores were inference from reading that courses existed.

### Stage 4 — Primary sources and measured competition (rev B)

Two changes:

**Primary reports fetched in full**, replacing search-result summaries. The Coursera *Job Skills Report 2026* (six million enterprise learners across ~7,000 institutions, 2023–2025, vendor-specific skills filtered out) and Upwork's *In-Demand Skills 2026* (freelancer earnings on completed US jobs, 2025 vs 2024, minimum $100k aggregate earnings per skill).

Reading Upwork's methodology surfaced a caveat that changes its interpretation: **it measures earnings on completed freelance jobs, not learning demand.** It is a proxy, and a lagging one.

**Competitor course pages read directly** rather than searched. This overturned the rev A recommendation. A large enterprise vendor already offers a free four-hour course covering substantially what rev A proposed building, with 8,319 enrollments and a 4.7 rating. Its gap score fell from 9 to 3.

### Stage 5 — Syllabus coverage matrix

Module-level outlines extracted from six offerings across three provider types — enterprise vendor courses, a university executive program, and a university-partnered certificate — then compared for what every provider covers versus what none do.

Every syllabus examined covers: what GenAI is, prompting, use-case identification, risk and governance, feasibility. **None cover** measuring whether the implementation saved time, recovering from a failed first attempt, sustaining use past the novelty period, or handing a workflow to a colleague.

Every syllabus in this market ends at the moment of first successful output.

That structural absence, triangulated against a documented abandonment pattern in learner reviews and adoption research, produced the current recommendation: a mini course on **post-adoption durability**. Full working in [`competitive-analysis-2026-07.md`](competitive-analysis-2026-07.md).

---

## 3. The scoring model

```
                 (D × w_D) + (P × w_P) + (G × w_G) + (B × w_B)
    score  =    ─────────────────────────────────────────────
                        w_D + w_P + w_G + w_B
```

Dividing by the weight total means weights need not sum to 100 — the dashboard sliders stay valid at any total.

**Default weights:** demand 30, willingness to pay 25, underserved gap 25, buildability 20.

### Anchoring rubric

Sub-scores are assigned against these anchors. Publishing the rubric is what makes the numbers auditable rather than arbitrary.

| Score | Demand | Willingness to pay | Underserved gap | Buildability |
|---|---|---|---|---|
| 9–10 | Triple-digit YoY growth in 2+ independent sources, or ranked #1 | Compliance-driven, or a direct revenue path for the buyer | Demand documented and supply verifiably absent from competitor syllabi | No tooling or vendor dependency; content ages well |
| 7–8 | Strong growth cited across multiple sources | Clear business ROI | Supply exists but is mistargeted by audience, price, or vendor | Some production needed; moderate tool-churn risk |
| 5–6 | Steady, not accelerating | Career benefit, indirect payoff | Adequately served | Heavy production, or fast tool churn |
| 1–4 | Flat or declining | Hobby or personal interest | Explicitly oversaturated, or a direct incumbent exists | Will not fit the build window |

### Worked example

Topic: *The Third Week* — demand 7, WTP 7, gap 10, buildability 10.

```
(7 × 30) + (7 × 25) + (10 × 25) + (10 × 20)   =   210 + 175 + 250 + 200   =   835
835 ÷ 100  =  8.35
```

### Source tiers

Every claim carries a tier tag:

- **`[A]` Primary** — the organization's own report or a course page read directly. Coursera JSR 2026, Upwork In-Demand Skills 2026, and provider course pages read directly.
- **`[B]` Secondary** — trade press, law firms, research summaries. Forbes, APA Monitor, Travers Smith.
- **`[C]` Weak** — SEO content marketing, methodology unstated, some plausibly AI-generated aggregations.

Tier `[C]` claims are not excluded, because some are the only available evidence on a question. They are flagged so you can see when a conclusion rests on thin ground.

---

## 4. Known limitations

**The sub-scores are judgments.** There is no measurement instrument, no coding scheme, no second rater. A different analyst applying the same rubric to the same evidence would produce different numbers. This is unvalidated single-rater rubric scoring, and it should be read as such.

**Precision is false.** The spread across the top four topics is narrower than the scoring error. Treat the output as tiers — "these four are worth testing, these two aren't" — rather than as a ranked list.

**Demand is the best-evidenced column; buildability is the worst.** Demand maps to real published growth figures. Buildability is a judgment about *your* production capacity, tooling, and comfort with video, made without knowing any of them — and it carries 20% of the weight. **Re-score that column yourself.**

**Absence of supply is not proof of demand.** The coverage matrix reliably shows that no competitor teaches durability. It cannot show whether that is because nobody wants it. This is the central risk on the current top recommendation and it is flagged on the dashboard card.

**Enrollment differentials are confounded.** The vendor funnel figure (50,663 introduction versus 8,319 use-case) is cited as suggestive of drop-off, but the courses launched at different times and enrollment is cumulative. Some of that spread is age, not attrition.

**Coursera's data is enterprise-weighted.** Six million *enterprise* learners reached through institutional customers. That population is corporate L&D, not small business owners — a different buyer from this dashboard's target. Directionally useful, not directly transferable.

---

## 5. Monthly refresh procedure

Reproduce these steps, or ask Claude to run them.

1. **Re-fetch the primary reports.** Coursera and Upwork publish annually; check for a new edition. Between editions, look for quarterly updates.
2. **Re-read the top three competitor course pages.** Record enrollment counts, ratings, price, and length. Enrollment deltas across a month are the closest thing to a real demand signal available for free.
3. **Re-run the syllabus matrix** for any competitor that has changed its outline. New modules appearing in incumbent courses are the earliest warning that a gap is closing.
4. **Search for new entrants** in the gap you're targeting. If someone has shipped it, the gap score drops immediately.
5. **Re-score, but do not re-weight without a reason.** Changing weights between cycles makes month-over-month comparison meaningless. If you change them, note it in `CHANGELOG.md`.
6. **Update `data/topics.json`,** bump `meta.cycle` and `meta.generated`, and commit.
7. **Record what changed and why** in `CHANGELOG.md`. The reasoning trail is worth more over time than any single month's ranking.

### The step this dashboard does not perform

Scoring identifies what to test. It does not test anything.

Before building any course on this list: publish a landing page with the real price and a real buy or waitlist button, drive modest traffic, and measure conversion. If the page doesn't convert, the finding costs a weekend instead of a month.

A high score on this dashboard justifies a landing page. Nothing more.

# Changelog

Every cycle records what changed and, more importantly, *why*. The reasoning trail is worth more over time than any single month's ranking.

---

## 2026-07 rev B — 27 July 2026

Triggered by a methodology challenge: the rev A scores were presented with more apparent rigor than the underlying evidence supported.

### Changed

- **Primary reports fetched in full**, replacing search-result summaries. Coursera *Job Skills Report 2026* and Upwork *In-Demand Skills 2026*, both including their methodology sections.
- **Competitor course pages read directly.** Two enterprise vendor courses, a university executive program, and a university-partnered certificate. Enrollment counts, ratings, prices, and module outlines recorded as measured values.
- **Syllabus coverage matrix built** — the first time gap scores rested on measurement rather than inference.
- **Source tiers added** to every claim: `[A]` primary, `[B]` secondary, `[C]` weak.

### Score revisions

| Topic | Gap: rev A → rev B | Reason |
|---|---|---|
| Find Your AI Use Case | 9 → **3** | A free vendor course covers this ground (8,319 enrolled, 4.7). Direct incumbent |
| Verifying AI Output | 8 → **9** | The leading course devotes one 7-minute video to this. Confirmed thin across the whole market |
| Workflow automation | 6 → 6 | Unchanged, now measured rather than assumed |
| AI video marketing | 5 → **4** | Confirmed crowded; fastest-decaying content of any candidate |

### Added

- **New #2: *The Third Week: Making AI Stick After the Novelty Wears Off*** (gap 10, buildability 10). Derived from the coverage matrix: every provider examined ends at first successful output, and none address measurement, failure recovery, durability, or handoff.

### Corrections to rev A

- **The rev A top recommendation was wrong.** Use-case discovery was scored as underserved on the reasoning that the market teaches tools rather than diagnosis. Reading the incumbent's actual syllabus disproved this. No amount of additional searching would have caught it — only reading the competitor's own page did.
- **Upwork data reinterpreted.** Its methodology measures freelancer *earnings on completed jobs*, not learning demand. It is a lagging proxy, now labeled as such on the dashboard.
- **Coursera data scope narrowed.** Six million *enterprise* learners via institutional customers — corporate L&D, not the small business owners this dashboard targets. Directionally useful, not directly transferable.

### Still outstanding

- Two further self-paced marketplaces remain unchecked.
- One cohort-course marketplace checked only briefly; appears adjacent but not overlapping, on weak evidence.
- The "B2B commands 2–3x B2C" claim remains `[C]` and single-sourced, and is load-bearing for the entire pricing strategy. Priority to verify or replace next cycle.

---

## 2026-07 rev A — 27 July 2026

Initial build.

- Audience fixed: small business owners primary, working professionals secondary.
- Fifteen web searches across marketplaces, skills reports, freelance data, SMB adoption surveys, and saturation commentary.
- Four-factor weighted scoring model established (demand 30, WTP 25, gap 25, buildability 20) with a published anchoring rubric.
- Five topics shortlisted, four on the watchlist.
- Dashboard built with re-weightable sliders and a JSON data layer.

**Known weakness at time of publication, corrected in rev B:** gap and buildability scores — 45% of total weight — had no measurement behind them. No competing courses had been counted.

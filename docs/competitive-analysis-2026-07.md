# Competitive analysis: AI-for-business learning market

**Cycle 2026-07 · Prepared 27 July 2026**

Source tiers used throughout:
**[A]** primary — the organisation's own report, or a course page read directly
**[B]** secondary — trade press, law firms, analyst summaries
**[C]** weak — SEO content marketing, methodology unstated

---

## 1. What changed from the first pass

The first dashboard scored "Find Your AI Use Case" as the #1 underserved topic, on the reasoning that everyone teaches tools and nobody teaches diagnosis.

**That was wrong, and reading the actual course pages is what showed it.** IBM ships `GenAI for Execs & Business Leaders: Formulate Your Use Case` on Coursera — a 4-hour course whose stated outcomes are, almost verbatim, what I proposed building. It has 8,319 enrolments and a 4.7 rating. [A]

The gap is real but sits one step later in the learner's journey than I placed it. Details in section 4.

---

## 2. Measured competitor inventory

Every figure below was read directly off the provider's own page on 27 July 2026. [A]

| Provider | Offering | Length | Level | Price | Enrolled | Rating |
|---|---|---|---|---|---|---|
| IBM / Coursera | GenAI for Execs: An Introduction | 3 h, 2 modules | Beginner | Free / Coursera Plus | 50,663 | 4.6 (536) |
| IBM / Coursera | GenAI for Execs: Formulate Your Use Case | 4 h, 2 modules | Intermediate | Free / Coursera Plus | 8,319 | 4.7 (139) |
| IBM / Coursera | GenAI for Execs: Integration Strategy | not read | — | Free / Coursera Plus | — | — |
| CMU Tepper | Transformational AI & Business Strategy | 2 days, in person (Pittsburgh, 4–5 Nov 2026) | Directors / senior managers | **$4,500** | — | — |
| CMU Tepper + SCS | AI for Business | Asynchronous | Non-technical, no coding | not published | — | — |
| MIT Schwarzman / Emeritus | AI & Automation for the Enterprise | 6 weeks, 4 modules | 5–10 yrs experience, degree required | not published | — | — |
| Udemy | Wide catalogue, no single dominant title | Varies | Varies | $15–$150 typical | — | Platform-level 1.8/5 Trustpilot [C] |

**The market is barbelled.** Free-to-cheap self-paced content at one end (IBM, Udemy), $4,500 in-person executive education at the other (CMU). There is very little in between, and nothing at all addressed to a business with fewer than 50 employees.

### Segment mismatch worth naming

CMU's programme targets "directors, senior managers, and leaders tasked with implementation of AI strategy across the organization" [A]. Emeritus requires a bachelor's degree and 5–10 years' experience [C]. IBM's course is written for "CXOs or line of business leaders" and requires two prior courses [A].

**None of these are built for the owner of a 12-person company.** That person has no AI strategy team, no data infrastructure to audit, and no budget for a two-day trip to Pittsburgh.

---

## 3. Syllabus coverage matrix

Module-level outlines extracted from IBM's two courses [A], CMU's published takeaways [A], and Emeritus/MIT's described modules [C].

| Topic | IBM intro | IBM use case | CMU | Emeritus | Verdict |
|---|---|---|---|---|---|
| What GenAI is, history, capabilities | ✅ | — | ✅ | ✅ | Saturated |
| Writing effective prompts | — | ✅ | — | — | Saturated market-wide |
| Identifying a use case | ✅ (light) | ✅ (core) | ✅ | ✅ | **Covered — was my #1 pick** |
| Risk, ethics, governance | ✅ | ✅ | ✅ | ✅ | Saturated |
| Feasibility assessment | — | ✅ | ✅ | — | Covered |
| Evaluating AI output | — | ✅ (7-min video) | — | — | Thin |
| Case studies of failure | — | ✅ (2 readings) | — | — | Thin |
| Data readiness | — | — | ✅ | ✅ | Enterprise-only |
| Change management / upskilling teams | — | — | ✅ | ✅ | Enterprise-only |
| **Measuring whether it actually saved time** | — | — | — | — | **Absent everywhere** |
| **What to do when the first attempt fails** | — | — | — | — | **Absent everywhere** |
| **Sustaining use past the novelty period** | — | — | — | — | **Absent everywhere** |
| **Handing a workflow to someone else** | — | — | — | — | **Absent everywhere** |

Every syllabus in this market ends at the moment of first successful output. Not one of them covers what happens in week three.

---

## 4. The gap: adoption doesn't survive contact with the calendar

Four independent signals converge on the same failure mode.

**Learners abandon between formulation and implementation.** IBM's specialisation shows 50,663 enrolments in course 1 and 8,319 in the use-case course [A]. *Caveat: this is an inference, not proof — the courses launched at different times and enrolment is cumulative, so some of that spread is age, not attrition. It is suggestive, not conclusive.*

**The complaint pattern in reviews is about implementation, not information.** Recurring phrasing in Coursera reviews includes "just an AI pep rally," "no simple demonstrations of how to implement the various tasks discussed," "too generic," and "could easily be found on YouTube" [B].

**The abandonment mechanism is documented.** People quit AI tools "because using them feels like managing another job" — jumping between tools, copy-pasting between apps, learning that feels like more work than the work [C]. The pattern is trying it once or twice, getting mediocre output, then either quitting or settling into low-value usage [C].

**The adoption statistics show the same shape.** Only 8% of businesses reach advanced AI adoption; the majority stay in early or experimental stages with one or two use cases and no broader strategy [C].

### What this means

The market has thoroughly solved *inspiration* and *initiation*. It has not touched *durability*. The learner's real question at week three is not "what could AI do for me" — they already know — it is **"why did the thing I set up stop being useful, and how do I tell if it was ever working?"**

That question has no course.

### Why this gap exists — and the risk it carries

Be clear-eyed: this gap is partly a gap because it is hard to sell. Nobody searches for "AI adoption durability." There is no keyword volume, no job title, no certification.

**The mitigation is to sell the symptom, not the category.** The buyer does not know they want a durability framework. They do know that they paid for ChatGPT Plus in February, used it enthusiastically for two weeks, and haven't opened it since. That is the hook.

This also means demand cannot be validated by search volume. It has to be validated by a landing page and a price.

---

## 5. Proposed mini course

**Working title:** *The Third Week: Making AI Stick After the Novelty Wears Off*

**Format:** 12 lessons, 5–8 minutes each. Roughly 75 minutes total. Self-paced.

**Learner:** Owner or operator of a business with 2–50 people who has already tried AI, got some value, and watched it fade.

**Positioning against the market:** IBM and CMU sell you the beginning. This is the only thing on the market that sells you the middle.

### Lesson map

*Part 1 — Diagnose the fade (lessons 1–4)*
1. The three ways AI use dies: novelty decay, quality drift, context loss
2. Audit: what did you actually stop using, and at what point
3. Distinguishing a bad use case from a bad implementation
4. The switching-cost trap — when the tool costs more attention than it saves

*Part 2 — Measure honestly (lessons 5–8)*
5. Establishing a before-time for a task you already do
6. The 5-minute time audit that survives contact with a real week
7. Quality floor: defining "good enough to ship" before you generate
8. When to kill a workflow — a decision rule, not a feeling

*Part 3 — Build durability (lessons 9–12)*
9. Anchoring AI to an existing trigger instead of a new habit
10. Writing the instruction down once so you stop re-deriving it
11. Handing a workflow to someone else without losing the quality
12. The monthly 20-minute review that keeps the whole thing alive

### Deliverable the learner walks away with

A completed one-page workflow card for one real task: trigger, instruction, quality floor, time saved, review date. This is the artifact that makes it feel like a product rather than a lecture.

### Buildability

No software dependency, no vendor lock-in, no screen recordings that expire when a UI changes. Framework, worksheets, and short talking-head or slide video. This is the single most durable asset of any candidate examined — it will not need re-recording when the next model ships.

### Pricing

Given the buyer is an owner with budget authority and the framing is operational rather than aspirational, $99–$149 is defensible for the self-paced version. Do not launch above that until the landing page has converted at all.

---

## 6. Recommended validation before you build

The analysis above justifies building a landing page. It does not justify building the course.

1. Write the sales page first, with the symptom as the headline and a real price.
2. Drive a small amount of traffic — your ID network, one or two SMB communities.
3. Look for pre-orders or waitlist-with-email-and-price-shown, not clicks.
4. Only build lessons 1–4 first. If those land, build the rest.

If the page does not convert, the finding is cheap and you have lost a weekend rather than a month.

---

## 7. Confidence and what would change my mind

**What I am reasonably confident about:** the coverage matrix. I read those syllabi directly, and the absence of durability content across all four providers is not ambiguous. [A]

**What is inferential:** that the absence represents unmet demand rather than absent demand. Course markets sometimes omit a topic because nobody wants it. The abandonment evidence [B/C] makes me think the need is real, but need and willingness to pay are different things.

**What would change my mind:** a landing page that doesn't convert. That is the only test that matters, and it is cheaper than any further research I could do.

**Cohort market, checked briefly:** Maven hosts live cohort courses on AI automation for business leaders and operations managers, and on building AI agents [C]. These are adjacent but still initiation-shaped — they teach building, not sustaining. No durability-focused offering surfaced. Treat this as weak evidence: a search that finds nothing is not the same as nothing existing, and Maven's catalogue is not fully indexed.

**Still unchecked:** LinkedIn Learning and Skillshare catalogues directly. Worth 30 minutes before you commit build time.

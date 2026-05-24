---
name: assumption-map
description: >-
  Maps riskiest assumptions on importance vs evidence, prioritizes falsification
  tests, and maintains an assumption ledger for software idea validation. Use when
  asking what to test first, assumption mapping, riskiest assumption, or pretotyping
  priorities.
disable-model-invocation: true
---

# Assumption Map

Surface what must be true for the idea to work. Link each assumption to one experiment in `validation-experiments`.

## Workflow

1. **Brain-dump assumptions** — problem exists, buyers pay, channel works, we can build, timing, regulation, etc.
2. **Score each** on **importance** (1–5) and **evidence** (1–5, from `idea-scorecard` hierarchy).
3. **Plot** mentally: prioritize **high importance + low evidence**.
4. **Pick top 3–5** to test this sprint.
5. **Assign** cheapest falsifying test per row.
6. **Update ledger** after each experiment.

## 2×2 guidance

|                     | Low evidence | High evidence  |
| ------------------- | ------------ | -------------- |
| **High importance** | **Test now** | Monitor        |
| **Low importance**  | Defer        | Ignore for now |

## Assumption ledger

| ID  | Assumption | Importance | Evidence tier | Test method | Success | Fail (kill) | Status |
| --- | ---------- | ---------- | ------------- | ----------- | ------- | ----------- | ------ |
| A1  |            |            |               |             |         |             | open   |

**Status:** open | testing | validated | killed

## Test method hints

| Assumption type    | Often use                       |
| ------------------ | ------------------------------- |
| Problem exists     | `problem-discovery` interviews  |
| Willingness to pay | Priced fake door / pre-sale     |
| Market size        | `market-sizing` + desk research |
| Can reach buyer    | Smoke test + paid traffic       |
| Solution workflow  | Concierge or Wizard of Oz       |
| Founder can win    | `feasibility-gate`              |

## Kill rule

If a **high-importance** assumption hits its **fail** threshold, stop or pivot — update `idea-scorecard` and `discovery/INDEX.md` decision.

## Output

Save to `discovery/<topic-slug>/research/YYYY-MM-DD-<topic-slug>-assumptions.md`.

Copy open rows into `idea-scorecard` assumption ledger before scoring.

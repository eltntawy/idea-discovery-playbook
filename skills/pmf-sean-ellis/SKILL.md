---
name: pmf-sean-ellis
description: >-
  Measures product-market fit after a prototype using the Sean Ellis survey,
  retention context, and directional benchmarks. Use for product-market fit,
  PMF test, Sean Ellis, or very disappointed survey—not for pre-build idea validation.
disable-model-invocation: true
---

# PMF — Sean Ellis Test

**Product validation only** — run after users have **experienced** the core value (prototype or v1). Not a substitute for `problem-discovery` or `validation-experiments` before build.

Prerequisite: scorecard **Strong go** or **Conditional go** with product shipped to a cohort.

## Survey core

Ask active users (used core value in last 2 weeks):

> How would you feel if you could no longer use [product]?
>
> - Very disappointed
> - Somewhat disappointed
> - Not disappointed

## PMF threshold

- **≥ 40%** "Very disappointed" among **target** users → directional PMF signal (segment-specific).
- **&lt; 40%** → improve segment or value before scaling acquisition.

## Context metrics (same memo)

| Metric     | Notes                                                    |
| ---------- | -------------------------------------------------------- |
| Activation | % reaching core value in 7 days                          |
| Retention  | D7 / D30 or logo retention at 12 months                  |
| NPS        | Directional; B2B often &gt;30, B2C &gt;50 as comparables |

Treat benchmarks as segment-dependent — cite your cohort only.

## Workflow

1. Define **target user** for the survey (not all signups).
2. Sample **40+** responses minimum for stability when possible.
3. Segment results (role, use case, plan).
4. Follow with 5–10 interviews on *why* very disappointed users answered that way.
5. Record **Decision:** scale acquisition, improve product, or narrow segment.

## Output

Save to `discovery/<topic-slug>/research/YYYY-MM-DD-<slug>-pmf.md`.

Update `idea-scorecard` Solution stage and `discovery-synthesis` if compiling a pack.

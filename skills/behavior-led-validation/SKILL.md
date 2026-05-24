---
name: behavior-led-validation
description: >-
  Runs behavior-led idea and market validation with problem interviews, pre-sales
  smoke tests, paid traffic experiments, search and forum demand signals, competitor
  revenue estimation, unit economics, and 2026 benchmarks. Use when validating a
  business idea, testing willingness to pay, measuring demand, estimating competitor
  MRR or ARR, or choosing validation experiments before build.
disable-model-invocation: true
---

# Behavior-Led Validation

## Principle

Validate with **observed behavior and payment**, not opinions. Treat compliments, likes, and hypothetical interest as weak evidence. Strongest signal: customers pay at the target price before software exists.

Keep validation types in order: **idea validation** (worth deeper research) → **market validation** (demand, reach, economics) → **product validation** (solution fit after a prototype). Do not treat landing pages, ad tests, or concierge delivery as product validation.

## When to use

Use this skill for an end-to-end validation plan or execution memo. For depth on one slice, also read:

- `problem-discovery` — Mom Test interviews, ICP, pain scoring
- `validation-experiments` — experiment loop, thresholds, artifact template
- `market-sizing` — bottom-up TAM, SAM, SOM
- `competitor-landscape` — competitor matrix and positioning
- `revenue-model` — pricing scenarios and LTV:CAC math
- `market-research` — live web gap and current-market analysis

Respect the workspace **no-build boundary**: no production app scaffold until a scorecard records **Strong go** or **Conditional go**.

Read `discovery/INDEX.md` and only the active research folder at `discovery/<topic-slug>/` before extending work. **Do not** list, open, search, or summarize `discovery/archive/` unless the user explicitly requests archived research.

## Phase 1 — Idea and market demand

### 1. Problem interviews (qualitative)

| Item | Guidance |
| --- | --- |
| Target | 15–20 potential customers in the ICP |
| Core questions | "How do you solve this problem today?" and "What's the hardest part about that?" |
| Look for | Recurring complaints about current, inferior solutions; workarounds; time or money already spent |
| Weak signal | Idea praise, future intent, or friend feedback without behavior |

Save interview evidence in `discovery/<topic-slug>/briefs/` or `discovery/<topic-slug>/research/`. Follow `problem-discovery` for scripts and kill criteria.

### 2. Willingness to pay (pre-sale / smoke test)

| Item | Guidance |
| --- | --- |
| Surface | One-page landing (Carrd, Webflow, or equivalent) with clear offer and pricing table |
| Offer | Early access, beta pricing, or pre-order via Stripe payment link **before** building product |
| Validated when | Visitor completes payment or leaves card details for the stated offer |
| Not validated | Email-only signup, waitlist without commitment, or unpriced interest |

Design thresholds with `validation-experiments`. Save plans and results under `discovery/<topic-slug>/experiments/`.

### 3. Low-cost paid traffic (quantitative)

| Item | Guidance |
| --- | --- |
| Channels | Meta Ads or Google Ads |
| Budget | Roughly $100–$500 to the landing or pre-sale page |
| Metrics | CTR to the page; conversion to signup or pre-sale |
| Interpretation | Use as a demand proxy with audience and offer quality noted; pair with interviews or payment evidence |

### 4. Existing demand signals (desk research)

| Source | What to capture |
| --- | --- |
| Keywords | SEMrush or Ahrefs — search volume and CPC for problem and solution terms |
| Communities | Reddit, Discord, niche forums — threads asking for solutions or comparing tools |
| Rule | High volume or CPC supports **research priority**, not proof of payment |

Cross-check with `market-sizing`; label search and forum signals as proxies.

## Phase 2 — Revenue, costs, and MRR

### 1. Competitor revenue estimation

| Method | How |
| --- | --- |
| Headcount heuristic | LinkedIn employee count × **$150k–$200k** per employee → rough ARR band (label as assumption) |
| Mobile | AppMagic, SensorTower — downloads and revenue estimates where applicable |
| Aggregators | BigIdeasDB and similar — reported revenue for comparable startups |

Record sources, formulas, and sensitivity in `discovery/<topic-slug>/research/`. Never present estimates as audited financials.

### 2. Costs and unit economics

| Area | Guidance |
| --- | --- |
| Benchmarks | IdeaProof or manual worksheets — MRR, ARR, churn, LTV, CAC |
| Target | **CAC < LTV ÷ 3** (equivalently LTV:CAC ≥ 3:1) unless the memo documents why a different bar applies |
| Ad longevity | Meta Ad Library — long-running competitor ads as a weak profitability signal, not proof |

Use `revenue-model` for scenario tables and payback.

### 3. Key metrics (2026 reference bands)

| Metric | Reference band |
| --- | --- |
| MRR / ARR | Seed-stage narratives often cite **$10k–$50k MRR** with **~15–20% MoM** growth where evidenced |
| Retention | B2B SaaS often targets **~70–80%** logo or revenue retention at 12 months |
| NPS | **> 30** B2B; **> 50** B2C as directional quality bars |

Treat bands as comparables for analysis, not pass/fail gates without segment context.

## Tool map

| Job | Examples |
| --- | --- |
| Validation / metrics | IdeaProof |
| Traffic / keywords | SEMrush, Ahrefs |
| Landing + pre-sale | Carrd (or Webflow) + Stripe |
| Mobile metrics | AppMagic, SensorTower |
| Startup revenue data | BigIdeasDB |
| Competitor ads | Meta Ad Library |

Prefer the smallest toolset that answers the current assumption; cite what was actually checked.

## Strongest validation path

When feasible, run a **concierge MVP**: deliver the outcome manually for a small paid cohort before automating in software. Pair with pre-sales or design-partner commitments where appropriate.

## Evidence ladder (workspace)

| Level | Examples | Weight |
| --- | --- | --- |
| L0–L1 | Views, likes, compliments | Context only |
| L2 | Waitlist, detailed signup | Supporting |
| L3 | Repeat use, workflow adoption | Strong supporting |
| L4 | Deposit, LOI, prepay, pilot | Strong |
| L5 | Recurring payment at target price | Strongest |

Strong go still requires the workspace scorecard bar (see `idea-scorecard` and `discovery/SYSTEM-RESEARCH.md`).

## Output checklist

- [ ] State riskiest assumption and validation phase (idea / market / product)
- [ ] List methods run or planned with success and kill thresholds
- [ ] Separate **facts**, **assumptions**, and **evidence** with sources
- [ ] Label revenue and competitor estimates with formulas and ranges
- [ ] Record **Decision** and **Next experiment**
- [ ] Save artifacts under `discovery/<topic-slug>/` (`briefs/`, `research/`, or `experiments/`) with dated filenames; update `discovery/INDEX.md` when opening or archiving a topic

Default memo sections: **Facts**, **Assumptions**, **Evidence**, **Analysis**, **Decision**, **Next experiment**.

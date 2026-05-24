---
name: behavior-led-validation
description: >-
  Orchestrates behavior-led idea and market validation—problem interviews, pretotype
  experiments, paid traffic, demand proxies, competitor revenue estimates, and unit
  economics—before build. Use when validating a business idea end-to-end, testing
  willingness to pay, or planning experiments before build.
disable-model-invocation: true
---

# Behavior-Led Validation

**Orchestrator skill.** For depth on one step, invoke the child skill listed below. For stage gates and artifact order, start with `discovery-playbook`.

## Principle

Validate with **observed behavior and payment**, not opinions. Strongest signal: customers pay at the target price before software exists.

Validation order: **idea validation** → **market validation** → **product validation** (after a prototype). Landing pages, ad tests, and concierge delivery are not product validation.

## Workspace rules

- **No-build boundary:** no production app scaffold until `idea-scorecard` records **Strong go** or **Conditional go**.
- Read `discovery/INDEX.md` and only `discovery/<topic-slug>/` before extending work. Create `discovery/INDEX.md` if missing.
- **Do not** open `discovery/archive/` unless the user explicitly asks.

## Phase map

| Phase                    | Goal                            | Primary skills                                                                                   |
| ------------------------ | ------------------------------- | ------------------------------------------------------------------------------------------------ |
| Idea                     | Problem is real and painful     | `assumption-map`, `problem-discovery`, `regulatory-risk-scan` (if regulated), `feasibility-gate` |
| Market                   | Demand, wedge, economics        | `market-research`, `competitor-landscape`, `market-sizing`, `positioning-wedge`, `revenue-model` |
| Demand test              | Falsify riskiest assumptions    | `validation-experiments`                                                                         |
| Decision                 | Go / conditional / pivot / kill | `idea-scorecard`, `discovery-synthesis`                                                          |
| Product (post-prototype) | Solution fit                    | `pmf-sean-ellis`                                                                                 |

## Phase 1 — Idea and market demand (summary)

1. **Problem interviews** — follow `problem-discovery` (15–20 ICP, Mom Test ladder, commitments). Optional switching depth → `jtbd-interviews`.
2. **Willingness to pay** — priced landing + Stripe or equivalent; thresholds in `validation-experiments`. Not validated: email-only waitlist.
3. **Paid traffic** — ~$100–$500; track CTR and conversion; compute **ILI** when applicable (see `validation-experiments`).
4. **Desk demand** — keywords and forums as **research priority** proxies only; pair with payment or interviews.

Save under `discovery/<topic-slug>/briefs/`, `research/`, or `experiments/`.

## Phase 2 — Revenue and costs (summary)

- Competitor revenue: headcount heuristic, mobile estimates, aggregators — label all as assumptions.
- Unit economics: **LTV:CAC ≥ 3:1** for strong go; **&lt; 2:1** kill — see `revenue-model` bands.
- Reference metric bands (directional, verify for segment): seed MRR narratives, B2B retention, NPS — not pass/fail without context.

Full scenarios → `revenue-model`.

## Evidence mapping

Use the **canonical hierarchy** in `idea-scorecard` (levels 1–5). Quick reference:

| Label                                | Maps to level |
| ------------------------------------ | ------------- |
| L0–L1 views, likes, compliments      | 1–2           |
| L2 waitlist / signup                 | 3             |
| L3 repeat use, design-partner time   | 4             |
| L4 deposit, LOI, pilot               | 5             |
| L5 recurring payment at target price | 5             |

**Strong go** still requires the weighted scorecard bar in `idea-scorecard`.

## Strongest path

When feasible: **concierge MVP** for a small paid cohort, then automate. Sequence with fake door → concierge per `validation-experiments`.

## Regulated ideas

If health, fintech, legal, or similar constraints apply → `regulatory-risk-scan` before scaling tests.

## Output checklist

- [ ] State validation phase and riskiest assumption
- [ ] List child skills invoked or planned
- [ ] Facts / Assumptions / Evidence / Analysis / Decision / Next experiment
- [ ] Update `discovery/INDEX.md` when opening or archiving a topic

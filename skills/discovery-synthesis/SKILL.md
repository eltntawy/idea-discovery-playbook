---
name: discovery-synthesis
description: >-
  Compiles discovery artifacts into one researcher or stakeholder pack—executive
  summary, evidence table, open assumptions, economics, decision, and next tests.
  Use when summarizing validation, writing a discovery report, or packaging idea
  research for review.
disable-model-invocation: true
---

# Discovery Synthesis

Merge existing work under `discovery/<topic-slug>/` into **one readable pack**. Do not invent evidence — cite artifacts and URLs.

## Inputs (read in order)

1. `discovery/INDEX.md` and `TOPIC.md`
2. Latest `briefs/`, `research/`, `experiments/`, `scorecards/`
3. `assumption-map` ledger if present

## Workflow

1. **Executive summary** — hypothesis, decision, one-line why (3–5 sentences).
2. **Evidence table** — claim | source artifact | tier (1–5) | confidence.
3. **Problem and ICP** — from briefs / problem-discovery.
4. **Market and competition** — wedge, key competitors, gap (from market + competitor memos).
5. **Economics** — TAM/SAM/SOM sketch, LTV:CAC band, pricing logic.
6. **Experiments run** — method, thresholds, result, ILI if any.
7. **Assumption ledger** — open vs validated vs killed.
8. **Scorecard snapshot** — total and decision if scored.
9. **Risks and regulatory** — include `regulatory-risk-scan` if run.
10. **Next 3 actions** — single owner and date if known.

## Quality bar

- Separate **facts**, **assumptions**, and **interpretation**.
- Flag weakest evidence (tier 1–2) driving the decision.
- State what was **not** tested.

## Output

Save to `discovery/<topic-slug>/YYYY-MM-DD-<slug>-synthesis.md` using [SYNTHESIS-TEMPLATE.md](SYNTHESIS-TEMPLATE.md).

Offer to update `TOPIC.md` **Current decision** and **Next experiment** one-liners.

---
name: feasibility-gate
description: >-
  Assesses build feasibility for software ideas—solo or small-team v1 scope,
  build-for-self vs build-for-market, motivation, and Build Wait Reject verdict.
  Use when asking can I build this, feasibility, scope lock, or build wait reject.
disable-model-invocation: true
---

# Feasibility Gate

Run after problem signal exists and before **Strong go** on build. Prevents committing months to ideas you cannot ship or do not want to sell.

## Checklist

- [ ] **Build-for-self vs market** — is demand from you alone or from ICP?
- [ ] **v1 scope** — list max 3 outcomes for first release; cut everything else
- [ ] **Solo + AI constraint** — can v1 ship in **4 weeks** part-time at stated skill stack?
- [ ] **Dependencies** — APIs, data, legal, payments, integrations that block v1?
- [ ] **Distribution** — one realistic channel you can access in 90 days
- [ ] **Motivation** — still excited after kill-criteria review?

## Scoring (1–5 each)

| Dimension    | Question                                        |
| ------------ | ----------------------------------------------- |
| Technical    | Can you implement core workflow?                |
| Scope        | Is v1 bounded?                                  |
| Distribution | Can you reach 100 ICP prospects?                |
| Economics    | Rough LTV:CAC plausible (see `revenue-model`)?  |
| Personal fit | Do you want to serve this segment for 2+ years? |

## Verdict

| Verdict    | Meaning                                                 |
| ---------- | ------------------------------------------------------- |
| **Build**  | Proceed to demand tests or implementation per scorecard |
| **Wait**   | Need more learning; name what unlocks Build             |
| **Reject** | Do not build; archive topic in `discovery/INDEX.md`     |

Record verdict in `idea-scorecard` — **Reject** or **Wait** blocks Strong go.

## Scope lock

If **Build**, write:

- **In v1:** …
- **Out of v1:** …
- **Deadline:** YYYY-MM-DD for v1 or next experiment

## Output

Save to `discovery/<topic-slug>/research/YYYY-MM-DD-<topic-slug>-feasibility.md`.

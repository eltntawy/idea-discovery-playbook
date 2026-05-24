---
name: idea-scorecard
description: Scores software ideas across validation stages using an evidence hierarchy and weighted go, conditional go, pivot, or kill thresholds. Use when the user asks to score an idea, make a go/no-go decision, or validate before build.
disable-model-invocation: true
---

# Idea Scorecard

## Evidence hierarchy

Weakest to strongest:

1. Awareness - views
2. Interest - opinions and compliments
3. Intent - signups, meetings, waitlists with context
4. Behavior - active use, repeated actions, design-partner time
5. Revenue - payment, deposits, LOIs, pre-orders

## Weighted scorecard

| Stage | Score 1-10 | Weight | Weighted | Evidence summary |
| --- | --- | --- | --- | --- |
| Problem |  | 1.5 |  |  |
| Solution |  | 1.5 |  |  |
| Market |  | 1.0 |  |  |
| Channel |  | 1.0 |  |  |
| Revenue |  | 1.5 |  |  |
| Scale |  | 0.5 |  |  |
| **Total** |  |  | **/70** |  |

## Decision thresholds

- 56-70: Strong go
- 42-55: Conditional go - close named gaps first
- 28-41: Pivot
- 0-27: Kill or restart

## Kill cues

- Problem confirmed by fewer than half of relevant interviews
- No paying customers after four weeks of revenue testing
- LTV:CAC below 2:1 in the base case
- All acquisition channels exceed target CAC

## Output

Save to `discovery/<topic-slug>/scorecards/YYYY-MM-DD-<topic-slug>-scorecard.md` using [TEMPLATE.md](TEMPLATE.md).

Do not recommend implementation unless the decision is Strong go or Conditional go with explicit remaining gaps.

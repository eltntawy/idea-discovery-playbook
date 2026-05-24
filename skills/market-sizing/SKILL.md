---
name: market-sizing
description: Builds bottom-up TAM, SAM, and SOM estimates with top-down cross-checks and search-demand proxies for software ideas. Use when the user asks about market size, TAM, SAM, SOM, addressable market, or search demand.
disable-model-invocation: true
---

# Market Sizing

## Checklist

- [ ] Define the buyer or user segment precisely
- [ ] Estimate segment count from credible sources
- [ ] Estimate adoption rate and price
- [ ] Compute bottom-up revenue
- [ ] Cross-check with top-down or search-demand proxies
- [ ] Record kill criteria for markets that are too small

## Bottom-up worksheet

| Input | Value | Source | Assumption |
| --- | --- | --- | --- |
| Segment count |  |  |  |
| Adoption rate |  |  |  |
| Price per year |  |  |  |
| Addressable revenue |  |  |  |

Formula: `segment_count x adoption_rate x price`.

## Thresholds

- Treat search volume as a proxy, not proof.
- Flag when addressable users or revenue look too small for the stated goal.
- Separate TAM, SAM, and SOM explicitly.

## Output

Save research to `discovery/<topic-slug>/research/YYYY-MM-DD-<topic-slug>-market.md` and reference it from the idea brief in the same topic folder.

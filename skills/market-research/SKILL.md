---
name: market-research
description: >-
  Researches the current market for a software or digital business idea using
  web search and credible public sources, maps competitors and substitutes,
  identifies gaps, and writes a cited gap-and-fit memo. Use when the user asks
  for market research, gap analysis, competitive landscape, demand signals, or
  whether an idea fits today's market.
disable-model-invocation: true
---

# Market research

## Goal

Find **what already exists**, **who gets paid today**, and **where the wedge is** for one idea in the **current** market. Use live web research; do not rely on memory or uncited synthesis.

Keep validation order: **idea validation** → **market validation** → **product validation**. This skill covers market validation research, not MVP build.

## Workflow

1. **Frame the idea** — one-sentence job-to-be-done, ICP, geography, and solo-plus-AI constraints.
2. **Resolve the research** — read `discovery/INDEX.md`, then that folder's `TOPIC.md` and existing artifacts under `discovery/<topic-slug>/` before contradicting them. **Do not** read `discovery/archive/` or unrelated active researches unless the user explicitly asks.
3. **Search the open web** — run multiple queries; vary keywords (problem, buyer role, category, "alternative", pricing, complaints).
4. **Collect primary evidence** — live pricing pages, product positioning, reviews, founder posts, listings, and forum threads.
5. **Map the market** — direct, indirect, and substitute solutions with price, audience, and strengths.
6. **Identify gaps** — recurring complaints, missing workflows, switching costs, and segments incumbents under-serve.
7. **Size bottom-up** — segment count × adoption × price; use search volume only as a proxy.
8. **Decide** — proceed, pivot wedge, or kill; name the next cheapest test.

## Search playbook

Run at least **three** query families before concluding:

| Family | Example queries |
| --- | --- |
| Category | `[category] software`, `[job to be done] tool` |
| Buyer pain | `[ICP] [pain] workaround`, `how to [job] without [incumbent]` |
| Competition | `[competitor] alternative`, `[competitor] pricing`, `best [category] for [segment]` |
| Demand proxy | `[problem] reddit`, `[category] site:news.ycombinator.com` |

Prefer **current** pages. Capture URL, publisher, and access date for each material claim.

## Source tiers

Use the smallest set that answers the question. Prefer **primary** pages over roundups.

| Tier | Use for | Examples |
| --- | --- | --- |
| **Primary** | Offers, pricing, positioning, reviews, public traction | Company sites, pricing pages, App Store / Play Store, G2, Capterra, Trustpilot, Product Hunt, Indie Hackers, LinkedIn headcount, public founder posts |
| **Market and keyword proxies** | Demand and category language | Google Trends, Google search results, Reddit, Hacker News, niche forums, Discord threads surfaced via search |
| **Idea and revenue databases** | Comparable ideas and public revenue signals | [IdeaProof](https://ideaproof.io/startup-ideas-database), BigIdeasDB, AppMagic, SensorTower |
| **Secondary** | Pointers only until triangulated | News roundups, listicles, VC blogs, analyst summaries |

Do not treat database labels, TAM copy, or viability scores as verified facts. Triangulate with live competitors and buyer language.

## Gap analysis checklist

- [ ] At least **five** named solutions mapped (direct, indirect, or substitute)
- [ ] **Pricing** captured from live pages when available
- [ ] **Recurring complaints** from reviews or forums (not marketing copy)
- [ ] **Gap hypothesis** stated as a buyer job plus segment, not "no one does this"
- [ ] **Clone vs wedge** decision documented
- [ ] **Kill criteria** if no wedge or economics fail the stated goal

## Output

Save to `discovery/<topic-slug>/research/YYYY-MM-DD-<topic-slug>-market.md` unless the user requests a brief-only pass. If the topic folder does not exist, add it under active topics and update `discovery/INDEX.md`.

Default sections:

- **Facts**
- **Assumptions**
- **Evidence** (with URLs)
- **Analysis** (market map, gap, sizing, risks)
- **Decision**
- **Next experiment**

Include:

- Competitor matrix (type, audience, price, strength, weakness, evidence URL)
- Gap table (segment, unmet job, workaround today, wedge, confidence)
- Bottom-up sizing table with formula and sensitivity note
- **Sources** list at the end

## Escalation

- **Economics and pricing depth** → `revenue-model` skill
- **Structured competitor memo** → `competitor-landscape` skill
- **Bottom-up TAM / SAM / SOM** → `market-sizing` skill
- **Demand tests after market evidence** → `validation-experiments` skill
- **Full phased discovery through scorecard** → `behavior-led-validation` and `idea-scorecard` skills

Do not recommend implementation until a scorecard records **Strong go** or **Conditional go** with explicit gaps to close.

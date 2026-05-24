---
name: problem-discovery
description: Runs Mom Test-style problem discovery for software ideas, including ICP definition, interview scripts, pain scoring, and kill criteria. Use when the user asks about problem interviews, pain validation, ICP, customer discovery, or whether a problem is real.
disable-model-invocation: true
---

# Problem Discovery

## Checklist

- [ ] State the problem hypothesis and target user
- [ ] Define ICP and disqualifiers
- [ ] Draft interview questions about past behavior, not hypotheticals
- [ ] Collect evidence from multiple independent sources
- [ ] Score pain frequency and intensity
- [ ] Record workaround behavior
- [ ] Set kill criteria before recommending more work

## Interview rules

- Ask about past behavior, current workarounds, and money or time already spent.
- Do not ask "Would you use this?"
- Treat compliments and friend feedback as weak evidence.

## Evidence table

| Source | Quote or signal | Frequency | Workaround | Willingness signal |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

## Pain score

Rate 1-10 for frequency, intensity, and work impact. Note whether the pain is professional, recurring, and tied to revenue or efficiency.

## Kill criteria

Kill or pause if:

- No independent sources describe the problem
- The problem is rare or tolerated
- Users show no workaround or spend behavior

## Output

Save to `discovery/<topic-slug>/briefs/YYYY-MM-DD-<topic-slug>-brief.md` using Facts, Assumptions, Evidence, Analysis, Decision, Next experiment. Read `discovery/INDEX.md` and the topic's existing artifacts first.

When opening a new active research folder, create `discovery/<topic-slug>/TOPIC.md` from `.cursor/skills/problem-discovery/TOPIC-TEMPLATE.md` and add the slug to `discovery/INDEX.md`.

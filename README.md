# Ideation Discovery Skills

Agent skills for **software and digital business idea validation** — problem discovery, market research, competitor mapping, revenue modeling, behavior-led validation, and go/no-go scorecards.

Skills follow the [Agent Skills](https://agentskills.io/) format and install with the [Skills CLI](https://github.com/vercel-labs/skills).

[![skills.sh](https://skills.sh/b/eltntawy/ideation-discovery-skills)](https://skills.sh/eltntawy/ideation-discovery-skills)

## Available skills

| Skill | Use when |
| --- | --- |
| `problem-discovery` | Problem interviews, ICP, Mom Test-style pain validation |
| `market-research` | Live web market research, gap analysis, cited memos |
| `market-sizing` | Bottom-up TAM, SAM, SOM with search-demand proxies |
| `competitor-landscape` | Competitor matrix, positioning, whitespace |
| `revenue-model` | Pricing, unit economics, LTV:CAC scenarios |
| `validation-experiments` | Smoke tests, landing pages, fake doors, pre-sales |
| `behavior-led-validation` | End-to-end behavior-led validation with payment signals |
| `idea-scorecard` | Weighted go / conditional go / pivot / kill decisions |

## Installation

Install all skills globally (available in every project):

```bash
npx skills add eltntawy/ideation-discovery-skills -g -y
```

Install into the current project only:

```bash
npx skills add eltntawy/ideation-discovery-skills -y
```

Install specific skills:

```bash
npx skills add eltntawy/ideation-discovery-skills --skill problem-discovery --skill idea-scorecard -g -y
```

List skills in this repo without installing:

```bash
npx skills add eltntawy/ideation-discovery-skills --list
```

## Usage

Skills load when the agent detects a matching task from each skill's description, or when you name the skill explicitly.

**Examples:**

```
Run problem discovery interviews for a B2B SaaS idea targeting solo founders
```

```
Score this idea with the idea scorecard before we build anything
```

```
Do market research on AI writing tools for agencies — map competitors and gaps
```

```
Design a pre-sale smoke test with success and kill thresholds
```

## Validation order

These skills enforce a discovery-first sequence:

1. **Idea validation** — is the idea worth deeper research?
2. **Market validation** — demand, reach, and economics
3. **Product validation** — solution fit after a prototype exists

They favor **behavior and payment** over opinions, page views, and compliments.

## Optional workspace layout

Several skills reference a `discovery/<topic-slug>/` folder layout for saving artifacts (`briefs/`, `research/`, `experiments/`, `scorecards/`). That layout is optional — skills still work without it; ask the agent to save outputs wherever you prefer.

## Skill structure

Each skill is a directory under `skills/` containing:

- `SKILL.md` — required instructions and YAML frontmatter (`name`, `description`)
- Supporting templates where needed (e.g. `idea-scorecard/TEMPLATE.md`)

## Contributing

Issues and pull requests welcome. Keep skills concise (under ~500 lines in `SKILL.md`), use third-person descriptions with clear trigger terms, and avoid project-specific paths in cross-skill references.

## License

MIT — see [LICENSE](LICENSE).

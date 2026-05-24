Run the **discovery-playbook** skill from **idea-discovery-playbook**.

Validate this idea **end to end** (phases 0–7). Treat any text the user typed **after** `/discovery-playbook` as the idea, ICP hints, and constraints.

- Propose a `topic-slug` if missing.
- Create `discovery/INDEX.md` and `discovery/<slug>/` if missing.
- Run phases in order; **stop** and report if a kill gate fails.
- **Do not** recommend production build until `idea-scorecard` is **Strong go** (60–75) or **Conditional go** (45–59).

If skills are not installed:

```bash
npx skills add eltntawy/idea-discovery-playbook -g -y
```

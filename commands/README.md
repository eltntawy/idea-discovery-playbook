# Chat commands

Reusable prompts for **Cursor**, **Claude Code**, and **GitHub Copilot**. They invoke the [ideation-discovery-skills](../README.md) pack — install skills first:

```bash
npx skills add eltntawy/ideation-discovery-skills -g -y
```

## Command list

| Command | What it runs |
| --- | --- |
| `/validate` | Full flow — `discovery-playbook` (phases 0–7) |
| `/validate-short` | Weekend path — assumptions → interviews → experiment → scorecard |
| `/validate-assumptions` | `assumption-map` |
| `/validate-interviews` | `problem-discovery` |
| `/validate-market` | `market-research` + `competitor-landscape` |
| `/validate-experiment` | `validation-experiments` |
| `/validate-scorecard` | `idea-scorecard` |
| `/validate-synthesis` | `discovery-synthesis` |

Add your idea **after** the command, for example:

```text
/validate A tool for solo founders to track validation experiments in one place. Topic slug: solo-validation-board
```

---

## Cursor

Commands live in [`.cursor/commands/`](../.cursor/commands/). Type `/` in **Agent** chat and pick a command.

**Project** (this repo): committed with the skills — works when you open this repository.

**Global** (all projects):

```bash
# Windows (PowerShell)
Copy-Item -Recurse .cursor\commands $env:USERPROFILE\.cursor\commands\ideation-discovery

# macOS / Linux
cp -r .cursor/commands ~/.cursor/commands/ideation-discovery
```

Or symlink `~/.cursor/commands/validate.md` → this repo’s file.

Skills must still be installed globally (`-g`) or in the project (`.cursor/skills/` or via `npx skills add`).

---

## Claude Code

Commands live in [`.claude/commands/`](../.claude/commands/). Type `/validate` in Claude Code.

Uses `$ARGUMENTS` for text after the command:

```text
/validate My idea: validation board for solo founders. slug: solo-board
```

**User-wide:**

```bash
cp -r .claude/commands ~/.claude/commands/ideation-discovery
```

Skills: same `npx skills add` install; Claude also loads `.claude/skills/` when present.

---

## GitHub Copilot (VS Code)

Prompt files live in [`.github/prompts/`](../.github/prompts/) (`*.prompt.md`).

1. Enable prompt files: Settings → `"chat.promptFiles": true`
2. In Copilot Chat, type `/validate` (or attach via **Prompt...**)
3. Add your idea in the chat box

Subset shipped: `validate`, `validate-short`, `validate-scorecard`. Copy other `.cursor/commands/*.md` into `.github/prompts/` as `name.prompt.md` if you want the full set.

Optional repo instructions: add a line to `.github/copilot-instructions.md` pointing agents to install and use `discovery-playbook` for idea validation.

---

## Skills vs commands

| | Commands | Skills |
| --- | --- | --- |
| **What** | Short prompt you type with `/` | Full workflow in `skills/*/SKILL.md` |
| **When** | You pick `/validate` in chat | Agent follows skill steps |
| **Install** | Copy `.cursor/commands` or `.claude/commands` | `npx skills add eltntawy/ideation-discovery-skills -g -y` |

Commands tell the agent **which skill to run**; skills contain the detailed checklists and outputs.

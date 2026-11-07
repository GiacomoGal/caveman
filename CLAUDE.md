# CLAUDE.md — caveman

## Fork checkout (GiacomoGal/caveman)

This section is the fork entry. Ordinary language. It does not replace the upstream rules below.

Read [the human preface and the matrix](README.md#matrice) before editing. `AGENTS.md` is the short agent entry and points here. Do not keep a second, divergent matrix.

- Inventory for this lot: fork, not archived, ref `main`, `nextdocscope=unresolved`, identity not proven, current use unknown. UNMAPPED: do not infer a VPS, a service, or an owner from the name `caveman`.
- Local origin path is `github.com/GiacomoGal/caveman`. In-tree text names `JuliusBrussee/caveman` and Julius Brussee. That is upstream authorship and a cited URL, not a proven forge parent and not a host. No API call was made.
- Base before this guide: `63e797cd753b301374947a5ed975c21775d962b9`.
- Skill files are artifacts. Do not rewrite README, AGENTS.md, or this fork section in caveman because those files exist. Apply a skill when its own frontmatter trigger fires, or where an always-on copy already in the tree injects `rules/caveman-activate.md`. This lot does not edit those copies (`.cursor/rules/caveman.mdc`, `.windsurf/rules/caveman.md`, `.clinerules/caveman.md`, `.github/copilot-instructions.md`) and does not edit `GEMINI.md`, which still `@`-includes the skills.
- Upstream percentages ("65%", "~75%", "~46%", and the rest in the product README) are claims. They are not a saving verified here. Do not invent, round, or re-certify them. `benchmarks/results/` lists `.gitkeep` only; result JSON was not opened; `benchmarks/run.py` was not run. `evals/snapshots/results.json` was not opened.
- Do not read secrets, env, backups, memories, or private data. Do not open host paths cited below (`~/.claude/`, `~/.config/caveman/`, `.env.local`). `CLAUDE.original.md` was not read.
- Do not install skills, run hooks, evals, benchmarks, providers, APIs, SSH, sync, merge, deploy, or archive as part of reading this file.
- Do not open an upstream pull request from this documentary lot.
- Commands in the product README are procedures under a separate mandate. Do not run them from this guide.
- This file is not a PASS and not a statement that the product works.

The rules under the next headings stay in force for product work. Where the product pitch says a saving is proven, the matrix rank wins: upstream claim, not a result of this checkout.

## README is a product artifact

README = product front door. Non-technical people read it to decide if caveman worth install. Treat like UI copy.

**Rules for any README change:**

- Readable by non-AI-agent users. If you write "SessionStart hook injects system context," invisible to most — translate it.
- Keep Before/After examples first inside the upstream pitch. That the pitch. The fork preface stands above that pitch and is not part of it.
- Install table always complete + accurate. One broken install command costs real user.
- What You Get table must sync with actual code. Feature ships or removed → update table.
- Preserve voice in the upstream product pitch. Caveman speak there on purpose. "Brain still big." "Cost go down forever." "One rock. That it." — intentional brand. Don't normalize that pitch. The fork preface above the pitch, and the two Fork notes on unverified savings, stay in ordinary language. Do not rewrite those notes into caveman, and do not treat `skills/caveman/SKILL.md` as an order to do so.
- Benchmark numbers from real runs in `benchmarks/` and `evals/`. Never invent or round. Re-run only under a mandate that allows that API call. This documentary reading does not re-run them and does not certify the published percentages.
- Adding new agent to install table → add detail block in `<details>` section below.
- Readability check before any README commit: would non-programmer understand + install within 60 seconds?

---

## Project overview

Upstream product description, not a saving measured in this fork: Caveman makes AI coding agents respond in compressed caveman-style prose. Upstream text says that cuts ~65-75% of output tokens and keeps full technical accuracy. This checkout does not certify that figure. Ships as Claude Code plugin, Codex plugin, Gemini CLI extension, agent rule files for Cursor, Windsurf, Cline, Copilot, 40+ others via `npx skills`.

---

## File structure and what owns what

### Single source of truth files — edit only these

| File | What it controls |
|------|-----------------|
| `skills/caveman/SKILL.md` | Caveman behavior: intensity levels, rules, wenyan mode, auto-clarity, persistence. Only file to edit for behavior changes. |
| `rules/caveman-activate.md` | Always-on auto-activation rule body. CI injects into Cursor, Windsurf, Cline, Copilot rule files. Edit here, not agent-specific copies. |
| `skills/caveman-commit/SKILL.md` | Caveman commit message behavior. Fully independent skill. |
| `skills/caveman-review/SKILL.md` | Caveman code review behavior. Fully independent skill. |
| `skills/caveman-help/SKILL.md` | Quick-reference card. One-shot display, not a persistent mode. |
| `caveman-compress/SKILL.md` | Compress sub-skill behavior. |

### Auto-generated / auto-synced — do not edit directly

Overwritten by CI on push to main when sources change. Edits here lost.

| File | Synced from |
|------|-------------|
| `caveman/SKILL.md` | `skills/caveman/SKILL.md` |
| `plugins/caveman/skills/caveman/SKILL.md` | `skills/caveman/SKILL.md` |
| `.cursor/skills/caveman/SKILL.md` | `skills/caveman/SKILL.md` |
| `.windsurf/skills/caveman/SKILL.md` | `skills/caveman/SKILL.md` |
| `caveman.skill` | ZIP of `skills/caveman/` directory |
| `.clinerules/caveman.md` | `rules/caveman-activate.md` |
| `.github/copilot-instructions.md` | `rules/caveman-activate.md` |
| `.cursor/rules/caveman.mdc` | `rules/caveman-activate.md` + Cursor frontmatter |
| `.windsurf/rules/caveman.md` | `rules/caveman-activate.md` + Windsurf frontmatter |

---

## CI sync workflow

`.github/workflows/sync-skill.yml` triggers on main push when `skills/caveman/SKILL.md` or `rules/caveman-activate.md` changes.

What it does:
1. Copies `skills/caveman/SKILL.md` to all agent-specific SKILL.md locations
2. Rebuilds `caveman.skill` as a ZIP of `skills/caveman/`
3. Rebuilds all agent rule files from `rules/caveman-activate.md`, prepending agent-specific frontmatter (Cursor needs `alwaysApply: true`, Windsurf needs `trigger: always_on`)
4. Commits and pushes with `[skip ci]` to avoid loops

CI bot commits as `github-actions[bot]`. After PR merge, wait for workflow before declaring release complete.

---

## Hook system (Claude Code)

Three hooks in `hooks/`. Communicate via flag file at `~/.claude/.caveman-active`.

```
SessionStart hook ──writes "full"──▶ ~/.claude/.caveman-active ◀──writes mode── UserPromptSubmit hook
                                               │
                                            reads
                                               ▼
                                      caveman-statusline.sh
                                     [CAVEMAN] / [CAVEMAN:ULTRA] / ...
```

### `hooks/caveman-activate.js` — SessionStart hook

Runs once per Claude Code session start. Three things:
1. Writes `"full"` to `~/.claude/.caveman-active` (creates if missing)
2. Emits caveman ruleset as hidden stdout — Claude Code injects SessionStart hook stdout as system context, invisible to user
3. Checks `~/.claude/settings.json` for statusline config; if missing, appends nudge to offer setup on first interaction

Silent-fails on all filesystem errors — never blocks session start.

### `hooks/caveman-mode-tracker.js` — UserPromptSubmit hook

Reads JSON from stdin. Checks if prompt starts with `/caveman`. If yes, writes mode to flag file:
- `/caveman` → configured default (see `caveman-config.js`, defaults to `full`)
- `/caveman lite` → `lite`
- `/caveman ultra` → `ultra`
- `/caveman wenyan` or `/caveman wenyan-full` → `wenyan`
- `/caveman wenyan-lite` → `wenyan-lite`
- `/caveman wenyan-ultra` → `wenyan-ultra`
- `/caveman-commit` → `commit`
- `/caveman-review` → `review`
- `/caveman-compress` → `compress`

Detects "stop caveman" or "normal mode" in prompt and deletes flag file.

### `hooks/caveman-statusline.sh` — Statusline badge

Reads flag file. Outputs colored badge string for Claude Code statusline:
- `full` or empty → `[CAVEMAN]` (orange)
- anything else → `[CAVEMAN:<MODE_UPPERCASED>]` (orange)

Configured in `~/.claude/settings.json` under `statusLine.command`.

### Hook installation

**Plugin install** — hooks wired automatically by plugin system.

**Standalone install** — `hooks/install.sh` (macOS/Linux) or `hooks/install.ps1` (Windows) copies hook files into `~/.claude/hooks/` and patches `~/.claude/settings.json` to register SessionStart and UserPromptSubmit hooks plus statusline.

**Uninstall** — `hooks/uninstall.sh` / `hooks/uninstall.ps1` removes hook files and patches settings.json.

---

## Skill system

Skills = Markdown files with YAML frontmatter consumed by Claude Code's skill/plugin system and by `npx skills` for other agents.

### Intensity levels

Defined in `skills/caveman/SKILL.md`. Six levels: `lite`, `full` (default), `ultra`, `wenyan-lite`, `wenyan-full`, `wenyan-ultra`. Persists until changed or session ends.

### Auto-clarity rule

Caveman drops to normal prose for: security warnings, irreversible action confirmations, multi-step sequences where fragment ambiguity risks misread, user confused or repeating question. Resumes after. Defined in skill — preserve in any SKILL.md edit.

### caveman-compress

Sub-skill in `caveman-compress/SKILL.md`. Takes file path, compresses prose to caveman style, writes to original path, saves backup at `<filename>.original.md`. Validates headings, code blocks, URLs, file paths, commands preserved. Retries up to 2 times on failure with targeted patches only. Requires Python 3.10+.

### caveman-commit / caveman-review

Independent skills in `skills/caveman-commit/SKILL.md` and `skills/caveman-review/SKILL.md`. Both have own `description` and `name` frontmatter so they load independently. caveman-commit: Conventional Commits, ≤50 char subject. caveman-review: one-line comments in `L<line>: <severity> <problem>. <fix>.` format.

---

## Agent distribution

How caveman reaches each agent type:

| Agent | Mechanism | Auto-activates? |
|-------|-----------|----------------|
| Claude Code | Plugin (hooks + skills) or standalone hooks | Yes — SessionStart hook injects rules |
| Codex | Plugin in `plugins/caveman/` with `hooks.json` | Yes — SessionStart hook |
| Gemini CLI | Extension with `GEMINI.md` context file | Yes — context file loads every session |
| Cursor | `.cursor/rules/caveman.mdc` with `alwaysApply: true` | Yes — always-on rule |
| Windsurf | `.windsurf/rules/caveman.md` with `trigger: always_on` | Yes — always-on rule |
| Cline | `.clinerules/caveman.md` (auto-discovered) | Yes — Cline injects all .clinerules files |
| Copilot | `.github/copilot-instructions.md` + `AGENTS.md` | Yes — repo-wide instructions |
| Others | `npx skills add JuliusBrussee/caveman` | No — user must say `/caveman` each session |

Fork note on the Copilot row: `AGENTS.md` in this checkout no longer `@`-includes skill prompts. The short always-on text for Copilot remains `.github/copilot-instructions.md`, which this lot did not edit. Full skill text applies when that skill's own trigger fires. `GEMINI.md` still `@`-includes the four skills; that file was left as upstream wrote it.

For agents without hook systems, minimal always-on snippet lives in README under "Want it always on?" — keep current with `rules/caveman-activate.md`. That snippet is product text for other agents. It is not the style of the fork preface.

---

## Evals

`evals/` has three-arm harness:
- `__baseline__` — no system prompt
- `__terse__` — `Answer concisely.`
- `<skill>` — `Answer concisely.\n\n{SKILL.md}`

Honest delta = **skill vs terse**, not skill vs baseline. Baseline comparison conflates skill with generic terseness — that cheating. Harness designed to prevent this.

`llm_run.py` calls `claude -p --system-prompt ...` per (prompt, arm), saves to `evals/snapshots/results.json`. `measure.py` reads snapshot offline with tiktoken (OpenAI BPE — approximates Claude tokenizer, ratios meaningful, absolute numbers approximate).

Add skill: drop `skills/<name>/SKILL.md`. Harness auto-discovers. Add prompt: append line to `evals/prompts/en.txt`.

Snapshots committed to git. CI reads without API calls. Only regenerate when SKILL.md or prompts change.

---

## Benchmarks

`benchmarks/` runs real prompts through Claude API (not Claude Code CLI), records raw token counts. Results committed as JSON in `benchmarks/results/`. Benchmark table in README generated from results — update when regenerating.

To reproduce: `uv run python benchmarks/run.py` (needs `ANTHROPIC_API_KEY` in `.env.local`).

---

## Key rules for agents working here

- Edit `skills/caveman/SKILL.md` for behavior changes. Never edit synced copies.
- Edit `rules/caveman-activate.md` for auto-activation rule changes. Never edit agent-specific rule copies.
- README most important file for user-facing impact. Optimize for non-technical readers. Preserve caveman voice in the upstream pitch. The fork preface stays ordinary language.
- Benchmark and eval numbers must be real. Never fabricate or estimate.
- CI workflow commits back to main after merge. Account for when checking branch state.
- Hook files must silent-fail on all filesystem errors. Never let hook crash block session start.
- Fork limits at the top of this file outrank a reading of these bullets that would delete the preface, certify a token saving, infer a host from the name, or open an upstream pull request from this lot.

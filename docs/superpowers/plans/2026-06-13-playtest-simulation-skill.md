# ttrpg-playtest-simulation Skill Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking. Because the deliverable is a prose skill file, ALSO invoke `superpowers:writing-skills` during execution for authoring conventions and final validation.

**Goal:** Author the `ttrpg-playtest-simulation` skill — a methodology for running dynamic, turn-by-turn simulated playtests that surface bugs static analysis misses — plus the repo folder its reports land in.

**Architecture:** A single user-level `SKILL.md` (house style, dense, methodology-only) at `~/.claude/skills/ttrpg-playtest-simulation/`, matching the existing `ttrpg-*` siblings. The skill describes two run modes (single-context default, subagent table opt-in), an adversarial player roster, two-pass GM adjudication, a per-turn watch list, and a triaged findings report written to a new in-repo `docs/superpowers/playtests/` folder. The skill finds; it never fixes.

**Tech Stack:** Markdown only. No build, no test framework. Verification = manual checks against the spec's acceptance criteria and the house style observed in `~/.claude/skills/ttrpg-balance-analysis/SKILL.md` and `ttrpg-system-review/SKILL.md`.

**Source spec:** `docs/superpowers/specs/2026-06-13-playtest-simulation-skill-design.md`

**Path note:** The `SKILL.md` is NOT inside this git repo — it lives under the user's home `~/.claude/skills/`. Only the `docs/superpowers/playtests/` folder is committed to this repo. Do not attempt to `git add` the skill file.

---

## File Structure

- Create (outside repo): `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md` — the entire skill, single file, house style.
- Create (in repo): `docs/superpowers/playtests/README.md` — establishes the reports folder and documents what lands here and the naming convention.

Both the skill prose and this plan reference the same canonical structure for `SKILL.md`, authored in this section order:
1. Frontmatter (`name`, `description` with "Use when…")
2. Overview + Core principle + the three-skill boundary
3. Execution model (Mode B default, Mode A opt-in)
4. Adversarial player roster
5. Session procedure (two-pass adjudication + watch list)
6. Findings report (artifact, schema, severity, triage, find-not-fix)
7. Quick Reference + Common Mistakes + Related Skills

---

## Task 1: Establish the reports folder in the repo

**Files:**
- Create: `docs/superpowers/playtests/README.md`

- [ ] **Step 1: Write the folder README**

Create `docs/superpowers/playtests/README.md` with this exact content:

```markdown
# Playtest Reports

Dynamic playtest reports produced by the `ttrpg-playtest-simulation` skill.

Each run writes a dated file here, kept separate from design specs so playtest
output and design intent don't intermix.

**Naming:** `YYYY-MM-DD-playtest-<scenario>.md`

**Each report contains:**
- The scenario and exact character builds used (so the run is reproducible)
- A condensed turn-by-turn session log
- A prioritized findings list: `id · severity · turn ref · spec link · failure class · repro · routed-to skill`

The skill **finds; it does not fix.** Each finding is routed to the relevant
design skill (balance-analysis, ability-design, rules-writing, creature-design,
system-review) for remediation.
```

- [ ] **Step 2: Verify the file exists and reads correctly**

Run: `git status --short docs/superpowers/playtests/`
Expected: shows `?? docs/superpowers/playtests/README.md`

- [ ] **Step 3: Commit**

```bash
git add docs/superpowers/playtests/README.md
git commit -m "Add playtests report folder for ttrpg-playtest-simulation"
```

---

## Task 2: Create the skill file with frontmatter, Overview, and boundary

**Files:**
- Create: `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md`

- [ ] **Step 1: Re-read a sibling skill for exact house style**

Read `~/.claude/skills/ttrpg-system-review/SKILL.md` in full to match: frontmatter shape, `# Title`, `## Overview` with a bolded **Core principle:**, dense tables, and the closing `## Related Skills` paragraph.

- [ ] **Step 2: Create the skill directory and write the opening block**

Create `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md` beginning with this exact content:

````markdown
---
name: ttrpg-playtest-simulation
description: Use when running a dynamic, turn-by-turn simulated playtest of TTRPG content to surface bugs static analysis misses — action-economy exploits, repeatable loops, dead turns, table-level rules ambiguity, predictable misreads. Also use when content passes the math but breaks at the table, when a combo or sequence feels exploitable, or before a milestone gate to validate a slice end-to-end.
---

# TTRPG Playtest Simulation

## Overview

A playtest simulation *runs* the rules instead of reading them. It executes
content turn-by-turn at a simulated table to surface the defects that only appear
in an actual sequence of play — exploits that need setup, loops that need a cycle,
turns that are dead only in context, and text that is ambiguous or misread only
when someone has to act on it right now.

**Core principle:** Play to break it, not to enjoy it. The simulated table exists
to manufacture failure, so players are adversarial by mandate and the GM logs
every gap it has to paper over. The output is a prioritized findings report routed
to fix skills — this skill **finds; it never fixes.**

## Boundary — what this is *not*

| Skill | Question | Mode |
|-------|----------|------|
| ttrpg-balance-analysis | Do the numbers compare fairly? | Static math |
| ttrpg-system-review | Do the rules agree and cover the loop? | Reading the rules |
| **ttrpg-playtest-simulation** | **What breaks when you actually run it?** | **Executing the rules** |

If a question can be answered without playing a turn, it belongs in one of the
other two skills. Send number problems to balance-analysis and structural holes
to system-review; this skill is for what only emerges in live sequence.
````

- [ ] **Step 3: Verify frontmatter and structure**

Confirm: `name` exactly matches the directory name; `description` starts with "Use when"; the file has `# TTRPG Playtest Simulation`, `## Overview` with a bolded `**Core principle:**`, and the boundary table. (No repo commit — file is outside the repo.)

---

## Task 3: Author the execution model (run modes)

**Files:**
- Modify: `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md` (append)

- [ ] **Step 1: Append the execution-model section**

Append this exact content to `SKILL.md`:

````markdown
## Execution Model: One Methodology, Many Actors

The "playtester" and "GM" are roles you spin up, not separate skills. Two run
modes. **Mode B is the default; use Mode A only when explicitly asked** ("Mode A",
"subagent playtest", "high-fidelity run").

### Mode B — Single-context role-play (DEFAULT)

One agent (you) voices the GM and all personas in-context. Cheap, fast, the
everyday run. Its weakness is shared knowledge — knowing the intended design makes
play charitable. Mitigate it:

- Play each persona in deliberate adversarial character (see the roster), arguing
  *against* the design, not for it.
- Treat the result as a strong smoke test, not a hard gate. For a milestone gate,
  escalate to Mode A.

### Mode A — Subagent table (opt-in, high fidelity)

Run only on request, for milestone gates. The validity gain comes from
**information asymmetry**: a player who can see intended use never finds the
*un*intended one.

- **GM subagent:** dispatched with the *full specs* (rules + designer intent).
- **Player subagents:** up to four, each given **only the player-facing rules plus
  its persona — deliberately blind to designer intent and to the other personas'
  reasoning.**
- **Orchestration:** you are the table conductor. Set the scene via the GM agent;
  for each turn, query the active player agent for its declared action, relay it to
  the GM agent for adjudication, relay the result back. Use the agent-continuation
  channel so each actor keeps its own context across turns.
- Cost is high (many round-trips). That is the price of a real gate; do not run it
  for routine checks.
````

- [ ] **Step 2: Verify**

Confirm Mode B is labelled DEFAULT and Mode A as opt-in, and that the asymmetry rationale is stated. Matches spec §2.

---

## Task 4: Author the adversarial roster and session procedure

**Files:**
- Modify: `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md` (append)

- [ ] **Step 1: Append the roster and procedure sections**

Append this exact content to `SKILL.md`:

````markdown
## The Adversarial Player Roster

Mandated panel — each persona hunts one failure class. Run the full four; if you
must use fewer, name which you dropped (coverage gap). Each plays to expose its
class, not to win the fiction.

| Persona | Hunts | Plays like |
|---------|-------|-----------|
| The Optimizer | balance/exploit, nova alpha-strikes, one dominant line | always takes the mathematically best action; stacks every resource into one spike |
| The Rules-Lawyer | wording loopholes, undefined interactions | reads rules literally; asks "where does it say I can't?"; chains effects the text doesn't forbid |
| The Chaos Player | unintended actions, scene/edge cases | does the off-script thing; targets terrain, allies, the environment; refuses the obvious plan |
| The New Player | misreads, unclear text, trap picks, analysis paralysis | acts on the first plain reading; picks the option that *sounds* good; stalls when text is unclear |

## Session Procedure

1. **Scenario setup.** Pick a target from the specs. Build the needed character(s)
   strictly per the rules and define one encounter or social scene. Record exact
   builds and scenario verbatim — the run must be reproducible.
2. **Run turn-by-turn with two-pass GM adjudication.** At every decision point:
   - **Pass 1 — rules-as-written.** Adjudicate using only what the text says.
     Whenever the text is silent or ambiguous and you must improvise, **log it as a
     finding** — a gap a human GM would also hit. Do not skip the log to keep
     things smooth; the log *is* the product.
   - **Pass 2 — proceed on intent.** Make a best-guess ruling so the session
     continues. This also yields end-to-end playability coverage.
3. **Apply the per-turn watch list.** Flag a finding whenever you see:
   - **action-economy net positive** — an action producing more than one action of value
   - **repeatable loop** — A→B→A that doesn't consume a limited resource
   - **dead turn** — no meaningful choice, or one forced action
   - **ambiguous ruling required** — ties back to a Pass-1 gap
   - **predictable misread** — the New Player took the obvious-but-wrong reading
   - **degenerate dominance** — one option is always correct
````

- [ ] **Step 2: Verify**

Confirm all four personas present (Optimizer, Rules-Lawyer, Chaos, New Player), two-pass adjudication described with the Pass-1 logging mandate, and all six watch-list items present. Matches spec §3–4.

---

## Task 5: Author the findings report (artifact, schema, triage)

**Files:**
- Modify: `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md` (append)

- [ ] **Step 1: Append the report section**

Append this exact content to `SKILL.md`:

````markdown
## The Findings Report

Every run writes a durable artifact — never findings-in-chat-only for a gate.

- **Location:** `docs/superpowers/playtests/YYYY-MM-DD-playtest-<scenario>.md`
  (its own folder, separate from design specs).
- **Contents, in order:** (1) scenario + exact builds; (2) a condensed
  turn-by-turn session log; (3) the prioritized findings list.
- **Finding schema:** `id · severity · turn ref · spec link · failure class ·
  repro · routed-to skill`.

### Severity rubric

| Severity | Means |
|----------|-------|
| Critical | breaks or blocks play, or a confirmed degenerate engine (infinite loop, unbounded nova) |
| Major | clear exploit, or confusion that recurs across turns/personas |
| Minor | annoyance or narrow edge case |
| Note | watch-list observation, not yet a problem |

### Triage — find, don't fix

This skill never edits the design. Route each finding to the skill that fixes it:

| Finding class | Routed to |
|---------------|-----------|
| Number / exploit / nova / eHP | ttrpg-balance-analysis |
| Ability identity / dead pick / dominance | ttrpg-ability-design |
| Ambiguous or misread text | ttrpg-rules-writing |
| Creature or encounter behaviour | ttrpg-creature-design |
| Cross-subsystem hole | ttrpg-system-review |
````

- [ ] **Step 2: Verify**

Confirm report path is `docs/superpowers/playtests/...`, the seven-field schema is present, the four-tier severity rubric is present, and the triage table routes to all five sibling skills. Matches spec §5.

---

## Task 6: Author scaffolding (Quick Reference, Common Mistakes, Related Skills)

**Files:**
- Modify: `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md` (append)

- [ ] **Step 1: Append the closing scaffolding**

Append this exact content to `SKILL.md`:

````markdown
## Quick Reference

- [ ] Scenario + exact builds recorded (reproducible)
- [ ] Run mode chosen: Mode B default, Mode A only if requested
- [ ] Full adversarial roster played (or dropped personas named)
- [ ] Two-pass adjudication: every Pass-1 gap logged
- [ ] Watch list applied each turn
- [ ] Report written to docs/superpowers/playtests/ with the finding schema
- [ ] Severity assigned and every finding triaged to a fix skill
- [ ] Find-not-fix held: no design edits made here

## Common Mistakes

| Mistake | Symptom | Fix |
|---------|---------|-----|
| Charitable play | Session "works", finds nothing | Play personas adversarially; the panel exists to break it |
| GM smoothing over gaps | Ambiguities never surface | Log every Pass-1 improvisation before proceeding |
| Fixing inline | Spec edited mid-run, issue masked | Record the finding; route to the fix skill, change nothing |
| Players seeing intent (Mode A) | Exploits/misreads vanish | Give player agents player-facing rules only; withhold intent |
| Treating Mode B as a gate | Milestone signed off on a smoke test | Escalate to Mode A for gates |
| No artifact | Findings lost, not diffable | Always write the dated report for a real run |

## Related Skills

Validate numbers behind a finding with ttrpg-balance-analysis; audit structure
with ttrpg-system-review. Route fixes to ttrpg-ability-design, ttrpg-rules-writing,
and ttrpg-creature-design. Probability foundations: ttrpg-core-mechanic.
````

- [ ] **Step 2: Verify**

Confirm Quick Reference checklist, Common Mistakes table, and Related Skills paragraph are all present and match house style.

---

## Task 7: Final validation against spec acceptance criteria

**Files:**
- Read: `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md`
- Read: `docs/superpowers/specs/2026-06-13-playtest-simulation-skill-design.md`

- [ ] **Step 1: Invoke writing-skills for conventions check**

Invoke `superpowers:writing-skills` and run its validation against the finished `SKILL.md` (frontmatter correctness, name/dir match, description trigger phrasing, no dangling references).

- [ ] **Step 2: Walk the acceptance criteria**

Confirm each spec acceptance criterion is met:
- [ ] SKILL.md exists at `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md`
- [ ] Frontmatter `name` + "Use when…" `description`; Overview + Core principle; dense tables; Quick Reference; Common Mistakes; Related Skills
- [ ] States boundary vs balance-analysis and system-review
- [ ] Documents both run modes — B default, A opt-in for gates
- [ ] Mandates adversarial roster, two-pass adjudication, per-turn watch list
- [ ] Specifies report location, finding schema, severity rubric, triage routing, find-not-fix
- [ ] A reader can run a playtest end-to-end from the skill alone

- [ ] **Step 3: Smoke-test the skill**

Mentally (or in-chat) run a one-encounter Mode B playtest against an existing spec to confirm the procedure is followable start-to-finish and produces a report in the documented shape. Note any step that stalls; fix the skill text.

- [ ] **Step 4: Confirm completion**

Report which acceptance criteria pass and surface any gaps. No repo commit for the skill file (outside repo); the only repo change was Task 1's folder README.

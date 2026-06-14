# Design Spec: `ttrpg-playtest-simulation` skill

**Date:** 2026-06-13
**Status:** Approved (brainstorming complete)
**Type:** New user-level skill (methodology) + subagent orchestration pattern

## Problem

The project has a complete playable vertical slice (12 specs) plus two validation
skills: `ttrpg-balance-analysis` (static math — DPR/eHP/action-value) and
`ttrpg-system-review` (structural audit — reading the rules for consistency,
holes, dead options). Neither one *plays the game*. A whole class of defects only
appears when content is executed turn-by-turn: action-economy exploits that need a
real sequence, repeatable loops, dead turns in context, rules that are ambiguous
*at the table*, and text players predictably misread.

We need a dynamic, experiential validation layer — a simulated playtest — that
surfaces those bugs and feeds them back into the specs.

## Goal & Non-Goals

**Goal:** A methodology skill that runs a simulated playtest session turn-by-turn
and produces a prioritized findings report routed to the right fix skills.

**Non-goals:**
- Not balance math (stays in `ttrpg-balance-analysis`).
- Not a static structural audit (stays in `ttrpg-system-review`).
- Not "is it fun" feel-testing as the primary aim (a secondary by-product at most).
- The skill **finds; it does not fix.** No design changes applied by this skill.

## Division of Labor (the boundary that justifies a new skill)

| Skill | Question it answers | Mode |
|-------|--------------------|------|
| `ttrpg-balance-analysis` | "Do the numbers compare fairly?" | Static math |
| `ttrpg-system-review` | "Do the rules agree and cover the loop?" | Reading the rules |
| **`ttrpg-playtest-simulation`** | **"What breaks when you actually run it?"** | **Executing the rules** |

## Design

### 1. Identity

- **Location:** `~/.claude/skills/ttrpg-playtest-simulation/SKILL.md` (user-level,
  alongside the other `ttrpg-*` skills). Single-file, house style.
- **Frontmatter description (triggers):** running a dynamic/simulated playtest of
  TTRPG content turn-by-turn to surface bugs static analysis misses; also when
  content "passes the math but breaks at the table," when a combo/sequence feels
  exploitable, or before a milestone gate to validate a slice end-to-end.

### 2. Execution model — skill + subagents

The "playtester" and "playtest GM" the user asked about are **subagents the skill
spins up**, not separate skills. One methodology, many actors. Two run modes:

- **Mode A — Subagent table (default for real validation runs):**
  - One **GM subagent** with the *full specs* (rules + designer intent).
  - Up to four **player subagents**, each given **only player-facing rules + their
    persona — blind to designer intent.**
  - The orchestrator passes turns between them (dispatch / SendMessage), feeding
    each player's declared action to the GM and the GM's adjudication back.
  - **Validity mechanism = information asymmetry.** A player who can see intended
    use never finds the unintended one; withholding intent manufactures the real
    misreads and exploits.
  - Cost: heavy (many round-trips). Acceptable — playtest is a deliberate gate,
    not a constant.

- **Mode B — Single-context role-play (explicit lightweight fallback):**
  - One agent voices GM + all personas in-context.
  - Cheap, good for a fast smoke test; weaker validity (shared knowledge → more
    charitable play). The skill marks this clearly as a smoke test, not a gate.

### 3. The adversarial player roster

Fixed panel; each persona hunts one failure class. The skill mandates this roster
(or a documented subset) so runs are repeatable and coverage is intentional.

| Persona | Hunts |
|---------|-------|
| The Optimizer | balance/exploit, nova alpha-strikes, single dominant line |
| The Rules-Lawyer | wording loopholes, undefined interactions, "RAW says I can" |
| The Chaos Player | unintended actions, scene/edge cases, off-script choices |
| The New Player | misreads, unclear text, analysis paralysis, trap picks |

### 4. Session procedure

1. **Scenario setup:** pick a target from the specs — build the needed
   character(s) per the rules, and an encounter or social scene to run. Record the
   exact builds and scenario so the run is reproducible.
2. **Run turn-by-turn** with **two-pass GM adjudication:**
   - Pass 1 — adjudicate strictly rules-as-written; whenever the text is silent or
     ambiguous and the GM must improvise, **log that as a finding** (a gap a human
     GM would also hit).
   - Pass 2 — proceed on a best-guess intent ruling so the session completes (also
     gives end-to-end playability coverage).
3. **Per-turn watch list** — flag when seen:
   - action-economy *net positive* (an action producing >1 action of value)
   - repeatable loop (A→B→A not consuming a limited resource)
   - dead turn (no meaningful choice / forced single action)
   - ambiguous ruling required (links back to Pass 1)
   - predictable misread (New Player took the text the "wrong" obvious way)
   - degenerate dominance (one option is always correct)

### 5. Findings report (artifact + triage)

- **Artifact:** a dated report written to `docs/superpowers/specs/`
  (`YYYY-MM-DD-playtest-<scenario>.md`), matching the Gate A pattern, so runs are
  durable and diffable across slices.
- **Contents:** the scenario + builds, a condensed session/turn log, then a
  prioritized findings list.
- **Finding schema:** `id · severity · turn ref · spec link · failure class ·
  repro · routed-to skill`.
- **Severity rubric:** Critical (breaks/blocks play or a known-degenerate engine) /
  Major (clear exploit or recurring confusion) / Minor (annoyance, edge case) /
  Note (watch-list, not yet a problem).
- **Triage table — find, don't fix:** each finding routes to a fix skill.

  | Finding class | Routed to |
  |---------------|-----------|
  | Number/exploit/nova/eHP | `ttrpg-balance-analysis` |
  | Ability identity / dead pick / dominance | `ttrpg-ability-design` |
  | Ambiguous or misread text | `ttrpg-rules-writing` |
  | Creature/encounter behaviour | `ttrpg-creature-design` |
  | Cross-subsystem hole | `ttrpg-system-review` |

### 6. Scaffolding (house style)

- **Quick Reference** checklist (setup recorded · roster covered · two-pass run ·
  watch list applied · report written · findings triaged · find-not-fix held).
- **Common Mistakes** table (e.g., charitable play, GM smoothing over gaps,
  fixing inline, players seeing intent, single-context run treated as a gate).
- **Related Skills** cross-links to the three siblings above.

## Acceptance Criteria

- `SKILL.md` exists at the user-level path, validates against the house style
  (frontmatter `name` + "Use when…" `description`; Overview + Core principle;
  dense tables; Quick Reference; Common Mistakes; Related Skills).
- Skill clearly states the boundary vs `balance-analysis` and `system-review`.
- Documents both run modes, marking A as the default gate and B as a smoke test.
- Mandates the adversarial roster, two-pass adjudication, per-turn watch list.
- Specifies the report artifact location, finding schema, severity rubric, and
  triage routing — and the find-not-fix discipline.
- A reader can run a playtest end-to-end from the skill alone.

## Out of Scope / Future

- Automated dice/encounter simulators (this is narrative turn execution, not code).
- A standalone "feel/fun" testing skill (could be a future sibling).

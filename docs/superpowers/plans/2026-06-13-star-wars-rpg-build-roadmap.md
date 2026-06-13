# Star Wars RPG — Framework Build Roadmap

> **Note on format:** This is a *design roadmap*, not a code implementation plan. Each "phase" is a design effort driven by a dedicated TTRPG skill and produces a spec document under `docs/superpowers/specs/`. "Tests" here are design review gates (balance analysis, system review, table playtest), not unit tests.

**Goal:** Sequence the design of the Star Wars RPG rules framework so dependencies are respected, the two novelties (no daily resource clock, no mandatory healer) are de-risked early, and the system reaches a *playable vertical slice* before any content is mass-produced.

**Approach:** Build the engine bottom-up (resolution → character → progression), then a thin vertical slice of content (social engine + one class per archetype + basic gear + a few creatures), balance-check and playtest the slice, *then* expand content on the proven chassis. Review gates sit between layers.

**Driving artifact:** [2026-06-13-star-wars-rpg-design-philosophy.md](../specs/2026-06-13-star-wars-rpg-design-philosophy.md) — every phase cites the pillars, tensions (T1–T5), and the binding licensing constraint (Section 0).

---

## Dependency Graph

```
Phase 0  Philosophy  ✅ DONE
            │
Phase 1  Core Mechanic + Trait System        (resolves T1 numerics, T2)
            │
Phase 2  Character Framework                  (attributes, skills, derived stats, recovery iface)
            │
Phase 3  Progression Chassis                  (level cadence, cooldown/resource model — T3)
            │
   ┌────────┼─────────────────────────┐
Phase 4   Phase 5                    Phase 6
Social/   Class Design +            Equipment & Economy
Intrigue  Force Subsystem           (consumables feed recovery — T3)
Engine    (T4, T5)
   └────────┼─────────────────────────┘
            │
Phase 7  Creatures & Challenge Framework      (bounded-accuracy enemy scaling — Pillar 1)
            │
  ═══  MILESTONE: PLAYABLE VERTICAL SLICE  ═══
            │
   GATE A: Balance Analysis  →  GATE B: Table Playtest
            │
Phase 8  Content Expansion + Light Supporting Systems (starships/vehicles/exploration)
            │
   GATE C: System Review (cross-artifact consistency)
            │
Phase 9  Rules Writing Consolidation  →  Framework 1.0
```

A first-class pillar (Social/Intrigue, Phase 4) and the content layers (5, 6) sit at the same dependency depth — they can be designed in any order or in parallel, but **all three must reach at least a thin version for the vertical slice.**

---

## Cross-Cutting Conventions (apply to every phase)

- **Spec output:** each phase writes `docs/superpowers/specs/YYYY-MM-DD-<layer>.md` and commits.
- **Trait discipline:** every entity defined in any phase (action, feat, item, class feature, creature) carries traits per the Phase 1 trait framework. No untyped content.
- **Licensing:** mechanics paraphrased in our own words; verbatim text only from ORC (Paizo) or SRD CC-BY (WotC), with attribution. (Philosophy §0.)
- **Ability principle:** any individual ability/feat/power is designed under `ttrpg-ability-design` and must satisfy Pillars 3 & 5 (active verb, engages rather than deletes challenges).
- **Per-phase exit check:** before a phase is "done," confirm it doesn't violate any pillar and that it actually resolves the tensions assigned to it.

---

## Phase 1 — Core Mechanic + Trait System

**Driving skill:** `ttrpg-core-mechanic` (+ trait framework as foundational infrastructure)
**Depends on:** Philosophy only.
**Resolves:** T1 (exact proficiency math), T2 (four-degree thresholds under bounded math), Pillar 1 (bounded participation math).

**Must define:**
- Dice & resolution: d20 vs DC, the four-degree engine (success/crit thresholds) tuned so crit frequency stays stable across the level band despite small modifiers (T2).
- Exact proficiency formula: `1 + (level // 4, min 1)` term **+ +1 per rank** (provisional per user note), and the *rank-gated effects* mechanism (what untrained simply cannot attempt) that carries "expertise feel" without bigger numbers.
- Action economy: three actions, free actions, one reaction/round; how multi-action activities and the action-cost notation work.
- Bonus-type rules: status & circumstance only — stacking rules, typical magnitudes within bounded math.
- **Trait system framework:** what a trait *is* (machine-readable tag), how traits encode prerequisites/conditions, the trait taxonomy skeleton (e.g., type traits, rarity, action, damage, Force, faction). This is infrastructure every later phase consumes.

**Exit gate:** a worked example showing a level-1 and level-12 character both meaningfully engaging the same mid-level check (Pillar 1), and a crit-frequency sanity table across levels (T2).

---

## Phase 2 — Character Framework

**Driving skill:** `ttrpg-character-framework`
**Depends on:** Phase 1.
**Resolves:** Pillar 2 (no mandatory seats — recovery decoupled from class).

**Must define:**
- Attributes as raw modifiers (no scores, no +/- pairs); how many, their names, generation method at creation.
- Skill list & proficiency application (ranks from Phase 1 applied to skills).
- Derived stats: HP model, defenses (AC/saves equivalents) under bounded accuracy, initiative.
- **Recovery interface:** the any-character out-of-combat recovery mechanic (Medicine-skill-driven), plus the *hooks* for in-combat patching (consumable slot, action cost) — economy filled in Phase 6. No mandatory healer.
- Character creation skeleton: order of operations, species/ancestry slot, background slot (full content later).

**Exit gate:** a complete blank character sheet skeleton; a demonstration that a healer-less party can recover to full between encounters using only universal options.

---

## Phase 3 — Progression Chassis

**Driving skill:** `ttrpg-progression-design`
**Depends on:** Phase 2.
**Resolves:** T3 (cooldown/action-economy as the resource model, formalized), Pillar 4 (a meaningful choice every level; no dead levels).

**Must define:**
- Level range (e.g., 1–20?) and the per-level advancement table skeleton: what *kind* of thing unlocks each level (class feature, feat slot, skill increase, attribute boost) such that **every level has a play-changing choice**.
- The cooldown/resource taxonomy: how "cooldowns" are measured (rounds; possibly scenes for big effects), recharge triggers, and the rule that there are **no daily pools**.
- Proficiency advancement track (when ranks go up, tied to Phase 1 math + bounded accuracy).
- Multiclassing/archetype rules (how the trait system gates cross-class access).

**Exit gate:** a filled level-by-level chassis table with zero dead levels; a written statement of how class depth is expressed without daily resources (T3).

---

## Phase 4 — Social / Intrigue Engine

**Driving skill:** `ttrpg-core-mechanic` (subsystem) + `ttrpg-ability-design` (social actions)
**Depends on:** Phases 1–2 (shares the resolution engine and uses skills).
**Resolves:** Core-loop second pillar; Pillar 5 (engage, don't delete — social actions are active, not "auto-win the negotiation").

**Must define:**
- The tracked social state (e.g., disposition / suspicion / faction standing) and how the three-action grammar maps onto a social scene.
- The standard social actions (the social equivalent of Strike/Stride) as trait-tagged abilities running on the four-degree engine.
- Failure/consequence structure so social scenes have stakes without binary win/lose.
- Hooks for class "social verbs" (filled in Phase 5).

**Exit gate:** a runnable example social scene resolved entirely through the engine, with at least two genuinely different good action choices per turn (Pillar at the social layer).

---

## Phase 5 — Class Design + Force Subsystem

**Driving skill:** `ttrpg-class-design` (+ `ttrpg-ability-design` for each feature/power)
**Depends on:** Phases 1–3 (chassis), references Phase 4 (social verbs).
**Resolves:** T4 (Force users as verb-having classes, not slot-casters), T5 (niche over tier), Pillars 3 & 4.

**Must define:**
- The **class chassis**: what every class receives at each level (hooking the Phase 3 table), and the "verb" design pattern (each class's signature active mechanic).
- The **Force subsystem**: how Force powers work as a broad, cooldown-gated, trait-gated toolkit — no spell slots, no daily clock, balanced horizontally against martials (T4). Healing-via-Force is *an* option, never *the* required one (Pillar 2).
- A **vertical-slice class roster** spanning the spectrum: at minimum one martial/soldier, one skill/scoundrel, one Force user, one tech/pilot — each with a distinct verb (Pillar 3) and a no-dead-levels progression (Pillar 4).

**Exit gate:** the four slice classes drafted to ~level 5; a same-class divergence check (two builds of one class play differently by level 3, Pillar 4); a contribution-parity argument across the four (T5).

---

## Phase 6 — Equipment & Economy

**Driving skill:** `ttrpg-equipment-design`
**Depends on:** Phases 1–2; calibrated against Phase 5 classes.
**Resolves:** T3 (consumables as the money-gated expendable that backs the no-daily-resource model), Pillar 1 (gear doesn't break bounded math).

**Must define:**
- Weapon/armor framework under bounded accuracy (gear adds *options and traits*, not runaway numbers).
- **Consumables** (stimpacks, grenades, etc.) — explicitly the layer that fills the Phase 2 recovery hooks and the Phase 5 cooldown-adjacent expendables.
- The money economy that prices consumables and gear so the "spend money for uptime" loop is balanced.
- Just enough gear for the vertical slice (not a full catalog yet).

**Exit gate:** a basic-gear set the slice classes can use; a demonstration that no single weapon/armor dominates (equipment skill's anti-dominance check).

---

## Phase 7 — Creatures & Challenge Framework

**Driving skill:** `ttrpg-creature-design`
**Depends on:** Phases 1–2 (PC math), 5–6 (to calibrate against).
**Resolves:** Pillar 1 (enemies scale via HP/abilities, not to-hit/defense, per the bounded-accuracy brief).

**Must define:**
- Stat block template (trait-tagged).
- The challenge/encounter-building math under bounded accuracy: how to rate a fight, how enemy scaling works (HP + abilities, near-flat attack/defense).
- Monster roles so encounters vary (Pillar: every encounter shouldn't feel the same).
- A handful of slice creatures across a small level range.

**Exit gate:** an encounter the slice party can fight; confirmation that a higher-level enemy threatens via durability/abilities rather than unhittable defenses (Pillar 1).

---

## ═══ MILESTONE: Playable Vertical Slice ═══

At this point the system can run a real session: 4 pregen characters (the slice classes), basic gear, a combat encounter, and a social scene, levels ~1–5.

### GATE A — Balance Analysis
**Driving skill:** `ttrpg-balance-analysis`
Quantify DPR, hit chances, effective HP, action-economy value across the four slice classes and slice creatures. Verify horizontal balance (T5) and that the no-healer recovery loop survives contact with real numbers. Fix outliers before playtest.

### GATE B — Table Playtest
Run the slice at a table (or simulate). The two novelties get their first real test: does combat work without a daily clock? Does a healer-less party survive? Revisit the T1 `+1/rank` provisional decision here (does expertise *feel* different?). Feed findings back into the relevant phase specs.

---

## Phase 8 — Content Expansion + Light Supporting Systems

**Driving skills:** `ttrpg-class-design`, `ttrpg-equipment-design`, `ttrpg-creature-design`, `ttrpg-ability-design` (iteratively); `ttrpg-core-mechanic` (thin) for supporting systems.
**Depends on:** a *passed* vertical slice (Gates A & B).

**Must define:**
- Additional classes, species/ancestries, backgrounds, feats, gear, and creatures — built on the now-proven chassis, each passing the per-ability and balance checks.
- **Light supporting systems:** starships/vehicles, exploration/survival — deliberately thin, reusing the core engine (Philosophy §3 budget discipline). A vehicle chase should be learnable in ~2 minutes by anyone who knows combat.

**Exit gate (per content batch):** runs through `ttrpg-balance-analysis` spot-checks; no new dead levels or mandatory seats introduced.

---

## ═══ GATE C — System Review ═══
**Driving skill:** `ttrpg-system-review`
Cross-artifact audit before 1.0: undefined interactions, trait-tag consistency, dead/trap options, design drift between early and late content, missing rules. Resolves recurring table disputes into errata.

---

## Phase 9 — Rules Writing Consolidation → Framework 1.0

**Driving skill:** `ttrpg-rules-writing`
**Depends on:** everything above, post-System-Review.

**Must define:**
- Player-facing prose for the framework: rulebook structure, ability/stat-block entry format, glossary, quickstart. Turns the design specs into text players can learn and look up.
- Final pass ensuring licensing attributions (ORC / CC-BY) are present and correct (Philosophy §0).

**Exit gate:** a coherent, navigable framework rulebook (v1.0) that a new group could learn from.

---

## Open Questions Parked for Their Phase

- **Setting/era & IP:** the Star Wars setting is closed IP (Philosophy §0). When does it get addressed, and with what serial-numbers-filed approach for public distribution? *(Not a rules-engine question; flag before Phase 9 / any release.)*
- **Level ceiling:** decided in Phase 3.
- **Attribute count & names:** decided in Phase 2.
- **T1 `+1/rank`:** provisional; re-evaluated at Gate B.

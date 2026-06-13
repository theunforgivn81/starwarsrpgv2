# Phase 3 — Progression Chassis

**Status:** Approved
**Date:** 2026-06-13
**Roadmap phase:** 3 of 9 — see [build roadmap](../plans/2026-06-13-star-wars-rpg-build-roadmap.md)
**Upstream:** [Design Philosophy](2026-06-13-star-wars-rpg-design-philosophy.md), [Phase 1 — Core Mechanic & Traits](2026-06-13-phase1-core-mechanic-and-traits.md), [Phase 2 — Character Framework](2026-06-13-phase2-character-framework.md)
**Resolves:** Pillar 4 (no dead levels), T3 (cooldown/action-economy resource model — fully formalized here). Closes Phase 2's deferred attribute-boost schedule.

> **Note:** *(Gate A)* = provisional pending balance calibration. *(content: Phase N)* = a slot defined here, filled later. Structure is fixed; some numbers are tunable.

---

## 1. Power Curve — Bounded (committed)

Flat-ish accuracy; growth via capabilities, not arithmetic (Phase 1). Curve-fit check (numeric sum at three points):

| Point | Key attack sum | Notes |
|---|---|---|
| Level 1 | `L1 + R(trained 1) + attr+3` = **+5** | |
| Level 10 | `L3 + R(master 3) + attr+5 + potency+1` = **+12** | |
| Level 20 | `L6 + R(legendary 4) + attr+6 + potency+3` = **+19** | optimization ceiling; **+16 without potency** (inside Phase 1 budget) |

The level term still cancels on-level (T2 holds); all accuracy above the baseline comes from **choices and rewards** (attribute investment, rank, gear), never automatic level scaling. **Gate-A levers** if the +19 ceiling proves too sharp: attribute cap (+6 vs +5) and whether a key attack may reach legendary.

---

## 2. Advancement Trigger — Pillar-Neutral XP (+ milestone option)

- **Default:** a fixed per-level XP threshold; XP is awarded for **overcoming any challenge by its difficulty** — a tense negotiation, a slicing gauntlet, or an exploration crisis pays the same as a combat encounter of equal difficulty.
- **Incentive audit:** because XP is pillar-neutral, the reward loop reinforces *both* first-class pillars (combat **and** social). Kills are not privileged.
- **Milestone** is offered as a first-class toggle (GM levels the party at story beats; zero bookkeeping, party stays synced).
- Exact XP values and per-difficulty awards: *(Gate A; the structure is "fixed threshold, difficulty-priced, pillar-neutral.")*

---

## 3. The No-Dead-Levels Chassis (resolves Pillar 4)

**The floor: every level 1–20 grants at least one feat or feature.** Adopts the proven PF2E cadence (ORC-licensed).

| Channel | Levels granted |
|---|---|
| **Species feat** | 1, 5, 9, 13, 17 |
| **Class feat** | 2, 4, 6, 8, 10, 12, 14, 16, 18, 20 |
| **Skill feat** | 2, 4, 6, 8, 10, 12, 14, 16, 18, 20 |
| **General feat** | 3, 7, 11, 15, 19 |
| **Skill increase** (raise one skill one rank) | 3, 5, 7, 9, 11, 13, 15, 17, 19 |
| **Attribute boosts** | 5, 10, 15, 20 |
| **Class features** (the verb + upgrades) | level 1 + class-determined, layered on top |

- Every level has ≥1 feat; most have two or more grants. **No dead levels by construction.**
- Classes (Phase 5) add features *on top* of this floor, so no class can introduce a dead level.
- **Feat-budget separation:** class / skill / general / species feats draw from separate budgets, so combat **class feats** can never cannibalize the **skill feats** that fuel active out-of-combat play (protects Pillar 5 structurally).
- **Feat-tax rule (design-time):** any feat taken by >70% of builds that *can* take it is folded into the baseline and replaced with a real choice.

---

## 4. Attribute Boosts (closes Phase 2 deferral)

At **levels 5, 10, 15, 20**: raise **four different attributes by +1** each (cannot boost the same attribute twice in one event), capped at **+6** (Phase 2 lifetime cap). A key stat reaches +6 by level 15; later boosts spread to secondaries, gently lifting the whole array (reducing late dump penalties) while staying inside the bounded budget.

---

## 5. Proficiency Rank Gates

Rank advancement is gated by level so neither the +1/rank math nor the Phase 1 **rank-gated effects** (the real "expertise feel") arrive too early:

| Rank | Available from |
|---|---|
| Trained | level 1 |
| Expert | level 3 |
| Master | level 7 |
| Legendary | level 15 |

Skill increases (§3) raise one skill per grant within these gates. Core proficiencies (saves, Perception, class DC, weapons, armor, defenses) advance at **class-determined levels** (Phase 5) within these same gates.

---

## 6. Tiers

| Tier | Levels | Fictional scope |
|---|---|---|
| **I — Fringe** | 1–4 | local operators; backwater stakes |
| **II — Sector** | 5–10 | sector-wide reputation; established threats |
| **III — Galactic** | 11–16 | galaxy-spanning conflicts; factions court the party |
| **IV — Legend** | 17–20 | galaxy-shaping legends |

**Tier-breaking capabilities** (gate at the boundary, not before): scaled telekinesis / mind-domination, precognition, personal cloaking, slice-anything, and reliable fast travel / flight. These invalidate lower-tier scenario assumptions, so they unlock consciously by tier.

---

## 7. Resource & Cooldown Model (fully resolves T3)

Abilities are gated by **action economy + time-based cooldowns**, never a per-day pool. Complete frequency vocabulary (every ability is priced in these):

| Frequency | Meaning | Resets |
|---|---|---|
| **At-will** (no marker) | limited only by action cost | — |
| **`[once per turn]`** / `[flourish]` | once on your own turn | each turn |
| **`[once per round]`** | once per round across all turns (most reactions) | top of round |
| **`[cooldown N]`** | unavailable for N rounds after use | after N rounds |
| **`[once per encounter]`** | once per fight/scene | at scene end |
| **Trigger-recharge** | "regain the use when [tactical/fictional condition]" (crit, refocus action, ally falls, etc.) | on the trigger |

- **Forbidden:** any `[once per day]` / per-rest frequency.
- **Full rest** resets `[once per encounter]` abilities and clears fatigue; it refills **nothing else, because nothing is daily**.
- **Encounter-scoped pools are legal:** a resource that builds and is spent within a single scene and **resets at scene end** (e.g., a Force user's rising *Attunement*, a soldier's *Momentum*). Gives crunchy resource-management depth without daily bookkeeping. Specific pools are class content (Phase 5); this section makes the category legal and T3-compliant.
- **Trigger-recharge is the Pillar-5 tool:** it turns resource management into in-the-moment tactical decisions rather than passive daily tracking.

---

## 8. Multiclassing — Archetype Dedication (grafting)

- **Model:** spend **class feats** to take an **Archetype Dedication** — another class's package *or* a concept package (e.g., Bounty Hunter, Force Adept).
- **Commitment rule:** after a Dedication, take **two more feats from that archetype** before taking a *new* Dedication (prevents collecting entry packages).
- **No 1-level dips:** breadth is bought from the existing class-feat budget, not by swapping levels — so a single-class character is **never strictly inferior** to a same-concept multiclass build (they traded combat feats for versatility, a real cost).
- **Limited-Force on-ramp:** a "Force Adept" (or similar) archetype lets a non-Force class acquire a few minor powers as a spendable choice — the structural mechanism that makes the "any party mix" power band work without a class wall.

---

## 9. End-Game (cap = 20)

Designed to function at cap, not extrapolated:

- **Save DCs vs saves:** both track the bounded spine, so there is **no high-level save-or-lose blowout** (a signature unbounded-d20 failure that bounded accuracy structurally prevents).
- **HP vs damage (slog risk):** the one cap-level risk — HP scales every level, so damage must keep pace via damage dice (Phase 1 §5) + class scaling. *(Flagged for Phase 7 creatures + Gate A.)*
- **Tier-breakers** gated per Tier IV (§6).
- **Post-20:** out of scope for the framework — optional horizontal "legendary boons," or the campaign concludes. No numeric extrapolation past 20.

---

## 10. Exit-Gate Checklist (per roadmap)

- [x] Advancement trigger chosen (pillar-neutral XP + milestone); incentive audit passed against pillars.
- [x] Power curve shape chosen (bounded); numeric sum checked at L1/mid/cap vs the modifier-spread budget (§1).
- [x] No dead levels: every level has a feat or feature (§3).
- [x] Tiers named; tier-breaking capabilities consciously gated (§6).
- [x] Growth channels mapped on one table and staggered; attribute-boost levels are intentional tier spikes (§3–4).
- [x] Feat-tax rule stated (>70% pick-rate → fold into baseline) (§3).
- [x] Multiclass model decided (Archetype Dedication); 1-level-dip dominance designed out (§8).
- [x] Cap-level math addressed, not extrapolated; the three classic break-modes (save-DC runaway, HP/damage slog, tier-breakers) each have a stated answer (§9).
- [x] **T3 fully formalized:** complete cooldown vocabulary + encounter-pool category, daily frequencies forbidden (§7).
- [x] **Phase 2 deferral closed:** attribute-boost schedule defined (§4).

## 11. Carried Forward (open items for later phases)

- **Class HP values, key attributes, per-class proficiency-advancement levels, class features/verbs, specific cooldowns & encounter pools, archetype packages** → Phase 5.
- **Skill-feat / general-feat / species-feat content** → respective content phases.
- **XP threshold & per-difficulty award values, attribute-cap & legendary-access tuning** → Gate A.
- **HP-vs-damage TTK validation** → Phase 7 + Gate A.

# Shared Force Toolkit — Disciplines & Powers (Phase 8)

**Status:** Structure ratified (six schools, tradition-split, economy, portability). **Balance pass complete** (`ttrpg-balance-analysis`, 2026-06-16): structural fixes (§4 control-authoring rule, §5 hard-control `[once per minute]` gate + corrected action-granting rule + spec-bug fixes) **and** the per-power math rebalance (§3.1 scaling conventions + §3.2 applied fixes) are done. Remaining: the prose rules-writing pass (§7).
**Date:** 2026-06-15
**Type:** Content design. Built by reading the prior-project **Power** table (55 powers) for *patterns and thematic scaffolding* — **mapped, not ported** — under our bounded system (three-action economy, four-degree success, Attunement economy, Tier gates).
**Upstream:** [Phase 5 — Class Design & Force](2026-06-13-phase5-class-design-and-force.md) (amended: 5 disciplines → 6 schools), [Phase 3 — Progression Chassis](2026-06-13-phase3-progression-chassis.md) (Tier gates §6, resource model §7), [Class Roster](2026-06-15-class-roster-sketch.md) (Force-design principle §3), [Sentinel §4.1](2026-06-15-class-sentinel.md) (don't class-lock iconic powers).

---

## 1. The Toolkit Principle

A Force class's **exclusive** claim is its **verb-framework** (Guardian = blade-flow/Forms, Consular = deep-Manifest, Sentinel = the Premonition reaction-engine). **Iconic Force powers are a shared, portable toolkit** — discipline/feat-gated, acquired with feats, applied *through* each class's framework. No power is class-locked. (Force-design principle, [roster §3](2026-06-15-class-roster-sketch.md) / [Sentinel §4.1](2026-06-15-class-sentinel.md).)

Every power carries the **`[Force]`** trait, exactly one **school** sub-trait (§2), and any number of **mechanical tags** (§4).

---

## 2. The Six Schools — Tradition-Split

The schools are the classic Legends **Jedi triad** mirrored by a **Sith triad**. The grouping is **thematic origin + emphasis, not a hard access wall** — access is feat-gated like everything else, and the cross-cutting **`[dark]`** trait (§4) flags individually-corrupting powers (hook for a future corruption subsystem). This **revises the Phase-5 lock** (5 disciplines → 6 schools); the old names map below.

| Tradition | School | Aptitude | Was (Phase 5) |
|---|---|---|---|
| **Jedi** | **Control** | self-mastery; energy control & defense (barrier, absorb, reflect, cloak) | *(Battle, defensive half)* |
| **Jedi** | **Sense** | precognition, perception, foresight | Sense |
| **Jedi** | **Alter** | kinetic manipulation — move/lift/throw/crush/fly | Telekinesis |
| **Sith** | **Body** | augmenting the flesh — vitality, healing, life-drain, defying death | Vitality |
| **Sith** | **Mind** | domination of others — influence, fear, control, memory | Influence |
| **Sith** | **Offense** | raw destruction — energy, lightning, annihilation | *(Battle, offensive half)* |

**Tradition is emphasis, not a moral wall:** the Body school holds both light healing (Vital Transfer) and dark drain (Drain Life `[dark]`); Mind holds the benign Jedi mind-trick and the coercive Dominate `[dark]`. The `[dark]` trait — not the school — marks corruption.

---

## 3. The Power Roster (mapped from the Power table)

Powers grouped by school and **Attunement cost tier** (§5). Each power's **min level = its Tier gate** (Power-table Level field 1/5/9/13/17 ≈ Tiers I–IV, [Phase 3 §6](2026-06-13-phase3-progression-chassis.md)), so the **Greater** tier-breakers self-gate to Tiers III–IV. `⟳` = reaction. `⊘` = **`[once per minute]`** (hard-control balance gate, §5). `[dark]` flagged inline.

### Jedi — Control *(self-mastery / energy defense)*
| Power | Lvl | Cost | Action | Effect (mapped) |
|---|---|---|---|---|
| **Breath Control** | 1 | 0 | 1 | Hold breath / +status vs inhaled & suffocation |
| **Battle Focus** | 1 | 0 | 1 | Re-save vs one fear effect; clear the mind |
| **Deflect** ⟳ | 1 | 0 | ⟳ | **+2 circ AC** vs a triggering **ranged energy** attack (req. wielding a lightsaber); a deflected miss is batted aside. *Push:* redirect a deflected bolt at an adjacent foe, **or** Deflect for an adjacent ally instead. |
| **Force Barrier** | 1 | 1 | 1 | Resistance (phys/energy) until next turn |
| **Energy Absorption** ⟳ | 5 | 2 | ⟳ | Resist a triggering energy instance |
| **Force Cloak** | 5 | 2 | 2 | Become invisible until you act hostilely |
| **Force Reflection** ⟳ | 9 | 2 | ⟳ | +AC vs ranged energy; on miss, redirect the bolt |
| **Force Immunity** | 13 | 3 | 1 | Immune to one chosen damage type, 1 round |
| **Force Void** | 17 | 3 | 2 | Suppress Force/supernatural in an area |
| **Wall of Light** | 17 | 3 | 2 | Hallowed zone; punishes `[dark]` users |

### Jedi — Sense *(precognition / perception)*
| Power | Lvl | Cost | Action | Effect (mapped) |
|---|---|---|---|---|
| **Sense Life** | 1 | 0 | 1 | Imprecise sense of living creatures in an emanation |
| **Precognitive Parry** ⟳ | 1 | 1 | ⟳ | +circ AC vs a foreseen attack |
| **Guidance of the Force** | 5 | 2 | 1 | Pre-roll a d20 to substitute on your next Strike |
| **Farseeing** | 9 | 2 | 10 min | Remote viewing of a known location/person |
| **Master Precognition** ⟳ | 13 | 3 | ⟳ | Roll initiative twice; party concealed round 1 |
| **True Sight** | 13 | 3 | 1 | See through illusion/invisibility/disguise |
| **Foresight** | 17 | 3 | 2 | Target can't be surprised/off-guard; roll-twice luck |

### Jedi — Alter *(kinetic manipulation)*
| Power | Lvl | Cost | Action | Effect (mapped) |
|---|---|---|---|---|
| **Telekinetic Grasp** | 1 | 0 | 2 | Move/manipulate an unattended object at range |
| **Force Push** | 1 | 1 | 2 | Fort save; push + bludgeoning (cone via Push) |
| **Force Hold** ⊘ | 5 | 2 | 2 | Fort save; slow/restrain/paralyze `[incap]` |
| **Kinetic Slam** | 5 | 2 | 2 | Reflex save; lift-and-slam, prone + stun |
| **Saber Throw** | 9 | 2 | 2 | Hurl saber, multi-target ricochet, returns |
| **Telekinetic Flight** | 9 | 2 | 2 | Fly Speed for a duration |
| **Force Wave** | 9 | 3 | 2 | Cone; bludgeon + knockback (basic Fort) |
| **Telekinetic Cataclysm** | 13 | 3 | 3 | Burst; implode terrain (basic Reflex) |
| **Telekinetic Singularity** | 17 | 3 | 3 | Gravity well; pull + crush `[force]` |
| **Kinetic Bombardment** | 17 | 3 | 3 | Orbital/debris artillery strike |

### Sith — Body *(augmenting the flesh)*
| Power | Lvl | Cost | Action | Effect (mapped) |
|---|---|---|---|---|
| **Force Surge** | 1 | 0 | 1 | Stride ignoring difficult terrain, +Speed |
| **Vital Transfer** | 1 | 2 | 2 | Heal target; you take unpreventable HP cost |
| **Drain Life** `[dark]` | 1 | 2 | 2 | Fort save; void damage, heal self |
| **Force Celerity** | 5 | 2 | 1 | Quickened (Stride/Step); fatigued after |
| **Force Valor** | 5 | 2 | 2 | Allies gain temp HP + vs-fear status |
| **Force Stasis** ⊘ | 9 | 3 | 2 | Fort save; slow/paralyze `[incap]` |
| **Force Revivify** ⟳ | 9 | 3 | ⟳ | Revive a just-dead ally; you take drained |
| **Suspended Animation** | 13 | 3 | 2 | Death-mimicking trance |
| **Force Resurrection** | 13 | 3 | 10 min | Restore the ≤3-day dead; heavy drained cost |
| **Force Enlightenment** | 17 | 3 | 1 | Regen + condition immunities + save bonus |
| **Transfer Essence** `[dark]` ⟳ | 17 | 3 | ⟳ | Cheat death into a vessel/possession |

### Sith — Mind *(domination of others)*
| Power | Lvl | Cost | Action | Effect (mapped) |
|---|---|---|---|---|
| **Mind Trick** | 1 | 1 | 2 | Will save; fascinate/suggest `[incap]` |
| **Force Fear** | 1 | 2 | 2 | Will save; frightened, escalates `[fear]` |
| **Force Disruption** | 5 | 2 | 1 | Will save; cut concentrate/Force actions |
| **Mind Probe** | 5 | 2 | 2 | Will save; extract a truthful answer |
| **Dominate Mind** `[dark]` ⊘ | 9 | 3 | 2 | Will save; control 1 min `[incap]` |
| **Mass Mind Trick** ⊘ | 9 | 3 | 3 | Area Will save; confuse/control 1 round |
| **Sever Force** `[dark]` | 13 | 3 | 2 | Will save; cut off Force use `[curse]` |
| **Mind Wipe** | 13 | 3 | 1 min | Erase/rewrite memory |
| **Mind Fracture** `[dark]` ⊘ | 17 | 3 | 2 | Will save; shatter the psyche (crit-fail re-pegged, §4) |

### Sith — Offense *(raw destruction)*
| Power | Lvl | Cost | Action | Effect (mapped) |
|---|---|---|---|---|
| **Force Shock** | 1 | 1 | 2 | Ranged Force Strike; electricity |
| **Force Choke** ⊘ | 5 | 2 | 2 | Fort save; bludgeon + grab, Sustain |
| **Force Lightning** | 5 | 2 | 2 | Cone; electricity (basic Reflex) |
| **Ionize** | 5 | 2 | 2 | Tech attack; ion vs constructs/powered armor |
| **Chain Lightning** | 9 | 3 | 2 | Arcs foe-to-foe, decaying dice |
| **Force Storm** `[dark]` | 13 | 3 | 3 | Sustained electricity cylinder |
| **Death Field** `[dark]` | 13 | 3 | 2 | Emanation; void damage, heal self |
| **Force Destruction** | 17 | 3 | 2 | Burst/line; force + fire, disintegrate |

### 3.1 Scaling & Re-Peg Conventions (math rebalance, 2026-06-16)

These uniform rules re-tune all 55 imported powers to our bounded system at once; per-power prose adopts them in the rules-writing phase.

- **Breakpoint re-peg (one substitution fixes the table).** Every imported *"+Nd_ / value increase at 4th / 12th / 19th level"* reads as **our Tier boundaries — 5th / 11th / 17th** ([Phase 3 §6](2026-06-13-phase3-progression-chassis.md)). The prior breakpoints already sat ~on our Tiers, so this is a clean shift, not a redesign.
- **Damage dice (auto-scaling, bounded).** A damage power starts at its access-Tier **base dice** and gains **+1 die at each later Tier boundary (L5/L11/L17)**. A Tier-I power therefore arcs **1→4 dice** across the campaign — matching the weapon dice curve (Phase 1) — so a low-level power stays relevant without re-selection ([Phase 5](2026-06-13-phase5-class-design-and-force.md)). Higher-Tier powers start with more base dice (fewer boundaries remain), the standard "higher-rank-starts-bigger" shape.
  - **Die size by delivery:** single-target attack-roll = **d8** (e.g. Force Shock 1d8→4d8); single-target / cone save = **d6**; persistent & special left per-power.
  - **No attribute added to Force damage.** This is the deliberate clamp that keeps damage powers *at or below* the weapon baseline: a melee Strike adds its attribute (and costs 0 Attunement), so a Force damage power buys **range / area / save-targeting**, never raw DPR above a weapon. (Verified on-curve in the balance pass.)
- **Save DCs are not per-power.** All powers roll against the caster's **Force DC = 10 + L + R(prof) + key attr** (the bounded spine), so there is nothing to tune per power; the four-degree *effects* are governed by §4.
- **Flat values key to the Level term `L`** (`1 + level//4`, range 1–6): **Force Barrier** resistance = **2 + L** (3 → 8); **Force Valor** temp HP re-pegs to its Tier breakpoints (**10 / 15 / 20** at Tiers II / III / IV). Resistance/temp-HP stay below the damage curve so they soak, never negate.

### 3.2 Applied Fixes (the powers whose printed numbers broke)

- **Crit-fail re-pegs (§4 control rule — no combat-removal / no death):**
  - **Force Stasis** — was crit-fail *paralyzed 4 rounds*. Now: success slowed 1 (1 rd) · failure stunned 1 + slowed 1 · **crit-fail paralyzed 1 round** (end-of-turn save). Escalation by *condition*, not multi-round removal.
  - **Mind Fracture** — was crit-fail *dies instantly*. Now: failure confused 1 min + mental dmg · **crit-fail stunned 3 + confused + max mental dmg** (lethal *only* via ordinary HP, never auto-kill).
- **Number-Push → effect-Push conversions (Break 5):**
  - **Force Lightning** — was Push *+10 ft cone*. Now: Push = targets that fail are **off-guard** until your next turn.
  - **Telekinetic Flight** — was Push *+10 ft fly Speed*. Now: Push = your flight **ignores reactions** triggered by movement.
  - **Chain Lightning** — was Push *delay dice decay*. Now: Push = a creature that **critically fails is stunned 1**.
  - **Force Barrier** — was Push *Sustained, resist **all** types*. Now: Push = you may **Sustain** it (up to 1 min) and **Step** when an attack is reduced — resistance **stays physical/energy** (drop the blanket all-types soak).

---

## 4. Mechanical Tags (cross-cutting, not schools)

Carried from the table as rules-descriptors, orthogonal to school:
- **`[dark]`** — corrupting power; "more potent at a cost." Hook for the deferred corruption subsystem ([Phase 5 §2 light/dark note](2026-06-13-phase5-class-design-and-force.md)). Marks the genuinely Sith applications regardless of school.
- **`[incapacitation]`** — the standard incap rules (a higher-level target steps the result one better) apply to hard control (Hold, Dominate, Mass Mind Trick, Stasis). **Control-power authoring rule (four-degree discipline):** on a control power, **critical failure escalates the failure effect** — a worse condition or a longer (by our standard durations) effect — but **never removes a creature from the fight outright or kills it.** This re-pegs imported crit-fails (e.g., the prior Force Stasis "paralyzed 4 rounds" and Mind Fracture "dies instantly") to our [four-degree success](2026-06-13-phase1-core-mechanic-and-traits.md) norm. *(General rule; also belongs in the Phase-1 degrees spec — flagged in §7.)*
- **`[fear]` / `[emotion]` / `[mental]`** — interact with immunities and the relevant defenses.
- **`[healing]`, `[fortune]`/`[misfortune]`, `[electricity]`/`[void]`/`[force]`, `[curse]`, `[light]`** — damage-type / effect descriptors.

---

## 5. Economy — Attunement Cost Tiers (honors F6/F7 lock)

Costs use the locked pricing **0 / 1–2 / 3** ([Phase 5 §2.2](2026-06-13-phase5-class-design-and-force.md), playtest F6/F7). Pool = `2 + L` (L = `1 + level//4`); refuel via **Center** (1 action, +2). The economy rule (F3): *every Force effect with combat impact costs ≥1 Attunement.*

| Tier | Cost | Role | Gate |
|---|---|---|---|
| **Basic** | **0** | at-will utility floor (Grasp, Sense Life, Breath Control, Force Surge, Battle Focus, **Deflect**) | none (action-only) |
| **Standard** | **1–2** | the save-DC / attack / buff workhorses | level / school access |
| **Greater** | **3** | the tier-breakers (scaled control, mass effects, resurrection, AoE artillery) | **Tier III–IV** ([Phase 3 §6](2026-06-13-phase3-progression-chassis.md)) |

**Second gate on hard control (balance pass, Break 1).** Attunement cost alone can't separate a damage AoE from a fight-ending control effect at the same price. So **hard control / mass action-denial powers also carry `[once per minute]`** (≈ once per fight) so the per-encounter pool can never be dumped into *repeated* save-or-lose. This applies to: **Force Hold, Force Stasis, Force Choke, Dominate Mind, Mass Mind Trick, Mind Fracture.** (Soft control — frightened/fascinated, e.g. Force Fear, Mind Trick — is exempt; Mind Trick further self-limits via its built-in 1-hour target immunity.) Pure damage AoEs stay cost-only.

**Action-granting rule (balance pass, Break 2 — corrected).** Action-granting is priced by *what the granted action can do × how many actors get it*, **not by duration.** A **movement-only, self** grant (e.g. **Force Celerity** — quickened Stride/Step, 1 minute) has near-zero tempo value per action and is fine at long duration (a mobility buff). A grant whose action can **Strike or cast**, **or** that affects **multiple actors** (mass haste), explodes in value and must be clamped — **Sustained or short duration, and/or `[once per minute]`, never a free minute of party-wide value-actions.**

**Mind Trick** (Standard, 1 Att) and **Battle Focus** (Basic, 0 Att) corrections (Break 6): Mind Trick is `[incapacitation]` action-denial and is **not** a 0-cost at-will power (it is Standard). Battle Focus stays at-will for the *re-save vs fear* (reactive, self-limiting), but its temp-HP **Push** is gated so it can't be used as free out-of-combat sustain-fishing.

**Push = +1 Attunement.** Every power's prior-project **`Connected:`** clause becomes its **Push upgrade** — and Push **adds an *effect*, not a number** (locked Push design). **Audit (Break 5):** several imported Connected clauses are *number*-bumps and must be converted or folded into level scaling during the per-power rewrite — flagged: **Force Lightning** (+10 ft cone), **Telekinetic Flight** (+10 ft fly Speed), **Chain Lightning** (delayed dice decay), and **Force Barrier** (Sustained, resist *all* types — re-cost or keep typed).

---

## 6. Acquisition & Portability

- **Powers are bought with feats**, chosen from schools the character can access — *not* granted by class identity. (Generalizes the "Guardian Mastery makes Forms portable" pattern.)
- **Class frameworks set starting allotment + emphasis, not exclusivity:**
  - **Consular (Manifest):** broadest access + **Mandates** = deep school-emphases (Telekinesis→Alter, Visions→Sense, Life→Body, Dominance→Mind). [Subclass sketch §2](2026-06-15-subclass-roster-sketch.md).
  - **Guardian (Blade-Flow):** leans **Alter / Control / Offense**; **masters Deflect** (the Guardian Mastery clause upgrades it — bigger AC swing, applies to melee via Soresu); [Forms](2026-06-18-lightsaber-forms.md) are the saber-channel layer on top. **Deflect is the genre-flip counter to the [Reactive Shot](2026-06-13-phase1-core-mechanic-and-traits.md) — the structural reason melee Force users can close on gunners.**
  - **Sentinel (Premonition):** leans **Sense**; spends Attunement on *reactions* (Precognitive Parry, Energy Absorption, Force Reflection are natural fits).
  - **Force Adept archetype** ([Phase 3 §8](2026-06-13-phase3-progression-chassis.md)): the limited on-ramp — a non-Force class buys a few Basic/Standard powers.
- **`[incapacitation]` + Tier gates** keep the save-or-lose powers (Dominate, Stasis, Mass Mind Trick) honest at the bounded spine.

---

## 7. Carried Forward

- **Balance pass — DONE (2026-06-16).** Verdict: economy skeleton sound; no-daily model and bounded-accuracy-for-damage intact (offensive single-target tracks the weapon dice curve). Structural fixes applied in-spec. Remaining items pushed to the per-power rewrite below.
- **Math rebalance — DONE (2026-06-16):** scaling/breakpoint re-peg, damage-dice curve, flat-value keying, and the specific crit-fail + number-Push fixes are captured as uniform conventions (§3.1) and applied fixes (§3.2).
- **Rules-writing (prose) pass — remaining:** turn each power into a full entry (exact dice per §3.1, ranges, all four degrees, Push text) in the final format. This is content authoring, not balance.
- **Promote the control-authoring rule** (§4) into the [Phase-1 four-degree-success spec](2026-06-13-phase1-core-mechanic-and-traits.md) so it governs all content, not just Force powers.
- **Content-curation (deferred, not a math fix):** hard-control *density* (6 powers) — revisit during the rewrite; `[once per minute]` already taxes repeated use.
- **School-access rules** per class/archetype (how many powers known, which schools, at what levels).
- **Corruption subsystem** (`[dark]` consequences) — still deferred.
- **Reconcile** the Consular Mandate sketch and Phase-5 §3 discipline references to the 6-school names.

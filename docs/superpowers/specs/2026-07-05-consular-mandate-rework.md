# Consular Mandate Rework — Mechanics over Grants

**Status:** Approved (design), pending implementation
**Date:** 2026-07-05
**Type:** Subclass restructure. Reworks the six Consular Mandates so power grants are consolidated into a level-gated list in the L1 entry and every feature slot (1/3/7/11/15/19) holds a real mechanic.
**Upstream:** [Class — Consular](2026-06-19-class-consular.md) (§5 is superseded by this spec), [Phase 4 social/intrigue engine](2026-06-13-phase4-social-intrigue-engine.md), [Force toolkit](2026-06-15-shared-force-toolkit.md).
**Downstream:** `docs/player-core/classes/consular.md` §Consular Mandates (and two adjacent feat fixes, §6 below).

---

## 1. Problem & Principles

Of the 36 Mandate features, ~25 were "You add **X** to your repertoire" with a thin rider or nothing at all. Granting powers is good, but it shouldn't be the bulk of what a subclass does — a grant is ammunition for the class verb (Manifest), not a modulation of it.

**The rework's skeleton (every Mandate):**

1. **Flavor line** — unchanged.
2. **L1 core mechanic** — one named, coherent engine. Grab-bag L1s are trimmed to a single mechanic; trimmed effects die or migrate to a later slot.
3. **Mandate Powers** — one level-gated list in the L1 entry: *"You add the following powers to your repertoire when you reach the listed level."* Same powers and levels as before; they still cost Attunement to Manifest. (The subclass-grants-override-level-gate convention, stated once.)
4. **Features at 3/7/11/15/19** — pure mechanics, no grant text. Per Mandate: two or three escalations of the L1 engine, one or two out-of-combat features placed **organically**, and an L19 apex that is a mechanic, never a grant.

**Out-of-combat distribution (organic, not fixed-slot):** Dominance is social-heavy (two features, including the game's first class-specific social verb — paying down [Phase 4 §13](2026-06-13-phase4-social-intrigue-engine.md)'s carried-forward debt); Visions gets social recon; Serenity gets the Composure/Defuse angle; Vitality gets downtime recovery; Telekinesis keeps exploration utility (Heavy Lifter); Destruction stays pure combat — the Mandate for players who opt out of the second pillar.

*(All numbers Gate-A unless noted.)*

---

## 2. The Six Mandates

### 2.1 Mandate of Telekinesis

**Powers:** Force Push (1st) · Kinetic Slam (7th) · Force Hold (11th) · Force Wave (15th) · Telekinetic Singularity (19th).

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Telekinetic Adept** | *(engine, unchanged)* When you deal damage with an Alter power or Telekinetic Impact, push the target 5 ft. |
| 3 | **Heavy Lifter** | *(kept — the exploration slot)* Double-Bulk Telekinetic Grasp; +5 ft forced movement. |
| 7 | **Kinetic Crush** | A creature you force-move is off-guard until the start of your next turn, **and** forcing it into an obstacle or another creature deals bludgeoning damage equal to your level. |
| 11 | **Crushing Grip** | *(kept)* Once per round, a creature attempting to escape or end one of your Alter effects rolls twice, takes the worse (misfortune). |
| 15 | **Gravity Well** | `[reaction]` When a creature within 30 ft begins to move: Fortitude vs your Class DC or its movement is halved and you redirect its first 10 ft. The old "drive upward/over an edge" text stays in this feature (player-core has no general forced-movement rules chapter yet to receive it). |
| 19 | **Singularity** *(apex)* | Once per round, apply an Alter power's Push upgrade free after seeing the result; your Telekinetic Adept push increases to 10 ft and, once per round, can also knock the target prone. |

### 2.2 Mandate of Visions

Identity guard: the **Sentinel** owns *personal* reactive foresight (Premonition); the Visions Consular is the *squad's* seer — foresight handed out.

**Powers:** Precognitive Parry (1st) · Guidance of the Force (7th) · Master Precognition (11th) · True Sight (15th) · Foresight (19th).

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Seer** | *(trimmed)* You can't be made off-guard by creatures of your level or lower; +1 status to initiative. (The +1 Perception rider dies — the chassis already advances Perception.) |
| 3 | **Forewarned** | *(kept)* When you roll initiative, allies within 30 ft can't be made off-guard during the first round. |
| 7 | **Read the Currents** *(social)* | You can Read the Room using The Force; on a success you also learn one of the opposing side's Levers or Guards. Once per scene, the GM tells you which action the opponent will take on its next turn. |
| 11 | **Battle Precognition** | `[reaction]` When an ally you can see attempts a saving throw, they roll twice and take the better result (fortune). |
| 15 | **Peerless Seer** | No creature can make you off-guard; Forewarned also grants those allies your +1 status to initiative. |
| 19 | **Foresight** *(apex)* | You are permanently under the effect of your Foresight power, no Attunement or Sustain required. |

### 2.3 Mandate of Serenity

**Powers:** Force Barrier (1st) · Energy Absorption (3rd) · Battle Focus (7th) · Force Cloak (11th) · Force Reflection (15th) · Wall of Light (19th).

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Eye of Calm** | *(engine, unchanged)* When you Manifest a Control power, gain temp HP = your level until the start of your next turn. |
| 3 | **Tutaminis** | *(kept)* Energy resistance you gain from Control powers +2. |
| 7 | **Becalming Presence** *(social)* | You can Defuse using The Force, and the first Composure loss your side takes each exchange is reduced by 1. |
| 11 | **Unclouded Mind** | *(moved from L7, deepened)* While you have ≥1 Attunement, +1 status vs fear and mental; Eye of Calm also triggers when you Center. (The old Veil rider dies; Force Cloak stands alone in the list.) |
| 15 | **Aegis** | *(promoted from rider)* Your defensive Control powers can target an ally within 30 ft instead of yourself; when they do, Eye of Calm's temp HP goes to that ally. |
| 19 | **Still Point** *(apex)* | *(renamed from Sanctuary)* `[3 actions]`, once per day: 20-ft emanation, Sustained up to 1 minute; allies inside gain temp HP = your level at the start of each of your turns and share your Unclouded Mind bonus. |

### 2.4 Mandate of Vitality

**Powers:** Vital Transfer (1st) · Force Surge (3rd) · Force Valor (7th) · Force Revivify (11th) · Force Enlightenment (15th) · Force Resurrection (19th).

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Life-Giver** | *(engine, unchanged)* When a Force power you Manifest restores HP, the target also gains temp HP = your level. |
| 3 | **Surge** | *(kept)* +10-ft status to Speed and ignore difficult terrain while a Body power is active. |
| 7 | **Vigor** | *(kept)* When you restore HP, also reduce one condition affecting the target by 1. |
| 11 | **Wellspring** *(downtime)* | When the party rests under your care, each ally recovers additional HP = your level; once per day per creature, attempt a The Force check to treat a poison or disease as expert medical care. |
| 15 | **Overflowing Life** | Once per round when you restore HP with a Force power, one other creature within 10 ft of the target regains half that amount (Life-Giver applies to it too). |
| 19 | **Fountain of Life** *(apex)* | Once per round, a power that restores HP costs 1 less Attunement; Life-Giver's temp HP lasts until expended. *(Gate-A watch: stacking with the One with the Force capstone feat at L20.)* |

### 2.5 Mandate of Dominance

**Powers:** Mind Trick (1st) · Force Fear (3rd) · Mind Probe and Force Disruption (7th) · Dominate Mind (11th) · Mass Mind Trick (15th) · Mind Fracture and Sever Force (19th).

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Mind's Eye** | *(unified)* You sense surface emotions within 30 ft (imprecise); +1 status to Deception, Diplomacy, and Intimidation against creatures whose emotions you sense. |
| 3 | **Fearmonger** | *(kept)* Frightened you impose with Force powers doesn't decrease at the end of the target's first turn. |
| 7 | **Whispered Doubt** *(social verb)* | `[1 action]` in a social encounter: The Force check vs the opponent's Will DC. Success: opponent is Off-Balance. Crit success: also Resolve −1. Crit failure: it feels the intrusion and gains a Guard against your next appeal. *(Named to dodge the Insidious Suggestion feat. The first class-specific social verb — Phase 4 §13.)* |
| 11 | **Puppeteer** | Once per round, when a creature critically fails a save vs your Mind power, it immediately spends its reaction to Stride or Strike as you direct. |
| 15 | **Looming Will** *(social)* | When a social encounter begins, choose: opposing side's starting Resolve −2, or your side's starting Composure +2. |
| 19 | **Shatter Will** *(apex)* | Frequency once per minute: when a creature fails (not critically fails) a save vs your Mind power, it critically fails instead. Incapacitation limits still apply. |

### 2.6 Mandate of Destruction

**Powers:** Force Shock (1st) · Force Lightning (7th) · Chain Lightning (11th) · Force Storm (15th) · Force Destruction (19th).

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Force Artillery** | *(engine, upgraded to a named condition — decided 2026-07-05)* When you deal damage to a creature with an Offense power or Telekinetic Impact, it is **clumsy 1** until the start of your next turn. An area power applies this to **every** creature it damages. |
| 3 | **Overload** | *(kept)* Once per turn, apply an Offense power's Push upgrade free. (Feat collision already resolved — the feat is *Overcharge*.) |
| 7 | **Arc Lightning** | *(kept, substrate fix)* Single-target Offense powers arc to a second creature within 10 ft for splash damage equal to **your level** (was Level Bonus — forbidden peg). |
| 11 | **Storm-Caller** | *(kept)* Your cones and lines increase one size step. |
| 15 | **Scoured Ground** | Your area Offense powers leave the area hazardous until the start of your next turn: creatures that enter or end their turn there take damage equal to your level (the power's damage type). |
| 19 | **Annihilation** *(apex)* | Once per round, when your Offense power reduces a creature to 0 HP, you regain 1 Attunement. |

**Force Artillery balance note (clumsy 1 vs the old −1 circumstance AC):** the penalty-type swap is the real change — status stacks with off-guard (the old version was dead against flanked targets) and clumsy's Reflex coverage feeds the Mandate's own area powers (rolling +5% effective DC). Assessed at ~1.5–2× the old rider's typical-case value; inside the L1 Mandate bracket (vs the temp-HP engines). **Gate-A watch:** the area-application case (mass clumsy ahead of the next barrage). Clumsy already exists in the conditions appendix — no closed-index work.

---

## 3. Cross-Mandate Parity

The six columns answer "how do you Manifest?" six ways, on one grammar: **L1** engine · **L3** early escalation · **L7** mode-defining feature (positioning / recon / Defuse / condition-healing / the social verb / the arc) · **L11** the engine hooks a class system (reactions, the Center loop, rest, crit-fail exploitation) · **L15** the engine goes wide (out-of-turn control, total foresight, ally-targeting, mass heal, meter-shaping, zone denial) · **L19** an economy or rules-bending apex, never a grant.

---

## 4. Design Rationale (why this shape)

- **Grants are ammunition, not identity.** A subclass must modulate the class verb; the gated list keeps the ammunition without spending feature slots on it.
- **The Consular is action-saturated** (Manifest + Attunement decisions), so most new features bend how the school's powers play (riders, economy, targets, reactions) rather than adding competing standard actions. The exceptions are deliberate: Whispered Doubt lives in the social economy, Gravity Well and Battle Precognition are reactions (the Consular is reaction-light).
- **Engine recurrence** (L1 mechanic visibly inside the 11/15/19 features) is what makes escalation feel like growth rather than a list of presents.

---

## 5. Balance Watch (Gate-A)

- Force Artillery area application (§2.6 note).
- Fountain of Life + One with the Force stacking at L20 (near-free healing loop).
- Looming Will's ±2 meter shift vs Gate-A meter sizing (Resolve ≈ 8 standard — a 25% head start; may need to scale with meter size).
- Reaction additions (Gravity Well, Battle Precognition) vs the flagged reaction-stacking budget — both are once-per-round by nature of being reactions; fine unless archetypes stack more.

---

## 6. Implementation Notes

- **Files:** update [class spec §5](2026-06-19-class-consular.md) (point it at this spec or inline the new tables) and `docs/player-core/classes/consular.md` §Consular Mandates.
- **Adjacent fixes in the same pass:** *Crushing Grasp* feat damage pegs to Level Bonus → level (same forbidden peg as Arc Lightning); verify *Shared Foresight* feat (8) doesn't duplicate the new Battle Precognition reaction — differentiate (attacks/checks vs saves) or rename if needed.
- **Closed indexes:** clumsy and off-guard already have condition entries; Off-Balance is a Phase 4 social condition — confirm it has a home (conditions appendix or the social chapter) when Whispered Doubt lands in player-core.
- **Playtest doc references** to old feature names (e.g., Kinetic Barrage) describe a superseded draft; no retro-edit needed.
- Phase 4 §13's "class-specific social verbs" debt: first payment (Whispered Doubt); note it there when convenient.

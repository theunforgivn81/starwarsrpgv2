# Class — Sentinel *(in progress)*

**Status:** Chassis locked. **Premonition core abilities designed** (§4: responses, Foretell, ✦ features — pending Gate-A). **Subclass development** (§5: Warden/Shadow/Justicar) and **class feats** are the next design step.
**Date:** 2026-06-15
**Type:** Class detail. First class detailed from the [Class Roster](2026-06-15-class-roster-sketch.md) / [Subclass sketch](2026-06-15-subclass-roster-sketch.md).
**Upstream:** [Phase 5 chassis](2026-06-13-phase5-class-design-and-force.md), [Phase 3 progression](2026-06-13-phase3-progression-chassis.md), [Creation Slot Contributions](2026-06-15-creation-slot-contributions.md), [Force subsystem](2026-06-13-phase5-class-design-and-force.md).

---

## 1. Identity

*A watchful Force-adept who sees the blow before it lands.* **Key attribute: Wisdom. HP 8.** The Sentinel's game is played **off its own turn** — its verb, **Premonition**, is a reactive/precognitive engine (dodge, counter, redirect, warn allies). It is the table's reaction specialist, distinct from the Guardian (proactive blade) and Consular (proactive powers). Defense comes from **anticipation** (saves + reactions), not toughness.

**Proficiency signature: Perception** — the Sentinel is the galaxy's keenest watcher and the only class to reach **Legendary Perception** (it also fuels Premonition's triggers).

---

## 2. Initial Proficiencies (Level 1)

| Category | Rank | Notes |
|---|---|---|
| **Perception** | **Expert** | the signature line |
| **Reflex** | **Expert** | precognitive dodge |
| **Will** | **Expert** | disciplined mind |
| **Fortitude** | Trained | the frail save |
| **Class DC** (Force) | Trained | Premonition effects |
| **Weapons** | Trained | simple weapons + **lightsabers** |
| **Defense** | Trained | **unarmored** + **light armor** |
| **Skills** | Trained in **4 + Int modifier** | a perceptive, moderately-skilled class |

Also at L1: gains **Attunement** (the Force resource; pool `2 + L`, [Phase 5 §2.2](2026-06-13-phase5-class-design-and-force.md)) — fuels Premonition (mechanics in §4).

---

## 3. Level Progression (chassis)

Chassis grants per [Phase 3](2026-06-13-phase3-progression-chassis.md) (incl. the new **level-1 class feat**). ✦ = Premonition class feature · ◆ = subclass feature (content → §4/§5).

| Lvl | Class features & chassis grants | Proficiency advances |
|---|---|---|
| 1 | **Premonition** ✦ · **subclass** ◆ · **class feat** · ancestry feat · Attunement | initial profs (§2) |
| 2 | class feat · skill feat | — |
| 3 | general feat · skill increase · ◆ | Class DC → **Expert** |
| 4 | class feat · skill feat | — |
| 5 | ancestry feat · skill increase · attribute boosts · ✦ | Fort → **Expert** · weapons → **Expert** |
| 6 | class feat · skill feat | — |
| 7 | general feat · skill increase · ◆ · **Weapon Specialization** | Perception → **Master** |
| 8 | class feat · skill feat | — |
| 9 | ancestry feat · skill increase | Reflex → **Master** |
| 10 | class feat · skill feat · attribute boosts | — |
| 11 | general feat · skill increase · ◆ | Will → **Master** |
| 12 | class feat · skill feat | — |
| 13 | ancestry feat · skill increase | Class DC → **Master** · armor → **Expert** · weapons → **Master** |
| 14 | class feat · skill feat | — |
| 15 | general feat · skill increase · ◆ · attribute boosts · **Greater Weapon Specialization** | Perception → **Legendary** ✦ |
| 16 | class feat · skill feat | — |
| 17 | ancestry feat · skill increase · ✦ | Fort → **Master** |
| 18 | class feat · skill feat | — |
| 19 | general feat · skill increase · ◆ | — |
| 20 | class feat · skill feat · attribute boosts · **capstone** ✦ | — |

- **Skill increases:** 3/5/7/9/11/13/15/17/19 (raise one skill within the Expert-L3 / Master-L7 / Legendary-L15 gates).
- **Skill feats:** every even level (2–20).
- **No dead levels:** every level grants a feat or feature.
- **Weapon track:** Trained (L1) → **Expert (L5)** → **Master (L13)** — the hybrid-martial cadence (the Sentinel's Counter is a weapon Strike, so it is a gish, not a pure caster). Weapons cap at Master; **Legendary weapons are reserved for dedicated martials/Guardian.**
- **Weapon Specialization** (L7) / **Greater** (L15) are the universal grants ([Phase 3 §3.1](2026-06-13-phase3-progression-chassis.md)); keyed to weapon rank, they are **live from L7** (+2, Expert), rise to **+3** when weapons reach Master at L13, and **Greater** makes it **+6** (Master) at L15. They apply to weapon Strikes including **Counter** — but never to Force-power damage.
- *(Exact advancement levels tunable at Gate A; one Legendary line, Perception — other saves cap at Master.)*

---

## 4. Premonition (the verb) — framework LOCKED; responses & ✦ features designed (2026-06-16)

**The Sentinel's *exclusive* identity is this reactive framework — not ownership of iconic Force powers** (see the Force-design principle, §4.1). The framework:

- **Premonition** `[reaction]` — one flexible reaction with a small menu of **responses** (fast to resolve — one decision, not a flowchart). **Trigger:** a creature you can perceive makes an attack or hostile action against you or an ally within range.
- **Two reactions baseline:** the Sentinel gains a **second reaction each round usable only for Premonition** (so 2 reactions/round — the core-mechanic table-speed budget).
- **Attunement overdrive:** spend **1 Attunement** for **one additional Premonition per round** (hard-capped at +1/round; pool-limited). This is the "out-react everyone" fantasy, *bounded* by the Force economy so it can never lock the table into endless interrupts. **Max 3 reactions/round, and only by spending resources.**
- **Foretell** `[1 action]` — the proactive *own-turn* play (so a reactor isn't bored on its initiative): read the immediate future to empower your next Premonition / mark a foreseen foe.
- **Fuel:** **Attunement** (Force resource, pool `2+L`, refuel via Center). The Sentinel spends Attunement on *reactions*, where the Consular spends it on *powers* — clean trinity differentiation.
- **Development (✦):** L5/L17/L20 deepen the engine (more responses available, overdrive/uses scaling, a capstone apex such as *never surprised / always act first*). **Breadth comes from subclasses (§5), not a pile of at-table reactions.**

### 4.0 Economy reconciliation (applies toolkit F3)

- **Range:** Premonition protects **you or an ally within 30 feet** that you can perceive.
- **The reaction is free; the *response* is what may cost Attunement.** Defensive responses (**Evade, Warn**) cost **0** — the never-gas-out-defensively baseline ([toolkit §5 / F3](2026-06-15-shared-force-toolkit.md)). Offense/debuff responses (**Counter, Foresee**) cost **1 Attunement** (the F3 rule that combat-impact offense/debuff is resourced). This is the snappy decision the framework wants: *defend for free, or spend to punish/disrupt.*
- **Overdrive** (the 3rd Premonition this round): **1 Attunement to unlock the extra reaction**, *plus* the chosen response's cost. (L17 makes the 3rd free.)
- **Foretell costs 0** — it is the reactor's free **proactive baseline** (its Strike-equivalent), not a resourced power.

### 4.2 Responses — the Premonition menu *(mechanism = position / timing / information, never energy/matter/minds; §4.1)*

One response per Premonition; pick on resolution (one decision, not a flowchart).

| Response | Type | Cost | Effect |
|---|---|---|---|
| **Evade** | position, defensive | 0 | **Step** (5 ft, doesn't trigger reactions) before the attack resolves. If the Step takes you out of the attacker's reach/range or into cover, apply that against the triggering attack (it may take the cover penalty or fail to reach you). *Foreknowledge footwork — not a flat AC dodge (that's the Sense toolkit's Precognitive Parry).* |
| **Counter** | timing, offensive | 1 | **`[once per round]`.** Make a single melee or ranged **Strike** against the triggering creature (must be a legal target). You strike into the opening as it commits. **Full accuracy — reaction Strikes are never subject to MAP** ([Phase 1 §4.2](2026-06-13-phase1-core-mechanic-and-traits.md)). |
| **Warn** | information, defensive (ally) | 0 | The ally targeted by the trigger may immediately **Step**, **or** gains a **+2 circumstance bonus** to AC (or the relevant defense) against the triggering effect. *A shouted warning — works against an area effect's edge via the Step.* |

**Niche/dead-zone check:** Evade is best when a square earns cover/breaks reach, dead when cornered; Counter is best when the foe is in range and you have Attunement, dead otherwise; Warn is best shielding a squishy ally from a big hit, dead when solo. None duplicates a toolkit power (deflection, parry, healing, telekinesis, mind influence).

### 4.3 Foretell `[1 action]` `[concentrate]` `[Force]`

Designate one creature you can perceive as **foreseen** until the start of your next turn (cost **0**; the proactive own-turn play). While a creature is foreseen:
- It **can't make you off-guard**, and you gain a **+1 circumstance bonus to AC and saves** against it (you see its moves coming).
- The **next Premonition you trigger off that creature is empowered:** *Evade* → you may **Stride** instead of Step · *Counter* → the Strike treats the target as **off-guard** · *Warn* → the ally gets the Step **and** the +2 (both).

*Foretell gives the reactor a satisfying initiative-turn button and converts foresight into a reactive payoff, without competing for the Attunement that fuels reactions.*

### 4.4 Premonition development (✦)

- **L5 — Widened Sight:** gain a fourth response, **Foresee** *(information, debuff, 1 Att)* — when the trigger creature acts, you call its move: it becomes **off-guard to the next attack made against it** before the start of your next turn. Foretell now affects up to **two** creatures, and a foreseen foe is also **off-guard to you**.
- **L17 — Unclouded Sight (Tier IV):** your **overdrive 3rd Premonition is free** (0 Att; still capped at 3 reactions/round — honors the locked table-speed cap, removing only the resource cost). At the **start of combat** you may Foretell every foe you can perceive for free (no action) — you read the whole battlefield's opening.
- **L20 — Prescience (capstone):** you **can't be surprised** and are **never off-guard** to any creature you can perceive; you and allies within 30 ft gain a **+4 status bonus to initiative**. Once per round, your Premonition may trigger off **any** hostile action a foe takes (not only attacks) — total foresight. *(The "never surprised / always act first" apex; keeps the 3-reaction cap intact — it broadens the* trigger*, not the count.)*

### 4.1 Force-design principle (cross-cutting) — *don't class-lock iconic powers*

A Force class's **exclusive** claim is its **verb-framework**, *not* ownership of iconic Force abilities. **Iconic powers** (deflection, telekinesis, mind influence, healing, precognitive foresight) are **shared Force toolkit** — discipline/feat-gated and **portable** across Force users (like Forms via their "Guardian Mastery" clause). So the Sentinel must **not** absorb e.g. the Guardian's **Deflect** as a Premonition response; if it deflects, it does so via the shared toolkit, as a specialist's *application*, not a class-exclusive grant. *(Recorded also in the [class roster](2026-06-15-class-roster-sketch.md) Force-trinity section.)*

## 5. Subclasses (Premonition forks) — *to be designed next*

On the **1/3/7/11/15/19** cadence. Sketched identities ([subclass roster](2026-06-15-subclass-roster-sketch.md)):
- **Warden** — reactive protector (intercept/redirect attacks meant for allies).
- **Shadow** — reactive ambusher (stealth + counter, then vanish).
- **Justicar** — reactive punisher (precognitive riposte/retaliation).

*(Each steers the open Premonition chassis by adding/shaping **responses**; full features next. Subclass abilities are vetted against §4.1 — they're reactive *applications*, not grabs of iconic shared-toolkit powers.)*

---

## 6. Carried Forward

- ~~**§4 Premonition** mechanics + ✦ development~~ — **DONE (2026-06-16):** responses (Evade/Counter/Warn + Foresee@L5), Foretell, and ✦ features (L5/L17/L20) designed via `ttrpg-ability-design`.
- **§5 subclass** features (L1 + 3/7/11/15/19) — Warden/Shadow/Justicar, the next step (each adds/shapes a response per §4.1).
- **Class feats** list (the Sentinel's own feat options).
- **Gate-A validation** (eHP via saves+reactions, reaction-economy/table-speed check, DPR-equivalent of counters).
- Flavor/description → rules-writing.

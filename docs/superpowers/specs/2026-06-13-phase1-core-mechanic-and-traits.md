# Phase 1 — Core Mechanic & Trait System

**Status:** Approved
**Date:** 2026-06-13
**Roadmap phase:** 1 of 9 — see [build roadmap](../plans/2026-06-13-star-wars-rpg-build-roadmap.md)
**Upstream:** [Design Philosophy](2026-06-13-star-wars-rpg-design-philosophy.md)
**Resolves:** T1 (proficiency math), T2 (four degrees under bounded accuracy), Pillar 1 (bounded participation math). Establishes the trait framework all later phases consume.

> **Note:** Values marked *(Gate A)* are provisional pending balance-analysis calibration once Phase 2 pins attribute ranges. The structure is fixed; some numbers are tunable.

---

## 1. The Resolution Engine

Every check in the game — attack, save, skill, social action — uses one engine:

> **`d20 + Proficiency + Attribute + situational modifiers`**, compared to a **DC**, resolved on a **four-degree** outcome.

The same engine runs combat and social/intrigue (the two first-class pillars share one resolution grammar), so mastery transfers between them.

---

## 2. The Scaling Spine (resolves T1)

### 2.1 Proficiency = Level term + Rank term

| Term | Definition | Range, levels 1–20 |
|---|---|---|
| **Level term (L)** | `1 + (level ÷ 4, rounded down)` | **1 → 6** |
| **Rank term (R)** | Untrained **0** · Trained **1** · Expert **2** · Master **3** · Legendary **4** | **0 → 4** |

`Proficiency = L + R` for **trained or better**. **Untrained = +0 total** (no Level term, no rank — an untrained creature adds only its attribute + situational modifiers). *(Decision A — untrained gets nothing, PF2E-style.)*

- Combat defenses (AC, saves, class/power DCs) are **always at least Trained**; there is no "untrained AC."
- Total check modifier ranges from **+1** (level 1 trained, no attribute) to **+10** proficiency at level 20 legendary; with attributes (key-stat range ~+3→+5, finalized Phase 2) the lifetime spread is roughly **+1 to +15** — inside the d20 engine's healthy spread.

### 2.2 The Level term is symmetric (resolves T2)

A creature of level *N* builds its attacks, AC, save DCs, and saves on the same `L = 1 + (N ÷ 4)`. **When an on-level attacker meets an on-level defender, the Level terms cancel.**

**Consequence (the T2 fix):** on-level hit rate *and* crit rate depend only on rank + attribute + situational differences, which are **level-independent**. Crit frequency is therefore **constant across all 20 levels**; it is driven by build optimization and tactics, never by character level.

This refines the philosophy's "defenses don't scale" into: **defenses scale only by the gentle universal Level term (+5 across the whole campaign); everything that makes an enemy *threatening* — HP, abilities, damage — scales as the philosophy specifies.**

### 2.3 Treadmill decision (explicit)

The Level term is a **deliberately tiny treadmill** (numbers move ~+5 over 20 levels). The real progression is **capabilities** — new actions, rank-gated effects, traits, HP, more powers (Pillar 4, T3). The Level term is kept (rather than removed entirely) for two reasons:

1. **Fixed DCs** (locks, climbs, environmental saves — which do *not* scale) get gentle bounded improvement: a level-20 hero reliably beats what challenged them at level 1, without that content scaling away.
2. **Cross-level encounters stay meaningful**: a level-20 party vs level-5 mooks face a ~+5 gap, not the +30 of unbounded systems — so weak-enemy swarms and mixed-level fights still matter.

### 2.4 Worked crit-stability example

Optimized attacker who is net **+4 ahead** of an on-level defender's AC (the build/attribute/situational edge), at level 1 and level 20:

| | Level 1 | Level 20 |
|---|---|---|
| Attacker mod | L1 + R + attr + edge | L6 + R + attr + edge |
| Defender AC | 10 + L1 + … | 10 + L6 + … |
| **Net margin** | **+4** | **+4** (L cancels) |
| To hit (need) | 6+ → **75%** | 6+ → **75%** |
| Crit by margin (total ≥ DC+10 → need 16+) | **25%** | **25%** |

Identical at both levels. Only the **edge** (build/tactics) moves the numbers — exactly where player agency should live.

---

## 3. Four Degrees of Success (resolves T2 outcome layer)

Compare `d20 + mods` to the DC:

| Outcome | Condition |
|---|---|
| **Critical Success** | Beat the DC by **10 or more** |
| **Success** | Meet or beat the DC (by 0–9) |
| **Failure** | Miss the DC by 1–9 |
| **Critical Failure** | Miss the DC by **10 or more** |

**Natural 20 → step result up one degree. Natural 1 → step result down one degree.** Applied *after* the margin-based degree.

- **Floor (Pillar 1):** a natural 20 always improves the result, so anyone who can succeed can crit, even an underdog who can't reach the +10 margin. Crits never fully vanish.
- **Anti-fumble:** if your margin would *succeed*, a natural 1 drops you only to **Failure**, never Critical Failure. High-skill characters don't catastrophically fumble on bad luck.

**Whiff mitigation:** primarily the three-action economy (a missed Strike is one of three actions, not a wasted turn) plus per-ability degree riders. "Success at a cost" partial outcomes are primarily a Phase 4 *social* tool.

---

## 4. Modifier Architecture

### 4.1 Three bonus/penalty types

| Type | Source | Examples |
|---|---|---|
| **Circumstance** | Positioning / situation | cover, flanking, aid, high ground |
| **Status** | Effects on the creature | buff powers, conditions (frightened), inspiration |
| **Item** | Worn/wielded gear | weapon/armor **potency** (§5) |

**Stacking:** same type does **not** stack (take the best bonus / worst penalty); **different types stack.** Proficiency and attribute are the base, not "bonuses." The **Multiple Attack Penalty is untyped** and stacks with everything.

### 4.2 Multiple Attack Penalty (MAP)

The three-action economy allows up to three Strikes per turn. To keep "attack, attack, attack" from dominating (Pillar 4 — every turn should offer genuinely different good options), each Strike after the first on a turn takes a cumulative untyped penalty:

- **2nd Strike: −4. 3rd+ Strike: −8.** Weapons with the `[agile]` trait: **−3 / −6**. *(Gate A — flagged as the #1 value to re-validate; compressed math makes this bite harder than PF2E's −5/−10.)*
- **MAP is per-turn and resets at the start of each of your turns.** **Reaction Strikes (made off your own turn — Reactive Shot, a Sentinel Counter, etc.) are never subject to MAP and never contribute to it.** Off-turn Strikes are full-accuracy by design; the action-economy clamp on them is their *trigger* and any resource/frequency cost, **not** an accuracy penalty.

### 4.3 Reaction Economy — the table-speed cap *(Gate A, 2026-06-19)*

A character may use at most **3 reactions per round**, total, regardless of how many reaction-granting features/feats they have. Most characters have 1; reaction-specialist chassis (Sentinel) and feats (Combat Reflexes, Vigilant Guard) raise that **toward, but never past, 3**. This keeps off-turn interrupts from grinding table speed — a hard ceiling the [Gate-A pass](2026-06-19-gate-a-balance-pass.md) found the Guardian and Soldier could otherwise exceed (chassis 2nd reaction + two Combat-Reflexes feats = 4). *(The Sentinel's Premonition engine already embodies this cap; it is now universal.)*

---

## 5. Item Potency & Damage Scaling

*(Full equipment design is Phase 6; this section fixes only how gear touches the core math.)*

- **Potency bonus (Item type):** upgraded weapons grant a small **+1/+2/+3** Item bonus to attack rolls; upgraded armor grants **+1/+2/+3** Item bonus to AC. **Hard cap +3.**
- **Model: optional edge, NOT baked into creature math** *(5E-style, not an item tax).* Creatures are tuned for **baseline on-level characters**; potency is a real but bounded reward that makes a geared character modestly better. Un-upgraded parties remain fully viable — there is no gear tax. Because potency is capped at +3, crit drift from gear stays small and bounded.
- **Damage-dice scaling:** weapon upgrades increase **weapon damage dice** (e.g., 1 die → 2 → 3 → 4). This is the primary "my weapon got stronger" payoff and is fully bounded-accuracy-safe — it scales damage and time-to-kill, never to-hit.
- Beyond potency and damage dice, gear grants **traits, properties, and new options** (Phase 6), never additional flat to-hit/AC math.

---

## 6. Target Numbers & When to Roll

### 6.1 DC ladder (fixed, not level-keyed) — *provisional (Gate A)*

| Band | DC |
|---|---|
| Trivial | 8 |
| Easy | 11 |
| Moderate (default) | 14 |
| Hard | 18 |
| Severe | 22 |
| Extreme | 26 |

**Anchor principle:** a trained specialist succeeds at a **Moderate** task ~65% of the time at their tier, and gets gently better as they level. Exact values calibrate at Gate A once Phase 2 sets attribute ranges.

### 6.2 Targeted-effect DCs

An effect that targets another creature sets **DC = `10 + Proficiency + key attribute`**; the target rolls a save (`d20 + save proficiency + attribute`) against it. AC and class/power DCs share this construction (`10 + Proficiency + attribute`), which is why the symmetric Level term applies to them.

### 6.3 When to roll

- Roll **only when failure is interesting** and success isn't guaranteed; otherwise narrate success or charge time/resources.
- **Passive value = `10 + modifiers`** for routine/ambient checks and GM-side secret checks (standing awareness, noticing), keeping ordinary competence off the dice.

---

## 7. Action Economy

- **Three actions per turn**, spent freely (point-pool model). Most activities cost 1, 2, or 3 actions; the action cost is part of each ability's definition (priced in Phase 5+ via `ttrpg-ability-design`).
- **One reaction per round** (a single commonly-triggering interrupt budget per character) and **free actions** (no action cost, usually trigger-gated). The signature combat reaction is the **Reactive Shot** (§11).
- Multi-Strike turns are governed by MAP (§4.2). The economy is the primary currency abilities are balanced against — there are **no daily resource pools** (T3); ability uptime is governed by action cost and round/scene cooldowns (formalized Phase 3).

---

## 8. The Universal Trait System

### 8.1 Definition

A **trait** is a keyword tag attached to any entity (action, activity, feat, item, creature, class feature, condition, Force power, damage instance). Written in brackets in rules text: `[Force]`, `[agile]`, `[fire]`. A trait is either:

- **Rules-bearing** — defined once in the master trait glossary, applies wherever it appears (`[agile]` reduces MAP; `[manipulate]` requires a free hand and can trigger reactions; `[flourish]` = once per turn; `[open]` = only as the first action of your turn).
- **Hook** — no inherent effect; exists for other rules to reference for prerequisites, immunities, and interactions (`[droid]` creatures are immune to `[emotion]`; a feat requires the `[Force]` trait).

### 8.2 Taxonomy skeleton

Each downstream phase **registers** its traits into one of these top-level categories:

| Category | Purpose | Examples |
|---|---|---|
| **Entity-type** | What something fundamentally is | `[droid]` `[beast]` `[humanoid]`; `[weapon]` `[armor]` `[consumable]` |
| **Action** (rules-bearing) | Behavior in the economy | `[attack]` `[move]` `[manipulate]` `[concentrate]` `[flourish]` `[open]` `[press]` |
| **Damage/energy** | Resistance/weakness hooks | `[kinetic]` `[energy]` `[fire]` `[ion]` `[sonic]` |
| **Effect/sense** | Immunity & interaction hooks | `[mental]` `[emotion]` `[fear]` `[visual]` `[auditory]` `[healing]` `[poison]` |
| **Power-source / tradition** | Access gating & cross-interactions | `[Force]` `[tech]` `[martial]` (+ Force disciplines, later) |
| **Faction / affiliation** | Access gating + reputation hooks | `[Jedi]` `[Sith]` `[Imperial]` `[criminal]` (setting layer) |
| **Rarity** | Availability gating | `[common]` `[uncommon]` `[rare]` `[unique]` |
| **Build-category** | Powers the prerequisite system | class traits (e.g. `[soldier]`), `[skill]`, `[archetype]`, `[species]` |

### 8.3 Prerequisites are machine-checkable

Prerequisites are expressed as required traits + thresholds, e.g. `Prerequisite: trained in [Stealth], the [Force] trait`. Access validation is therefore **data, not prose** — the stated goal of "in-system metadata that makes conditions and prerequisites easy."

### 8.4 Governance (anti-sprawl, complexity-budget guard)

A new trait is justified **only if** (a) more than one rule references it, **or** (b) it carries a reusable baseline effect. One-off interactions stay as plain rules text. The trait glossary is a tool, not a second rulebook.

### 8.5 Relationship to conditions

**Conditions** (Frightened, Prone, etc.) are standardized status effects that carry traits and impose mostly **Status**-type modifiers. They slot into this trait/bonus architecture rather than living outside it. The standard condition list is content for a later phase.

---

## 9. Exit-Gate Checklist (per roadmap)

- [x] Die engine and distribution understood (d20, flat, +1 = +5%).
- [x] Lifetime modifier spread ≤ ~75% of die range (≈ +1 to +15 on d20). ✔
- [x] Stacking rule decided (typed: circumstance / status / item; MAP untyped).
- [x] Target-number model decided; bounded vs treadmill decided **explicitly** (§2.3).
- [x] Success spectrum decided (four degrees + nat-20/nat-1 step); whiff mitigation stated.
- [x] Action economy decided (three actions, 1 reaction, free actions); reactions bounded.
- [x] "When do we roll" principle stated (§6.3).
- [x] **Pillar 1 demonstration:** worked example shows constant on-level math across levels 1–20 (§2.4).
- [x] **T2 demonstration:** crit frequency constant across the level band (§2.4).

## 10. Carried Forward (open items for later phases)

- **Attribute count, names, ranges, generation** → Phase 2. (DC ladder & lifetime-spread numbers finalize here.)
- **MAP value, DC ladder values, potency breakpoints** → re-validate at Gate A.
- **Cooldown taxonomy (round/scene), no-daily-pool formalization** → Phase 3.
- **Ability action-pricing**, condition list, Force-discipline traits → Phases 4–5.
- **Potency breakpoints, damage-dice progression, full item traits** → Phase 6.
- **Creature-building math** (how level *N* sets L, role-based ranks/attributes) → Phase 7.

---

## 11. Combat Engagement Assumptions *(amendment — added 2026-06-13 during Phase 5)*

**Ranged is the default mode of engagement.** In a blaster-saturated galaxy, the typical combatant fights at range. Consequences:

- **The balance baseline is a ranged Strike.** DPR benchmarks, the "typical turn," and encounter/creature math all assume ranged engagement as the reference point. Melee is the high-risk/high-reward alternative that sits *above* the ranged DPR baseline.
- **Melee is deadlier:** melee weapons carry bigger damage dice, add the wielder's attribute to damage (STR, or DEX for `[finesse]` weapons such as lightsabers), and lean on stronger crit effects (`[deadly]`). *(Exact numbers: Phase 6.)*
- **Melee is riskier — the Reactive Shot:**

> **Reactive Shot** `[reaction]` — **Trigger:** a creature you can perceive makes a melee **Strike** while **within 10 feet of you**, you have a ranged weapon ready, and your reaction is available. *(It triggers on a melee Strike, **not** on movement — a creature that merely Strides past does not provoke it.)* **Effect:** make a ranged Strike against the triggering creature. Per reaction timing it resolves as the Strike is declared, so if it incapacitates the attacker the triggering Strike is simply lost — there is no separate "disrupt" mechanic.

- **Covering fire (resolves F2):** the reaction is **not** limited to the creature being attacked — *any* armed gunner within 10 ft who can perceive the attacker may Reactive-Shot it. A meleer charging a clustered squad can draw fire from the whole squad (each gunner spends its one reaction), delivering the "don't charge a firing line" fantasy. Bounded by the 1 reaction/round economy and unable to loop (a Reactive Shot is a *ranged* Strike, which never provokes).
- **Only risky vs gunners.** A Reactive Shot requires a nearby gunner with a ranged weapon and an available reaction, so closing on unarmed or melee-only foes is safe. The fiction: charging a blaster line is dangerous; charging a vibro-axe thug is not.
- **Movement stays free** — only the melee *Strike* provokes, never repositioning (keeps tactical movement fluid; avoids fiddly range-band triggers).
- **Counters (what makes melee worth the risk):** melee's higher damage; **Force deflection** (negates the Reactive Shot — the structural reason Force defenses exist, see the Phase 5 Guardian); **stealth/surprise** (a target unaware of the threat can't react); and **flanking/teamwork** (a foe that already spent its reaction can't shoot).
- This deliberately **inverts** the traditional fantasy-TTRPG assumption (melee punishing movement): here the **gunner punishes the swordsman**.

**Forward effects:** weapon traits, damage, ranges (`[finesse]`, `[deadly]`, range increments) → Phase 6; ranged/melee creature roles and how monsters use the Reactive Shot → Phase 7; Force deflection and melee-closer kits → Phase 5.

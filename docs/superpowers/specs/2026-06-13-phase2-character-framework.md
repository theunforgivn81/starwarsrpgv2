# Phase 2 — Character Framework

**Status:** Approved
**Date:** 2026-06-13
**Roadmap phase:** 2 of 9 — see [build roadmap](../plans/2026-06-13-star-wars-rpg-build-roadmap.md)
**Upstream:** [Design Philosophy](2026-06-13-star-wars-rpg-design-philosophy.md), [Phase 1 — Core Mechanic & Traits](2026-06-13-phase1-core-mechanic-and-traits.md)
**Resolves:** Pillar 2 (no mandatory seats — recovery decoupled from class). Closes Phase 1's deferred items: attribute range (finalizes the DC ladder) and the HP/recovery model.

> **Note:** Values marked *(Gate A)* are provisional pending balance-analysis calibration. Structure is fixed; some numbers are tunable. Items marked *(content: Phase N)* define a slot here and are filled by a later phase.

---

## 1. Identity Model — Species + Class + Background

A character is defined by three slots (the Origin + Vocation + Background model):

- **Species** — origin/ancestry. Grants attribute boosts, traits, a speed, and a species feat. *(content: later phase)*
- **Class** — vocation and the source of the character's gameplay **verb**. Sets the key attribute, proficiency ranks, HP value, and first class feature. *(content: Phase 5)*
- **Background** — pre-adventuring life. Grants attribute boosts, a trained skill, and a skill feat. *(content: later phase)*

Rejected alternatives: **Lifepath** front-loads identity and fights Pillar 4 (meaningful choice every level); **point-buy** serves only the hardcore pole and abandons the high floor.

---

## 2. Attributes

### 2.1 The six (classic names, modifier-only)

Stored as **modifiers only** (no scores — Phase 1). Six attributes:

| Attribute | Drives checks | Feeds derived stats | Primary for | Anti-dump hook |
|---|---|---|---|---|
| **Strength (STR)** | Athletics, melee Strikes | melee damage | melee bruisers | physical-offense path |
| **Dexterity (DEX)** | Acrobatics, Stealth, Thievery, Piloting, ranged/finesse Strikes | **AC** (armor-capped), **Reflex** | skirmishers, scoundrels, gunslingers | physical-offense path |
| **Constitution (CON)** | — | **HP**, **Fortitude** | universal | **HP** = universal hook |
| **Intelligence (INT)** | Computers, Repair, Lore | **bonus trained skills** | slicers, mechanics, scholars | extra skills = no dump |
| **Wisdom (WIS)** | Survival, Medicine | **Perception**, **Will**, initiative | medics, survivalists, the attuned | Perception = universal hook |
| **Charisma (CHA)** | Deception, Persuasion, Intimidation | (social pillar) | faces, leaders, some Force users | elevated by first-class social pillar |

### 2.2 God-stat / dump-stat audit

- **DEX is deliberately de-fanged:** initiative moves to a Perception (WIS) check, and AC applies an **armor Dex-cap**, so a heavy-armor STR build needs no DEX. STR and DEX form a "pick one physical-offense stat" pair — neither is universal.
- **CHA is rescued** from dump-stat status by the first-class social pillar; Presence is as build-relevant as a combat stat.
- No attribute feeds more than two top-tier derived stats: DEX → AC + Reflex; CON → HP + Fort; WIS → Perception + Will.

### 2.3 Range & growth

- **Creation cap:** key attribute ≤ **+3** at level 1 (tighter than PF2E's +4, honoring bounded accuracy).
- **Lifetime cap:** **+6** (lets a L20 legendary specialist reach the ~+15–16 total the Phase 1 spine targets: `L6 + R4 + attr6`).
- **Assignment:** a **boost system** bundling Species + Background + Class + a few free boosts (bundling controls the creation decision count).
- **Growth schedule** (when boosts arrive) is deferred to **Phase 3 (progression)**; only the *range* is fixed here.

### 2.4 Saves

Three saves, one attribute each (no save god-stat): **Fortitude = `L+R+CON`**, **Reflex = `L+R+DEX`**, **Will = `L+R+WIS`**.

---

## 3. Skills

Ranked proficiency (`L + R + attribute`; untrained = +0, per Phase 1). The list promises a tech-rich game with a first-class social pillar.

| Skill | Attr | Covers |
|---|---|---|
| Athletics | STR | climb, jump, swim, grapple, shove |
| Acrobatics | DEX | balance, tumble through, escape |
| Stealth | DEX | hide, sneak, conceal |
| Thievery | DEX | sleight of hand, physical locks, disarm devices |
| Piloting | DEX | drive/fly vehicles & starships *(light supporting pillar; rules Phase 8)* |
| Computers | INT | slicing, electronics, security, data |
| Repair | INT | repair, craft, demolitions, droids *(renamed from "Engineering" to avoid colliding with the `[engineering]` Lore trait)* |
| Lore | INT | Recall Knowledge; subject specializations via traits (e.g. `[underworld]`, `[galactic-history]`, `[engineering]`) |
| Survival | WIS | tracking, navigation, subsist |
| Medicine | WIS | first aid, **Treat Wounds** (recovery hub) |
| Deception | CHA | lie, feint, disguise, create a diversion |
| Persuasion | CHA | request, negotiate, gather info, shift attitudes |
| Intimidation | CHA | coerce, demoralize |

- **Perception** is a **separate core proficiency** (not a skill), keyed to WIS; drives awareness and default initiative.
- **No "Use the Force" skill.** The Force is class actions with verbs, not a skill check — this is where the "no spellcasters" commitment (T4) is enforced structurally; Force access requires a class/build commitment, not a trained skill.
- Consolidations against phantom skills: **Society** folded into Lore (knowledge) + Persuasion (interaction); standalone **Performance** dropped (rides on Deception/Persuasion).
- **Bonus trained skills:** a character is trained in `class/background-granted skills + INT modifier` skills at creation (INT's anti-dump hook).

---

## 4. Derived Stats

| Stat | Formula | Notes |
|---|---|---|
| **HP** | `species base + level × (class HP value + CON mod)` | CON payoff; HP is a primary bounded-accuracy scaling axis. *(class HP value: Phase 5; species base: species content)* |
| **AC** | `10 + armor proficiency (L+R) + DEX (capped by armor) + item potency + circumstance` | armor Dex-cap is the DEX pressure-valve *(armor details: Phase 6)* |
| **Fortitude / Reflex / Will** | `L + R + (CON / DEX / WIS)` | §2.4 |
| **Perception** | `L + R + WIS` | default initiative roll |
| **Class DC / class attack** | `L + R + key attribute` | key attribute set by class *(Phase 5)* |
| **Speed** | flat, by species | not attribute-driven (keeps STR/DEX off it) |
| **Initiative** | usually a **Perception** check; sometimes a relevant skill (e.g., Stealth for an ambush) | decoupled from DEX |

---

## 5. Recovery Model (resolves Pillar 2 at the HP layer)

HP recovery is **time-gated**, not class-gated or daily-gated, with a floor that requires no one.

| Mechanism | Who | When | Effect |
|---|---|---|---|
| **Catch Your Breath** (the floor) | anyone, no check | a ~10-minute lull out of danger | regain up to **~½ max HP** *(Gate A)*; the class-agnostic floor |
| **Treat Wounds** | trained+ in Medicine | out of combat, takes time | heals more / faster, on four degrees (crit success heals more; crit failure deals minor damage) — the **accelerant**, not a gate *(numbers: Gate A)* |
| **First Aid / Stabilize** | trained in Medicine | in combat (action cost) | stop a dying ally; minor patch |
| **Stimpacks & class verbs** | anyone with the item; specific classes | in combat | tactical top-ups; stimpacks are money-gated *(Phase 6)* |
| **Full rest** | anyone | a night's rest / downtime | restore **all HP**, clear fatigue, **reset scene-cooldowns** |

**Design consequences:**
- **No mandatory healer (Pillar 2):** the free floor needs no one; Medicine/stimpacks only make recovery faster/better.
- **No daily clock (T3):** recovery is time-gated; full rest refills **no daily pool because none exists**. The GM creates attrition tension by **denying time** (ticking objectives, pursuit), an exploration-pillar fiction question, not bookkeeping.
- **Combat is roughly per-encounter:** most fights start near-full, so each is balanced as a fresh challenge — keeping bounded-accuracy encounter math clean.

---

## 6. Character Creation Sequence

Audience is hardcore-leaning with a high floor, so the decision count can be high *if* bundled and backstopped by quick-builds:

1. **Concept**
2. **Species** → attribute boosts, traits, speed, species feat
3. **Background** → attribute boosts, a trained skill, a skill feat
4. **Class** → key attribute, proficiency ranks, HP value, first gameplay verb
5. **Finalize attributes** → apply free boosts (key attribute ≤ +3 at creation)
6. **Trained skills** → `class/background skills + INT mod`
7. **Buy gear**

- Decisions are **bundled** (each of Species/Background/Class delivers multiple sheet entries in one pick).
- **Every class ships a quick-build** (recommended species, boosts, skills, gear) to preserve the high floor for casual players.
- Bracketed content is authored in later phases; Phase 2 fixes the **sequence and slots**.

---

## 7. Character Sheet Anatomy (cognitive-load tiers)

1. **Constant** (every turn, top of sheet): AC, HP, three-action tracker, attacks, key DC, Perception, saves, speed.
2. **Frequent** (every scene): skills, conditions, consumables/ammo.
3. **Occasional**: feature full text, inventory detail.
4. **Archive** (level-up only): build choices.

Because bonuses are typed (no flat item stacking on the core math) and conditions impose clean **Status** modifiers, **no constant-tier value requires mid-session recomputation** — the framework stays inside its cognitive budget without mandatory digital tooling.

---

## 8. DC Ladder Confirmation (closes a Phase 1 open item)

With the attribute range now fixed, the Phase 1 provisional DC ladder is consistent with the anchor principle. A trained specialist at low level (`L1 + R1 + attr+3 = +5`) vs **Moderate ≈ 13–14** succeeds ~60–65%, matching the target; the ladder gets its final calibration at Gate A.

---

## 9. Exit-Gate Checklist (per roadmap)

- [x] Identity pillar model chosen (Species + Class + Background); hybrids justified.
- [x] Attribute count chosen (6); every attribute passes the coverage test; dump-stat audit done.
- [x] Modifier-only confirmed (scores carry no separate job).
- [x] Attribute range at creation (+3) and cap (+6) defined; fits the modifier-spread budget.
- [x] Skill model chosen (ranked proficiency); every skill maps to a recurring activity; no phantom skills.
- [x] Every derived-stat formula written; no god-stat (≤2 top-tier derived stats per attribute).
- [x] Creation decision count managed via bundling; quick-build path exists.
- [x] Sheet elements sorted into four tiers; constant tier needs no mid-session recomputation.
- [x] **Pillar 2 demonstration:** a healer-less party recovers to full via Catch Your Breath + full rest, using only universal options.

## 10. Carried Forward (open items for later phases)

- **Attribute boost growth schedule** → Phase 3 (progression).
- **Cooldown taxonomy (round/scene), no-daily-pool formalization** → Phase 3.
- **Class HP values, key attributes, proficiency-rank progressions, gameplay verbs** → Phase 5.
- **Species content** (base HP, speeds, boosts, traits, feats) and **Background content** → later phase.
- **Armor Dex-cap values, stimpack items, Treat Wounds numbers** → Phase 6.
- **Catch Your Breath fraction, Treat Wounds numbers, final DC ladder** → Gate A.
- **Condition list** → Phase 4–5.

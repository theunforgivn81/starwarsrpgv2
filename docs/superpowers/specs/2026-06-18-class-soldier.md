# Class — Soldier *(in progress)*

**Status:** Foundation — identity, initial proficiencies, L1–20 chassis, and the **Suppress** verb framework designed. **Subclasses** and **class feats** are the next design steps.
**Date:** 2026-06-18
**Type:** Class detail. The first **non-Force** chassis (no Attunement) — validates the martial baseline cleanly. Pairs with the [Guardian](2026-06-18-class-guardian.md) as the two "tank" classes (different shapes). ORC-core Soldier read for its Suppressed/Area-Fire bones; our divergences per the design discussion.
**Upstream:** [Phase 5 chassis](2026-06-13-phase5-class-design-and-force.md), [Phase 3 progression](2026-06-13-phase3-progression-chassis.md), [Phase 1 core mechanic](2026-06-13-phase1-core-mechanic-and-traits.md) (MAP, conditions, Reactive Shot), [Creation Slot Contributions](2026-06-15-creation-slot-contributions.md).

---

## 1. Identity

*A heavy-weapons trooper who owns the field of fire — turning their own offense into the party's defense.* **Key attribute: Constitution. HP 10.** The Soldier is the **control-tank**: it lays down **Suppressing Fire** that debuffs a whole cone's accuracy and posts a kill-zone that punishes movement, then **soaks** the fire it draws with high HP and heavy armor. It protects allies *indirectly* — fewer enemy attacks land, fewer reach the squishies — where the Guardian protects *directly*.

*"You play a trooper who lays down suppressing fire, and on a typical turn you blanket a zone — chunking and pinning everyone in it — pick off a suppressed foe, and hold a reaction to punish anyone who moves in your sights."*

**The two tank levers** (soft aggro, no hard taunt):
- **Lever A — costly to ignore:** Suppression cripples enemy offense and the **Suppressing Reaction** punishes movement/action in your zone, so dealing with the Soldier is the enemy's best play.
- **Lever B — protect the party:** Suppressed foes **miss more** (accuracy debuff) and are **pinned** (zone-punish slows their advance), so allies take fewer, weaker hits — and the Soldier **soaks** what comes (HP + heavy armor).

**Uniqueness (the verb):** **Suppress** — the only class that posts a debuffing kill-zone and enforces it with reactions. **No Force resource; runs at-will** (action-economy gated) so it never gases out of tanking.

**Role profile:** Control 3 · Durability 3 · Area offense 2 · Single-target 1 · Support 1 · Social 1 · Utility 0 *(sum 11 — the inverse of the Guardian's offense-led shape).*

---

## 2. Initial Proficiencies (Level 1)

| Category | Rank | Notes |
|---|---|---|
| **Perception** | Trained | advances to Expert |
| **Fortitude** | **Expert** | the signature save → **Legendary** (the toughest body in the game) |
| **Will** | **Expert** | disciplined, hard to break |
| **Reflex** | Trained | the lagging save |
| **Class DC** | Trained | Suppression save-DC + suppressed-feat effects |
| **Weapons** | Trained — simple + martial (+ unarmed) | a dedicated attacker (→ Legendary, §3) |
| **Defense** | Trained — **all armor (incl. heavy)** + unarmored | heavy armor is the soak |
| **Skills** | **Intimidation** + Trained in **3 + Int modifier** | the menacing frontliner |

No Attunement — the Soldier is **non-Force**. Its limiter is **action economy + the reaction economy** (and, at the equipment layer, ammo/reload on area weapons — Phase 6).

---

## 3. Level Progression (chassis)

Grants per [Phase 3](2026-06-13-phase3-progression-chassis.md) incl. the L1 class feat and universal **Weapon Specialization** (L7/L15). ✦ = Soldier core feature · ◆ = subclass feature.

| Lvl | Class features & chassis grants | Proficiency advances |
|---|---|---|
| 1 | **Suppress** ✦ (Suppressing Fire + Zone + **Suppressing Reaction**) · **Overwhelming Assault** ✦ · **subclass** ◆ · class feat · ancestry feat · CON boost | initial profs (§2) |
| 2 | class feat · skill feat | — |
| 3 | general feat · skill increase · ◆ | Reflex → **Expert** · Class DC → **Expert** |
| 4 | class feat · skill feat | — |
| 5 | ancestry feat · skill increase · attribute boosts | weapons → **Expert** · armor → **Expert** |
| 6 | class feat · skill feat | — |
| 7 | general feat · skill increase · ◆ · **Weapon Specialization** | Perception → **Expert** |
| 8 | class feat · skill feat | — |
| 9 | ancestry feat · skill increase · **Dig In** ✦ | Will → **Master** |
| 10 | class feat · skill feat · attribute boosts | — |
| 11 | general feat · skill increase · ◆ | Fort → **Master** · Class DC → **Master** |
| 12 | class feat · skill feat | — |
| 13 | ancestry feat · skill increase · **Withering Fire** ✦ | weapons → **Master** · armor → **Master** |
| 14 | class feat · skill feat | — |
| 15 | general feat · skill increase · attribute boosts · ◆ · **Greater Weapon Specialization** | **Fortitude → Legendary** ✦ |
| 16 | class feat · skill feat | — |
| 17 | ancestry feat · skill increase · **Pinned Down** ✦ | Perception → **Master** · Reflex → **Master** |
| 18 | class feat · skill feat | — |
| 19 | general feat · skill increase · ◆ | weapons → **Legendary** |
| 20 | class feat · skill feat · attribute boosts · **No Quarter** ✦ *(capstone)* | — |

- **Weapon track (dedicated attacker):** Trained → **Expert (L5) → Master (L13) → Legendary (L19)** — the Soldier caps a weapon, per the "dedicated attackers reach Legendary" principle. *(Proposed; the per-class weapon track is a confirm-point.)*
- **Fortitude → Legendary (L15)** is the Soldier's signature line (as Perception is the Sentinel's) — the toughest save in the game.
- **No dead levels**; exact advancement levels Gate-A tunable.

---

## 4. The Verb — Suppress (zone + reaction)

The Soldier's turn is **post a zone → enforce it → soak**. Typical turn: **Suppressing Fire** (2 actions) to blanket a cone, then a 3rd action (a Strike on a Suppressed foe at reduced MAP, reposition, or Reload), holding the **Suppressing Reaction** for the enemy turn. The decisions — *where* to place the zone, *whom* to punish, *when* to react — are the variety, not "Strike ×3."

### 4.1 The Suppressed condition *(new, formal)*

**Suppressed** *(condition)*: the creature takes a **−1 circumstance penalty to attack rolls** (it's keeping its head down). Lasts until the start of the suppressing Soldier's next turn (or while it remains in an active Suppression Zone). *Deepens to −2 at L13 (Withering Fire).* **One-rider rule** (from ORC): when a Soldier takes an action that applies Suppressed, it may also apply **one** effect with the **`[suppressed]`** trait (feat/subclass riders — off-guard, slowed, etc.); only one such rider per suppressing action.

### 4.2 Suppressing Fire `[2 actions]` + the Suppression Zone

- **Suppressing Fire:** with a ranged weapon, lay down fire in a **cone or burst** within range — a **Suppression Zone**. Creatures in the area attempt a **basic Reflex save** (vs Class DC): take **area damage** (save-for-half, scales with weapon dice — *consistent, not spiky*) and become **Suppressed**. With an **area/automatic weapon** the zone is larger (the subclass/equipment axis).
- **The Zone persists until the start of your next turn.** While it's up, enemies in it are **Suppressed**, and any enemy that **Strides within/through the zone or takes a hostile action while inside it provokes your Suppressing Reaction**. *(This is the kill-zone — the genre point: the gunner punishes movement.)*

### 4.3 Suppressing Reaction `[reaction]`

- **Trigger:** an enemy in your Suppression Zone **moves** or **takes a hostile action**.
- **Effect:** make a ranged **Strike** against it (a covering shot) **or** halt its movement (it stops). Full-accuracy ([reaction Strikes ignore MAP](2026-06-13-phase1-core-mechanic-and-traits.md)). **Once per round** baseline; **Withering Fire** (L13) grants a 2nd, and feats add more — filling the **empty ORC Soldier reaction slot** the chassis deliberately claims.

### 4.4 Overwhelming Assault *(chassis, L1)*

Your **MAP against Suppressed targets is reduced one step** (−3/−6, agile −2/−4). So while your area work debuffs the cone, your single-target follow-up **Strikes vs the foes you've suppressed stay accurate** — the source of *respectable* (never spiky) single-target damage.

### 4.5 ✦ development

- **L9 Dig In** — the soak spike: while you haven't moved since your last turn (holding the line), gain **resistance** to physical & energy = your CON mod (you're dug in behind the heavy armor).
- **L13 Withering Fire** — Suppressed deepens to **−2**; you gain a **2nd Suppressing Reaction** per round.
- **L17 Pinned Down** — Suppressed enemies can't take **reactions** and are **off-guard** to ranged attacks; your Zone is larger.
- **L20 No Quarter** *(capstone)* — total zone dominance: enemies can't leave your Suppression Zone toward your allies without provoking, and a creature that critically fails its save vs your Suppressing Fire is also **slowed 1**.

---

## 5. Subclasses *(to design next — ~5 target)*

Branch at **L1** on the **1/3/7/11/15/19** cadence; each modulates **Suppress**. Sketched ([roster §5](2026-06-15-subclass-roster-sketch.md)):
- **Bulwark** (Armor Storm) — the two-handed **melee** Soldier: maneuvers + suppression at reach, resistance vs Suppressed enemies (the immovable frontline).
- **Suppressor** (Action Hero) — auto-fire/zone-denial specialist; the biggest, meanest Suppression Zones.
- **Demolitionist** (Bombard) — explosives & grenades; burst area damage + suppressed riders.
- *(Two more toward the ~5 target — e.g., a **Sentinel/Bodyguard** body-blocking protector and a **Heavy Gunner** single-zone-anchor — TBD.)*

---

## 6. Class Feats *(to design next)*

~50 (ORC norm): general feats (Suppression shapers, the **`[suppressed]`** riders that customize the debuff, reaction upgrades, soak/durability, Intimidation/menace) + subclass feats. Mined from the prior Soldier `ClassFeat` suite (Overwhelming Assault, Ammo Hoarder, Run Cowards!, Bullet Typhoon, Scattering Fire, etc.).

---

## 7. Carried Forward

- **§5 subclasses** (~5) on the 1/3/7/11/15/19 cadence; Armor Storm = the melee fork.
- **§6 class feats** (~50), general + subclass, including the **`[suppressed]`** rider feats.
- **Define `Suppressed` formally** in the conditions glossary (Phase 1 / connective-tissue) once finalized.
- **Gate-A validation:** Suppressed value (−1/−2) as an area debuff, the Suppressing Reaction economy + Dig In resistance, area DPR vs the bracket, the weapon track (Legendary at 19), and the reworked CON key (vs the slice's DEX Soldier).
- Flavor/description → rules-writing.

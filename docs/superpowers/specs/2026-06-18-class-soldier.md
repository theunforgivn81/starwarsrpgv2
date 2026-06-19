# Class — Soldier *(in progress)*

**Status:** Foundation — identity, initial proficiencies, L1–20 chassis, and the **Suppress** verb framework designed (**ORC-core progression kept & supplemented**; Primary Target dropped). **Subclasses** and **class feats** are the next design steps.
**Date:** 2026-06-18
**Type:** Class detail. The first **non-Force** chassis (no Attunement) — validates the martial baseline cleanly. Pairs with the [Guardian](2026-06-18-class-guardian.md) as the two "tank" classes (different shapes). **We keep the ORC-core Soldier ability progression** (Walking Armory, Fearsome Bulwark, the Suppressed condition, the durability spine, the prof scaffold) and **modify/supplement** it (Suppression Zone + Suppressing Reaction, Overwhelming Assault baselined, ✦ upgrades, a real L20 capstone), **dropping Primary Target**.
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

We **keep the ORC-core Soldier progression** and supplement it; **Primary Target is dropped** (poorly-worded, GM-disliked — its single-target role is covered by Overwhelming Assault). **Kept-from-ORC** features in *italics*; **our additions (✦)** in bold. ◆ = subclass (fighting style).

| Lvl | Class features & chassis grants | Proficiency advances |
|---|---|---|
| 1 | **Suppress** ✦ (Suppressing Fire + **Zone** + **Suppressing Reaction**) · **Overwhelming Assault** ✦ · *Walking Armory* · **subclass (fighting style)** ◆ · class feat · ancestry feat · CON boost | initial profs (§2) |
| 2 | class feat · skill feat | — |
| 3 | general feat · skill increase · *Fearsome Bulwark* · ◆ | Reflex → **Expert** |
| 4 | class feat · skill feat | — |
| 5 | ancestry feat · skill increase · attribute boosts · *Soldier Weapon Expertise* (area/auto crit spec) | weapons → **Expert** · Perception → **Expert** |
| 6 | class feat · skill feat | — |
| 7 | general feat · skill increase · ◆ · *Tough as Nails* · Weapon Specialization | Fort → **Master** · armor → **Expert** · Class DC → **Expert** |
| 8 | class feat · skill feat | — |
| 9 | ancestry feat · skill increase · **Dig In** ✦ | — |
| 10 | class feat · skill feat · attribute boosts | — |
| 11 | general feat · skill increase · ◆ · *Soldier's Resolution* | Will → **Master** |
| 12 | class feat · skill feat | — |
| 13 | ancestry feat · skill increase · **Withering Fire** ✦ | armor → **Master** |
| 14 | class feat · skill feat | — |
| 15 | general feat · skill increase · attribute boosts · ◆ · *Unshakable Juggernaut* ✦ · Greater Weapon Specialization | **Fort → Legendary** · weapons → **Master** · Class DC → **Master** |
| 16 | class feat · skill feat | — |
| 17 | ancestry feat · skill increase · **Pinned Down** ✦ | armor → **Legendary** · Perception → **Master** |
| 18 | class feat · skill feat | — |
| 19 | general feat · skill increase · ◆ | **weapons → Legendary** · Class DC → **Legendary** |
| 20 | class feat · skill feat · attribute boosts · **No Quarter** ✦ *(capstone)* | — |

- **Weapon track:** ORC's curve (Trained → Expert L5 → Master L15) **+ our Legendary at L19** (the "dedicated attackers reach Legendary" principle — the one place we diverge upward from ORC). *(Per-class confirm-point.)*
- **Reflex stays Expert** — the Soldier's deliberate weak save (heavy and slow; the vector enemies get against it).
- **Durability spine (kept from ORC):** *Tough as Nails* (L7, Fort success→crit success), *Soldier's Resolution* (L11, Will success→crit success), *Unshakable Juggernaut* (L15, Fort→Legendary; crit-fail→fail; **halve damage on a failed Fort save vs damage**). Multiple Legendary lines (Fort/armor/weapons/Class DC) are intentional — the Soldier is the supreme durability/control specialist; flagged for Gate-A.
- **No dead levels** (ORC's L20 had no capstone feature — **No Quarter** fixes that); advancement levels Gate-A tunable.

---

## 4. The Verb — Suppress (zone + reaction)

The Soldier's turn is **post a zone → enforce it → soak**. Typical turn: **Suppressing Fire** (2 actions) to blanket a cone, then a 3rd action (a Strike on a Suppressed foe at reduced MAP, reposition, or Reload), holding the **Suppressing Reaction** for the enemy turn. The decisions — *where* to place the zone, *whom* to punish, *when* to react — are the variety, not "Strike ×3."

### 4.1 The Suppressed condition *(new, formal)*

**Suppressed** *(condition, from ORC)*: the creature takes a **−1 circumstance penalty to attack rolls** *and* a **−10-foot status penalty to its Speeds** (head down, pinned — the penalty hinders *both* their offense and their advance on your allies, serving Lever B twice). Lasts until the start of the suppressing Soldier's next turn (or while it remains in an active Suppression Zone). *The attack penalty deepens to −2 at L13 (Withering Fire).* **One-rider rule** (ORC): when a Soldier takes an action that applies Suppressed, it may also apply **one** effect with the **`[suppressed]`** trait (feat/subclass riders — off-guard, frightened, slowed, etc.); only one such rider per suppressing action.

### 4.2 Suppressing Fire `[2 actions]` + the Suppression Zone

- **Suppressing Fire:** with a ranged weapon, lay down fire in a **cone or burst** within range — a **Suppression Zone**. Creatures in the area attempt a **basic Reflex save** (vs Class DC): take **area damage** (save-for-half, scales with weapon dice — *consistent, not spiky*) and become **Suppressed**. With an **area/automatic weapon** the zone is larger (the subclass/equipment axis).
- **The Zone persists until the start of your next turn.** While it's up, enemies in it are **Suppressed**, and any enemy that **Strides within/through the zone or takes a hostile action while inside it provokes your Suppressing Reaction**. *(This is the kill-zone — the genre point: the gunner punishes movement.)*

### 4.3 Suppressing Reaction `[reaction]`

- **Trigger:** an enemy in your Suppression Zone **moves** or **takes a hostile action**.
- **Effect:** make a ranged **Strike** against it (a covering shot) **or** halt its movement (it stops). Full-accuracy ([reaction Strikes ignore MAP](2026-06-13-phase1-core-mechanic-and-traits.md)). **Once per round** baseline; **Withering Fire** (L13) grants a 2nd, and feats add more — filling the **empty ORC Soldier reaction slot** the chassis deliberately claims.

### 4.4 Overwhelming Assault *(chassis, L1 — replaces the dropped Primary Target)*

Your **MAP against Suppressed targets is reduced one step** (−3/−6, agile −2/−4). So while your area work debuffs the cone, your single-target follow-up **Strikes vs the foes you've suppressed stay accurate** — the source of *respectable* (never spiky) single-target damage. *(This covers the niche the dropped **Primary Target** filled — focusing a suppressed foe — without its clunky "success becomes failure" wording.)*

### 4.5 Durability & CON-mastery *(kept from ORC — the single-attribute engine)*

These are why a one-stat CON class works; we keep them intact:
- **Walking Armory** (L1): use **CON instead of STR** for armor requirements; if you already meet the requirement, reduce the armor's Bulk by 1; +carry capacity. *(Lets the CON tank wear heavy armor with no STR investment.)*
- **Fearsome Bulwark** (L3): use **CON instead of CHA** for Intimidation (Coerce/Demoralize) and **instead of STR** for Athletics (Reposition/Shove). *(Powers the menace **and** the Armor Storm maneuver fork on CON alone — anti-MAD.)*
- **Tough as Nails** (L7): Fort → Master; a **success on a Fort save becomes a critical success**.
- **Soldier's Resolution** (L11): Will → Master; a **success on a Will save becomes a critical success**.
- **Unshakable Juggernaut** (L15): Fort → Legendary; a **critical failure on a Fort save becomes a failure**; and when you **fail** a Fort save against an effect that deals damage, you **halve** that damage. *(The capstone of the soak — the Soldier shrugs off what would fell others.)*

### 4.6 Suppression upgrades *(✦ — our additions)*

- **L9 Dig In** — while you haven't moved since your last turn (holding the line), gain **resistance to physical & energy = your CON mod** (dug in behind the armor — stacks the soak with §4.5).
- **L13 Withering Fire** — Suppressed's attack penalty deepens to **−2**; you gain a **2nd Suppressing Reaction** per round.
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

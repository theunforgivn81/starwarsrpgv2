# Character Creation — Slot Contributions (Background / Species / Class)

**Status:** Approved
**Date:** 2026-06-15
**Type:** Framework spec — defines exactly what each creation slot grants. Fills the boost-allocation detail [Phase 2 §2.3/§6](2026-06-13-phase2-character-framework.md) deferred. Largely inherited from PF2E/SF2E (Paizo **ORC**, Philosophy §0), reiterated for our system with our deviations marked.
**Upstream:** Phase 2 (slots, attributes), [Phase 3](2026-06-13-phase3-progression-chassis.md) (progression, rank gates), [Phase 5](2026-06-13-phase5-class-design-and-force.md) (class chassis).
**Scope:** the *expectations/contract* for each slot. Specific Backgrounds, Species, and Classes are **content (Phase 8)**.

---

## 1. Background

- **Trained** in **one Skill** and **one Lore**.
- **One Skill Feat** for the skill it trains.
- **Two attribute boosts** (+1 each): **one** must go to one of **two background-relevant attributes** (e.g., a Politician → Intelligence *or* Charisma); the **other is free**. (Per §4, the two must target *different* attributes.)

## 2. Species (Ancestry)

- **Attribute boosts netting +2**, in one of two formats:
  - **Free:** boosts the player assigns freely (net +2), *or*
  - **Fixed:** a combination of fixed boosts and **flaws (−1)** plus **one assignable boost**, also **netting +2**.
  - **Constraint:** species may not move any single attribute by **more than ±1** (a species boost can't stack onto a species flaw/boost of the same attribute).
- Defines **Size**, base **Speed**, and starting **racial HP** (the "species base" term in the [Phase 2 HP formula](2026-06-13-phase2-character-framework.md)).
- *May* grant: an **enhanced sense**, a **non-standard movement type**, and/or **starting languages** beyond Galactic Basic.
- Any further racial benefits are reserved for **Species Feats** (Ancestry Feats), gained per the [Phase 3 cadence](2026-06-13-phase3-progression-chassis.md) (levels 1/5/9/13/17).

## 3. Class

**At creation:**
- **HP per level** (the class HP tier, [Phase 5](2026-06-13-phase5-class-design-and-force.md): 6/8/10) and the **key attribute** (with its **+1 boost**).
- **Starting proficiencies:**
  - **Perception** and **all saving throws**: **Trained or Expert** — **never Untrained**. Every class is at least Trained in all three saves and Perception; the **Trained-vs-Expert** split is *core* to how classes are differentiated as "good" vs "bad" at each.
  - **At least one core class Skill** + an **additional number of trained skills** (set per class for balance) + the **INT-modifier** bonus skills ([Phase 2](2026-06-13-phase2-character-framework.md)).
  - **Unarmed** attacks and **unarmored** defense: **Trained**; plus additional **weapon** and **armor** categories per class balance.
  - **Class DC:** **Trained.**

**Over levels (the class table defines):**
- The levels at which **Perception, class DC, saving throws, armor, and weapon** proficiencies **rank up**.
- The cadence of **skill increases** (assignable skill-rank boosts) and **skill feats**.
- When class features / the class verb upgrade (Phase 5 chassis; Phase 3 no-dead-levels floor).

---

## 4. The Creation Attribute-Boost Model

Total starting boosts come **only** from **Background (2) + Species (net +2) + Class (1)** — **no separate "free boost" pool** *(deliberate deviation from PF2E's four free boosts; it is what holds our key stat to the bounded **+3 creation cap** vs PF2E's +4)*.

**Rules:**
- **Same-source boosts must target different attributes** (PF2E-inherited). A background can't put both its boosts on one attribute; species free boosts likewise spread.
- **Key-stat creation cap: +3** (Phase 2). Reached as class (+1 key) + one background boost (+1 key) + species (+1 key); the same-source rule + species' ±1 limit make +4 unreachable at creation.
- All attributes start at **+0** before boosts.

**Worked example** — CHA-key class, Politician background, free-boost species:
| Source | Boosts |
|---|---|
| Class | +1 CHA (key) |
| Background (Politician) | +1 CHA (constrained: INT/CHA) · +1 DEX (free, must differ) |
| Species (free) | +1 CHA · +1 CON (must differ) |
| **Array** | **CHA +3**, DEX +1, CON +1, rest +0 |

Focused and tighter than a PF2E starting array (one +3, a couple of +1s) — by design.

---

## 5. Consistency Reconciliation — Initial Proficiency vs the Rank Gates

The [Phase 3 §5](2026-06-13-phase3-progression-chassis.md) gates (**Expert L3 / Master L7 / Legendary L15**) refer specifically to **player-assignable Skill boosts** (the skill-increase track) and are the **hard Master/Legendary caps** for everyone. They do **not** restrict a class's level-1 *floor*: starting Perception or a Save at **Expert is core to the system** (it's how classes read as "good" vs "bad" at each), and **no class starts Perception or any Save Untrained.**

**A class's *initial* proficiencies are set by its table and may start as high as Expert at level 1** in core/signature areas (Perception, a save, a weapon group) — this does **not** violate the gates, which restrict the *advancement track* and the *Master/Legendary* ceilings, not a class's level-1 floor. *(Phase 3 §5 wording amended to say so.)*

**Gate-A note:** a class that grants **Expert** in a proficiency at level 1 also gains that proficiency's **rank-gated effect** at level 1 (e.g., Expert weapons → critical specialization). That is a deliberate, balanceable class-design choice (the class's identity), validated at Gate A — not an exploit.

---

## 6. Carried Forward

- **Specific Backgrounds, Species (with their boosts/senses/speeds/HP/feats), and Classes** → Phase 8 content.
- **Per-class starting-proficiency tables and advancement schedules** → authored with each class (Phase 5 slice classes already conform; full roster Phase 8).
- **Languages list, size categories, sense types** → Phase 8 / rules-writing.

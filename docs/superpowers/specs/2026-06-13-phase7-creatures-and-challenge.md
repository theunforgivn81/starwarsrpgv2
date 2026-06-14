# Phase 7 — Creatures & Challenge Framework

**Status:** Approved
**Date:** 2026-06-13
**Roadmap phase:** 7 of 9 — see [build roadmap](../plans/2026-06-13-star-wars-rpg-build-roadmap.md)
**Upstream:** [Philosophy](2026-06-13-star-wars-rpg-design-philosophy.md), [Phase 1 (§2.2 symmetric L, §11 engagement)](2026-06-13-phase1-core-mechanic-and-traits.md), [Phase 2](2026-06-13-phase2-character-framework.md), [Phase 3](2026-06-13-phase3-progression-chassis.md), [Phase 4](2026-06-13-phase4-social-intrigue-engine.md), [Phase 5](2026-06-13-phase5-class-design-and-force.md), [Phase 6](2026-06-13-phase6-equipment-and-economy.md)
**Resolves:** Pillar 1 at the enemy layer (threat via HP/abilities, not climbing to-hit); closes the deferred **creature-building math**; completes the **vertical slice** (PC side + opposition).

> *(Gate A)* = provisional pending balance calibration. The framework and method are fixed; numbers are illustrative.

---

## 1. Build Method — to a benchmark, on the L-spine

A creature of level *N* scales on **L(N) = 1 + (N ÷ 4)** (Phase 1 §2.2), but its offsets are tuned to **hit-rate targets**, not PC build math (creatures are *experience devices*, not characters).

### 1.1 Benchmark table (provisional — Gate A)

| PC Level | PC attack | PC AC | PC HP | Save DC |
|---|---|---|---|---|
| 1 | +5 | ~16 | ~18 | ~16 |
| 3 | +6 | ~18 | ~35 | ~17 |
| 5 | +8 | ~20 | ~55 | ~19 |

### 1.2 Standard on-level creature targets
- **PCs hit it ~60%** → its AC sits *below* PC AC (e.g. ~17 at L5).
- **It hits PCs ~60%** → its attack sits *above* PC attack (e.g. ~+11 at L5).
- Two-sided floor: never let PCs hit below ~40% (slog) or the creature hit below ~50% (toothless).

### 1.3 Why the asymmetry is correct (the bounded-accuracy demonstration)

Creatures carry *higher attack and lower AC* than same-level PCs. Because **L(N) appears on both sides and cancels on-level**, the **offsets — and thus hit *and* crit rates — are constant at every level.** Therefore:
- A higher-level creature is *not* harder to hit on-level; it threatens through **more HP, more damage, and nastier abilities.**
- Cross-level is a **gentle slope**: a L5 creature hits L1 PCs ~80% (not 100%) and L9 PCs ~45% — never the unhittable wall of unbounded systems.

This is the entire bounded-accuracy enemy thesis, falling straight out of the Phase 1 spine.

### 1.4 Derived numbers
- **HP** = (party DPR) × (intended rounds the creature survives).
- **Damage/round** = **lethality constant** × PC HP (§2).
- **Saves/DCs** = `L(N) + role offset` (good/poor by role), tuned to the benchmark.

---

## 2. Lethality Constant (the deadliness dial — a design constant)

- **Standard on-level creature removes ~15% of a PC's HP per round; a boss ~30% (spread across targets).** *(Gate A exact.)*
- A focused PC drops in ~4–5 rounds of incoming fire — tense, not brutal; fits the per-encounter recovery model and the "not brutal/slow" steer.
- **Melee's higher damage and `[deadly]` crits spike above this** (the §11 risk/reward); ranged sits at baseline.
- Every creature inherits this constant; deviating is a deliberate role choice (Artillery higher, Brute slower-but-harder, etc.).

---

## 3. Creature Roles

Same threat budget, different fights (mix 2–3 per encounter):

| Role | Build | Function in our system |
|---|---|---|
| **Minion** | 1–2 hits; real damage | makes **grenades & Suppression** matter; dies visibly |
| **Standard** | benchmark | the encounter-math unit |
| **Elite** | ~2× HP/threat | lieutenant; pressures focus-fire |
| **Solo/Boss** | 4×+ HP, multiplied actions | §4 |
| **Artillery** | low defense, high ranged damage | punishes turtling |
| **Controller** | debuffs/zones | changes PC decisions, not HP |
| **Skirmisher** | mobile, hit-and-run | punishes static lines; **forces the Reactive-Shot/positioning game** |
| **Brute** | high HP/damage, low accuracy | the wall; closes to melee (and eats Reactive Shots — the "safe to charge" melee case) |

---

## 4. Boss Engineering (the solo action-economy problem)

A solo boss faces 4+ PC turns/round with one of its own; unprotected, it is focus-fired and deleted. Our model (no daily resources to lean on):

- **Boss Actions (1–2/round):** taken on *PCs'* turns (legendary-action style) — Stride, a Strike, or a short ability — restoring action parity. Reset each round.
- **Phases (HP thresholds):** the fight changes (new ability, terrain shift, ranged mode) — resets PC momentum and **masks the HP slog**.
- **Condition resilience:** the *first* action-denial each round is **downgraded** (stun → slowed), **not negated** — so controllers/the Technician still act (no blanket immunity).
- **Nova check:** if a perfect party alpha-strike removes 60%+ of boss HP in round 1, **phase-gating is mandatory** (our showcase boss passes).
- A boss uses **≥2** of these; bosses may also field **adds** and **lair actions**.

---

## 5. Signature Abilities & Behavior

- **1–2 signatures** per creature above minion; the benchmark is the chassis, the signature is the identity. A signature must **change PC behavior**, be **telegraphed**, and is **paid for in chassis** (lower HP/damage). Cap specials at **3–4**, organized by trigger.
- **Behavior script (3 lines):** opener · target priority · break condition. **Morale/break conditions** are mandatory — creatures that sometimes flee or yield make outcomes richer than binary TPK-or-loot.

---

## 6. Social Layer (Phase 4 integration)

Any creature that can talk gets the **social block**: **Want** (current goal), **Off-ramp** (what ends the encounter without violence and its cost), **Leverage** (what it fears/bargains with), plus the Phase 4 social-defense numbers — **Resolve, Will DC (for Composure attacks), situational Levers/Guards.** A social pillar with no statted NPCs is unsupported; this is where NPC social stats live.

---

## 7. Unified Stat Block Template

```
NAME — Level N — [traits: type, faction…] — Role
Perception +X; senses
AC X; Fort/Ref/Will +X; HP X; (immunities / resistances / weaknesses)
Speed X
Strikes: melee/ranged +X (damage, traits)
Signature (1–2, by trigger): …
[Boss] Boss Actions (1–2/round, on PCs' turns); Phases (HP thresholds); Condition resilience
Tactics: opener · target priority · break condition
[If it can talk] Want · Off-ramp · Leverage · Social: Resolve X, Will DC X, Levers/Guards
Rewards: credits / special item / story access
```

---

## 8. Slice Roster (L1–5, role-mixed)

| Creature | Lvl | Role | Hook |
|---|---|---|---|
| **Gang Thug** | 1 | Minion/Standard (ranged) | blaster goon; minion dies in 1–2 hits (grenades/Suppression shine) |
| **Stormtrooper** | 2 | Standard (ranged) | *Squad Tactics* (allies firing the same target get a bonus → PCs spread/break the squad) |
| **Gamorrean Enforcer** | 2 | Brute (melee) | high HP/damage, low accuracy; closes and **eats Reactive Shots** — §11 from the enemy side |
| **Combat Droid** | 3 | Standard/Artillery `[droid]` | immune `[mental]`/`[emotion]`, **weak to ion** — trait immunity/weakness demo |
| **Nexu** | 3 | Skirmisher (beast) | *Pounce/Withdraw*; punishes static lines, rewards readied actions |
| **Bounty Hunter** | 4 | Elite (ranged + gadgets) | pressures focus-fire; **full social block** (can be bought off) |
| **Inquisitor** | 5 | Solo/Boss (Force) | the showcase — §9 |

### 9. Boss showcase — the Inquisitor (L5)

**Signature — Deflect Blaster Bolts** (the enemy mirror of the Guardian's stance): negates/reduces ranged Strikes, so the party's *ranged default stops working* — forcing melee (the risky game), ion/grenades, or their own Force user. A signature that **changes PC behavior** and teaches §11 from the other side.

- **AC ~18 — PCs still hit ~55%** (NOT unhittable); staying power is **HP + Boss Actions + phases**, not a wall of AC. *(The bounded-accuracy demonstration.)*
- **Boss Actions (2/round):** Stride / saber Strike / *Force Shove* on PCs' turns.
- **Phase 2 (≤50% HP):** hurls the saber (ranged mode), gains a second deflection, terrain shifts.
- **Condition resilience:** first action-denial/round downgraded (stun → slowed).
- **Nova check:** phase-gating prevents a >60% round-1 burst. ✔
- **Social:** a fanatic — a `[Guard]` vs all appeals (can't be talked down), so the *roster* exercises Phase 4 via the Bounty Hunter / crime-tier NPCs instead.

---

## 10. Rewards & Slog Control

- **Intended rounds by role:** minion 1–2 · standard ~2 · elite ~3 · boss ~4–5 (phases mask it) — keeps fights off the HP-slog cliff (the Phase 3 risk).
- **Rewards:** credits + **pillar-neutral XP** (Phase 3) + occasional **signature loot** (the Inquisitor's kyber crystal; a mod). Check against **wealth-by-level** (Phase 6) so a generous drop doesn't break the economy two levels later.

---

## 11. Exit-Gate Checklist (per roadmap)

- [x] Stat-block template (trait-tagged; combat + social) (§7).
- [x] Challenge math under bounded accuracy; enemy scaling via HP + abilities, near-flat attack/defense offsets (§1).
- [x] Monster roles defined; encounters mix roles (§3).
- [x] Boss model: 2+ action-economy compensations; nova check (§4, §9).
- [x] A handful of slice creatures across a small level range (§8).
- [x] **Bounded-accuracy demonstration:** a higher-level enemy (Inquisitor) threatens via durability/abilities, not unhittable defenses (§9).
- [x] Social-defense numbers on talking creatures (§6) — Phase 4 supported.
- [x] **Vertical slice complete** — PC content (Phases 5–6) + opposition (Phase 7) can run a real session.

---

## 12. Carried Forward (open items)

- **All numbers** (benchmark table, role offsets, HP/damage by level, boss action budgets, lethality exact, reward values) → **Gate A** (`ttrpg-balance-analysis`).
- **Full bestiary, vehicle/starship-scale combatants, hazard/trap stat blocks, more bosses & phases** → Phase 8.
- **Encounter-building budget rules** (how many creatures of which roles per party level/tier) → finalized at Gate A and expanded Phase 8.

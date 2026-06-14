# Connective Tissue & System-Review Remediation

**Status:** Approved
**Date:** 2026-06-13
**Type:** Post-Phase-7 system-review remediation (not a roadmap phase)
**Upstream:** all Phase 0–7 specs; audited with `ttrpg-system-review`.
**Resolves:** the seven Significant load-bearing gaps (S1–S7) found in the vertical-slice review. Cosmetic findings (C1–C6) are parked.

---

## A. System-Review Summary (slice, Phases 0–7)

- **No Critical show-stoppers.** No action-positive/loop engines, no load-bearing contradictions. The Reactive-Shot's melee-only trigger structurally forecloses reaction loops (a reaction Strike is ranged, and ranged Strikes never provoke).
- **7 Significant gaps (S1–S7):** rules the slice *assumed* but never wrote — resolved below.
- **6 Cosmetic (C1–C6):** parked (§C).
- **Passes 4–5 (power-outlier / dead-content)** deferred as premature (4 hand-tuned classes, no numbers) — revisit after Gate A + content expansion.

---

## B. Resolutions

### S1 — Stealth & Detection *(adopt Paizo ORC)*

Adopt PF2E's detection framework (ORC-licensed; §E):
- **Detection states** (observer → target): **Observed · Concealed** (DC 5 flat to target it) **· Hidden** (DC 11 flat) **· Undetected · Unnoticed.**
- **Cover:** lesser **+1**, standard **+2** (can Take Cover; enables Hide), greater **+4** — a **circumstance** bonus to AC (consistent with Phase 1).
- **Actions:** Hide, Sneak, Seek, Point Out; Stealth vs Perception DCs (our DC ladder; flat checks 5/11 as ORC).
- **Bindings to our system:**
  - An **Undetected or Hidden** attacker's target is **Off-Guard** to it → powers the Scoundrel's **Exploit** and "strike from concealment."
  - An attack by an attacker the target **can't perceive** does **not** provoke a **Reactive Shot** (the "target unaware can't react" counter, §11) → makes melee-from-stealth safe.
  - Feeds initiative (S3).

### S2 — Dying & Wounded *(adopt Paizo ORC)*

- At **0 HP** you're knocked out and gain **Dying 1** (Dying 2 if reduced by a critical hit; +your current **Wounded** value).
- **Dying X:** unconscious; at the start of each of your turns make a **recovery check** (flat DC `10 + Dying`): crit success −2 Dying · success −1 · failure +1 · crit failure +2. **Dying 4 = dead.**
- **Wounded X:** gained/incremented each time you recover from Dying; adds to future Dying values; cleared only by full recovery (downtime/extended care).
- **Stabilize / First Aid** (Medicine, in combat) sets Dying to 0 (still unconscious at 0 HP; Wounded persists). HP above 0 wakes you (Wounded remains).
- **No hero points** — the recovery check is the lifeline; the **moderate lethality dial** (Phase 7) is balanced around this.
- *(Massive-damage instant-death threshold, if any → Gate A.)*

### S3 — Initiative & Encounter Start *(adopt Paizo ORC)*

- At encounter start each participant rolls **initiative** — usually a **Perception** check; the GM may call a relevant skill (e.g., **Stealth** when sneaking, which *also* sets the roller's detection state, S1).
- Order **highest-first**; ties → PCs before NPCs (or GM choice).
- **No separate surprise round.** Ambush = **Stealth-for-initiative + Undetected** (S1): sneaks who beat their foes act first while Undetected, with **Off-Guard** targets on the opening Strike. Surprise is unified with the stealth system.

### S4 — Scene vs Encounter *(keyword definitions; corrects reset language)*

- **Scene:** any scenario containing specific challenges for the players (a discrete chunk of play with stakes).
- **Encounter:** a **subcategory of Scene** — a structured, initiative/exchange-based challenge: a **combat encounter** or a **social encounter**. A Scene may contain several Encounters.
- **Reset bindings (authoritative):**
  - **Attunement** and **encounter-scoped pools** reset **at the end of each Encounter** (per fight / per social exchange) — *corrects* the earlier "scene end" wording (Phase 3 §7, Phase 2 §5 amended).
  - `[once per minute]` / `[once per hour]` reset by **elapsed time**; `[once per day]` on a **full rest**.
  - Scene-level tools (e.g., the optional **Suspicion clock**, Phase 4) persist across a Scene's Encounters.

### S5 — Reaction Timing & MAP *(codified)*

- A **reaction resolves immediately when its trigger occurs**, per the **exact wording** of the trigger. Standard trigger points: **when targeted** by an attack · **when hit** (after the attack is confirmed a hit, before damage) · **after damage is dealt**.
- **Reactive Shot** triggers on "*a creature you can perceive makes a melee Strike while within 10 ft of you*" (revised per playtest F2 — any nearby gunner, not just the target) — i.e. when the Strike is **declared** (before it resolves), so the Reactive Shot resolves first and can **disrupt** it (dropping/disabling the attacker can cause the Strike to be lost).
- **MAP never applies to reactions** — a reaction Strike is at full accuracy and does not raise your MAP.
- A reaction spends your **one reaction/round** unless an ability grants more (the Soldier's *Reactive Volley*). Suppression's Reactive Shot spends your reaction normally.

### S6 — Force Powers & Class Abilities in Social Encounters *(codified)*

- In a **social encounter**, **Force powers and other class abilities** may be used as **1- or 2-action social activities**, action cost set by what they accomplish.
- They **act *within* the engine, never bypass it** (Pillar 5): a "mind trick" is a strong **appeal** (e.g., a 2-action appeal that may ignore a Guard, or hit a `[mental]`-susceptible target harder) — it does **not** auto-resolve the scene.
- Targets immune/resistant to the relevant trait (droids vs `[mental]`/`[emotion]`; a Guarded fanatic) resist accordingly (S7). The Influence discipline is thus first-class in social *without* deleting the challenge.

### S7 — Trait Immunity Semantics *(codified)*

- **Immunity to a trait grants immunity to the *entire* ability bearing that trait**, including all knock-on effects (damage, forced movement, riders).
- Example: a `[droid]` immune to `[mental]` is **wholly unaffected** by a `[mental]` power, even one that also deals damage.
- **Design implication:** to apply *part* of an effect to immune targets, split it into separate abilities/traits. Authors of Force powers and grenades must keep this in mind.

---

## C. Cosmetic / Minor — parked for later revisit

| # | Issue |
|---|---|
| C1 | Phase 1 §6.2's prose AC formula predates the armor-base term (reconcile wording). |
| C2 | Blaster **ammo** abstraction undefined (infinite? power packs / `[reload]` only?). |
| C3 | **Dual-wielding** rules undefined (two blasters / two melee + MAP). |
| C4 | Combat→social **de-escalation** (reverse escalation bridge) undefined. |
| C5 | Social **stalemate** resolver (both sides only Defuse/Stand Firm). |
| C6 | **PC-vs-PC** edge (Force/social used on an ally) undefined. |

---

## D. Re-Audit (fix-discipline — Passes 1 & 3 on touched areas)

- **Pass 1 (terminology):** new keywords registered — Observed/Concealed/Hidden/Undetected/Unnoticed, cover degrees, Dying/Wounded, Scene/Encounter. No near-synonyms introduced (reused Off-Guard, circumstance bonus, Reactive Shot, MAP).
- **Pass 3 (interactions):** stealth×combat now defined (S1+S3+S5); Force×social defined (S6); immunity×multi-component defined (S7); reaction timing/ordering defined (S5). No new contradictions; reaction-loop foreclosure preserved.

---

## E. Licensing Note

S1–S3 adapt Paizo **ORC**-licensed content (PF2E stealth/detection, dying/wounded, initiative) — within the [Philosophy §0](2026-06-13-star-wars-rpg-design-philosophy.md) allowance. Mechanics are paraphrased in our own words and bound to our DC ladder, recovery model, and Reactive-Shot rules; the required ORC notice/attribution travels with any published text.

---

## G. Forced Movement & Hazards *(playtest F3 — system-wide rule)*

Surfaced by the F3 exploit (a cheap repeatable shove-off-a-ledge). Applies to **every** push/pull effect (Telekinetic Nudge, the Inquisitor's Force Shove, grenade knockback, future feats):

- Forced movement specifies a **distance and direction** and **does not provoke reactions** (it isn't the moved creature's action).
- **Default — stop at the brink:** if forced movement would carry a creature **off a precipice or into a hazard**, the creature **stops at the edge** (it is *not* pushed in). Forced movement is therefore **never a free instakill**.
- **"Hurl" exception:** only an effect that *explicitly* states it can hurl a target off/into a hazard may do so, and the target then attempts a **basic Reflex save** (vs the effect's DC) to stop at the brink anyway — falling/entering only on a failure.
- **Obstacles:** forced movement into a solid obstacle stops the creature adjacent to it (collision damage only if the effect says so).
- **Falling / hazard damage** resolves per its own rules *(falling-damage values → Gate A / rules-writing)*.

This immunizes all displacement effects against the F3 class of exploit at once. Combined with the **F3 economy rule** (offensive Force costs Attunement → no free spam, [Phase 5 §2.2](2026-06-13-phase5-class-design-and-force.md)), Telekinetic Nudge can neither be spammed for free nor instakill.

### Sources of forced movement (balanced by access cost)

At-will, zero-cost forced movement **still exists** — it just isn't free *and* ranged *and* repeatable at once:

| Source | Cost | Gated by | Roll |
|---|---|---|---|
| **Athletics: Shove / Reposition** | free, at-will | `[attack]` (incurs **MAP**); **melee-only** (closing provokes Reactive Shots) | Athletics vs target's **Fortitude DC**; push 5 ft (10 ft on crit) |
| **Telekinetic Nudge** (Force) | **1 Attunement** | ranged & safe | target's **Fort save** vs Force DC; same distances |

Same effect, different price: the mundane version pays in *exposure + MAP*; the Force version pays in *Attunement* for doing it at range. Both obey the stop-at-edge rule above.

---

## H. Carried Forward

- **C1–C6** cosmetic fixes.
- **Numbers** (recovery-check DCs already fixed by ORC; massive-damage threshold; flat-check tuning) → Gate A.
- Full condition catalogue (now including the detection states) → consolidate in rules-writing.

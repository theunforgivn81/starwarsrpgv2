# Lightsaber Forms — the Stance System (shared layer)

**Status:** Designed. The seven base Form stances + the chain/portability framework. Full **chain feats** are authored with the Guardian class feats; subclasses (Form specializations) build on this.
**Date:** 2026-06-18
**Type:** Content design — a **shared martial layer** (like the [Force toolkit](2026-06-15-shared-force-toolkit.md) is the shared *power* layer). Mapped, not ported, from the prior `ClassFeat` Form chains under our bounded system.
**Upstream:** [Guardian](2026-06-18-class-guardian.md) (the masters), [Phase 1 core mechanic](2026-06-13-phase1-core-mechanic-and-traits.md) (MAP, circ bonuses, conditions), [Subclass sketch §1](2026-06-15-subclass-roster-sketch.md).

---

## 1. Principle

Forms are the **shared lightsaber-combat vocabulary** — a stance system any lightsaber user can learn, that the **Guardian masters**. They are the *martial* counterpart to the Force toolkit's *powers*: the Guardian bridges both (Blade-Flow). This mirrors the toolkit's portability rule — *a class owns its verb-framework, not the iconic vocabulary* — so Forms are feat-gated and portable, and the Guardian is their specialist.

- **Forms are martial, not Force:** entering a Form costs **1 action** and **no Attunement** (it requires a lightsaber, not the Force). Attunement stays reserved for Force powers — so a Guardian flows between blade Forms *and* telekinetic powers without the two competing for the same resource.

---

## 2. How Forms Work

- A Form is a **`[Form]` `[Stance]` feat**. The base feat grants a **Stance action**: **`[1 action]`**, **requirement: wielding a lightsaber**, enter the stance.
- **One stance at a time.** Entering a Form ends any current stance; you **switch Forms mid-combat** freely (1 action each). The stance lasts until you leave it, are knocked out, or stop wielding a lightsaber.
- Each Form has a **while-in-stance effect** + a **`Guardian Mastery`** clause that upgrades it (see §4 portability).
- Each base Form **anchors a chain** of prerequisite-gated follow-up feats (Strikes, activities, stance upgrades) — authored with the [Guardian class feats](2026-06-18-class-guardian.md); §3 lists one example each.
- **Bounded by design:** Form effects are circumstance bonuses (+1/+2), conditions (off-guard), or positioning — never level-scaling numbers. They stack with nothing of the same type (circumstance), keeping the math flat.

---

## 3. The Seven Forms (base stances)

All: `[1 action]`, `[Form]` `[Stance]`, requirement *wielding a lightsaber*. **GM** = Guardian Mastery clause.

| Form | Role | While in stance | **Guardian Mastery** | Sample chain feat |
|---|---|---|---|---|
| **I — Shii-Cho** | multi-target | Your lightsaber Strikes gain **Sweep**: +1 circ to attack a creature if you've already Struck a *different* creature this turn. | Strikes against a creature you **haven't attacked this turn** don't accrue or suffer **MAP** (so spreading blows stays accurate). | *Cyclone* — a 1-action Strike against each adjacent enemy at your current MAP. |
| **II — Makashi** | duelist *(one-handed, free hand)* | Designate a **Dueling Target** (free action to change, or when it drops): **+1 circ AC vs that target's attacks**. | Once per round, **Feint** your Dueling Target as a **free action** (sets up off-guard → Counter/precision). | *Contentious Riposte* — reactive Strike when your Dueling Target misses you. |
| **III — Soresu** | defense / Deflect | **+2 circ AC vs ranged Strikes**; Speed −10 ft. | The AC bonus also applies **vs melee** (the eye-of-the-storm). | *Deflecting Wall* — your Deflect protects an adjacent ally too. |
| **IV — Ataru** | mobility | You can **Tumble Through** enemies' spaces (even larger); on a success they're **off-guard** to your attacks until end of turn. | **+10 ft status Speed**; you **don't provoke reactions** when you Move. | *Hawk-Bat Swoop* — Leap + a mid-air Strike (+1 weapon die); GM: a second Strike at −5. |
| **V — Shien / Djem So** | counterattack | **+2 circ damage** with two-handed lightsaber Strikes. | Hit by **melee** → +2 circ to your next attack vs that foe; hit by **ranged** → +2 circ AC vs that foe's ranged attacks for 1 round. | *Returned Fury* — when you Deflect/Intercede, your next Strike vs that foe gains +2 circ damage. |
| **VI — Niman** | blade↔Force balance | A successful lightsaber Strike → **+1 circ** to your next **Force power's DC/attack** (until end of next turn). | The synergy reverses: using a **Force power** → +1 circ to your next lightsaber Strike. | *Balanced Flow* — enter Niman as a free action when you Center. |
| **VII — Juyo / Vaapad** `[dark]` | reckless aggression | **−1 AC**, **+1 circ to attack rolls** (open to the chaos of battle). | The attack bonus increases to **+2**. | *Vaapad Surge* `[dark]` — convert the AC penalty into bonus damage on a hit. |

*(Roles cover the offensive/defensive spread so a Guardian's Form choice is a real tactical read: Soresu to weather fire, Ataru to reposition, Djem So to punish attackers, Makashi to lock down one foe, Shii-Cho vs a crowd, Niman to chain blade-and-power, Juyo to gamble. `[dark]` Juyo hooks the deferred corruption subsystem.)*

---

## 4. Portability & Access (the Guardian Mastery gate)

Same pattern as the Force toolkit — Forms are shared, mastery is the Guardian's:

- **Guardian** — gains a **signature Form** (its subclass's base stance) free at L1, learns more Forms + chain feats via **class feats**, and **always benefits from every `Guardian Mastery` clause** (its **Blade-Flow** feature *is* Form mastery). The Guardian also flows between known Forms freely.
- **Consular** — leans on **Niman** (the blade↔Force Form); can learn base Forms via feats. **Base effect only** (no Mastery) unless a feat grants it.
- **Force Adept / other lightsaber users** — may learn a **base Form** via the archetype; base effect only.
- **The Mastery clause activates only for those with Form mastery** (Guardians, or a rare archetype capstone). This is the "Guardian Mastery makes Forms portable" rule generalized: others get the *stance*, the Guardian gets the *stance + upgrade*.

---

## 5. Balance & Design Notes

- **Bounded:** every base effect is a circ bonus, a condition, or positioning — no scaling numbers. Stances don't stack (one at a time); circumstance bonuses don't stack with same-type.
- **Shii-Cho Mastery re-peg:** the prior "ignore MAP entirely" became "Strikes vs **new** targets don't accrue/suffer MAP" — preserves the multi-target fantasy, naturally bounded by enemy count. *(Gate-A: confirm vs the Soldier's reduced-MAP-vs-suppressed.)*
- **Deflect synergy:** Soresu (defense) and Shien/Djem So (counter) pair with the shared **[Deflect](2026-06-15-shared-force-toolkit.md)** power (now defined — Control school, Basic/0) — the Guardian's Lever-B self-mitigation; Soresu's Mastery extends Deflect's AC swing to melee.
- **Niman ↔ Consular:** Niman is the concrete proof of portability — the Consular's favored Form, used at base while the Guardian masters it.
- **`[dark]` Juyo/Vaapad:** the reckless Form is the lightsaber-side hook for the corruption subsystem (parallel to the toolkit's `[dark]` powers).
- **Action economy:** 1 action to enter + free mid-combat switching means stance choice is a live tactical decision, not a set-and-forget — central to the "not Strike ×3" goal.

---

## 6. Carried Forward

- **Full chain feats** (≥3 per Form) → authored with the [Guardian class feats](2026-06-18-class-guardian.md) (§6) and shared/archetype feats.
- **Guardian subclasses** = Form specializations (Soresu/Ataru/Djem So/Makashi/Niman) → next, building on §3.
- ~~Slot the basic `Deflect` power into the Force toolkit~~ — **DONE:** [toolkit Control school](2026-06-15-shared-force-toolkit.md), Basic/0.
- **Gate-A:** Shii-Cho MAP clause, Juyo risk/reward, Niman double-dip with Force powers, cross-Form switching tempo.

# Lightsaber Form Design Philosophy

**Status:** Approved (2026-07-11) — not yet implemented. Governs the pending SQL-dump re-analysis and the rebuild of the Form feat chains.
**Date:** 2026-07-11
**Type:** Design philosophy. Sets the principles for how lightsaber Forms and their feat chains are structured, how faithful they stay to the source fiction, and how the Guardian subclass integrates with them. Does **not** specify the concrete techniques — that is the output of the dump re-analysis this doc authorizes.
**Upstream:** `docs/player-core/the-force.md` §Lightsaber Forms (current chains, to be rebuilt); `docs/player-core/classes/guardian.md` (subclass ladder); [Consular Mandate Rework](2026-07-05-consular-mandate-rework.md) (the grant-table/decoupling pattern this mirrors).
**Downstream:** SQL-dump re-analysis → rebuilt Form chains in `the-force.md` → Guardian Form subclass restructure in `guardian.md`.

---

## 1. Problem

The Form feat chains currently in `the-force.md` are mechanically clean but **thin** — each Form is a stance feat plus a 3–4 feat menu capped around Feat 8–10 — and in slimming them we discarded most of the source fiction's named-technique vocabulary (Sun Djem, Sokan, Falling Avalanche, Sarlacc Sweep, and the rest). The techniques had roots in the fiction; very little of that survived. This philosophy fixes the target the rebuild aims at before we re-open the dump.

---

## 2. Principles

### 2.1 Two layers, one canon

Forms live in two places, with a strict ownership rule:

- **The universal Form chains (`the-force.md`) are the heart and soul.** They hold the full, fiction-rooted expression of each Form and are open to any lightsaber user (a Consular favoring Niman, a Sentinel who dips a Form).
- **The Guardian subclass ladder (`guardian.md`) is expansion and improvement layered onto those same chains** — never a parallel system. The Guardian masters what the chains already contain.

### 2.2 Fidelity — canon leads, mechanics adapt

Each chain's backbone is the Form's **canonical named techniques**, re-stated freely into our ORC/2E substrate. We keep the recognizable names and their fictional feel; we bend the numbers to fit our frame (flat effects, our action economy). Breadth of recognizable named moves is itself a goal, delivered **across the seven chains** rather than by a wide menu inside any one Form.

### 2.3 Structure — linear mastery, four rungs

Each Form is a **linear prerequisite chain**, not a grab-bag menu:

> **Stance → Technique A → Technique B → Signature**

Each rung requires the one before it. Fewer parallel picks; a real sense of earned mastery with a gated payoff (the Signature) at the top. A dabbler can climb a rung or two; only real investment reaches a Form's signature move.

**Count:** 4 feats per Form (the stance is the first rung). Seven Forms → **7 stances + 21 named techniques.**

### 2.4 Level schedule — the Guardian rides a step ahead

| Rung | General access | Guardian (free) |
|---|:---:|:---:|
| Stance | Feat 2 | Level 1 |
| Technique A | Feat 4 | Level 3 |
| Technique B | Feat 8 | Level 7 |
| Signature | Feat 14 | Level 13 |

A Form is a career-long path whose signature technique lands in the high teens (Feat 14), not at Feat 8. The Guardian receives each rung **one level early and for free** on their signature Form, mirroring how a Consular Mandate hands over its powers on a fixed schedule.

### 2.5 Guardian Mastery

Each granted rung carries its **Guardian Mastery** upgrade (masters only; a dabbler gets the base technique). This is unchanged from the current model — the Guardian gets the stance *and* its mastery clause on every rung.

---

## 3. Guardian integration (mirrors the Consular decoupling)

The Consular Mandate rework decoupled *grants* from *mechanics*: each Mandate opens with a **Mandate Powers** table (`Level | Power`) that hands over powers on a schedule, and that table sits above the untouched levelled features, which are pure mechanical riders. The Guardian mirrors this exactly.

Each Guardian Form subclass writeup gains a **Form Feats** table at the top:

| Level | Feat |
|:---:|---|
| 1st | *(Stance)* |
| 3rd | *(Technique A)* |
| 7th | *(Technique B)* |
| 13th | *(Signature)* |

**The table sits on top of, and does not replace, the subclass's levelled features.** The Guardian's bespoke ladder (Resolute Guard, Sheltering Intercede, Deflecting Wall, … on its 1/3/7/11/15/19 schedule) stays exactly as it is. The grants add to the ladder; the ladder improves what the grants gave.

The only changes to the Form subclass writeups are therefore:

1. **Add** the Form Feats grant table at the top.
2. **Strip** the now-redundant "you gain the *Cyclone* feat" style grant-clauses out of the levelled features (the table owns grants now), leaving those features as pure mechanical benefits — the same cleanup the Consular already went through.

The levelled-feature *schedule* is unchanged; no feature is deleted for being a grant, only rewritten to drop the grant text it no longer needs to carry.

---

## 4. Carried-over guardrails (unchanged)

- **Martial, not Force.** Entering a Form is one action and costs no Attunement; it asks only that you're wielding a lightsaber. Blade and Force never compete for the same fuel.
- **One stance at a time,** freely switchable mid-combat (one action each, or free via Blade-Flow for the Guardian).
- **Flat effects only** — circumstance bonuses, conditions, positioning. Never level-scaling numbers, so Form effects don't stack with same-type bonuses.

---

## 5. Consequences to honor in implementation

- **The stance moves from Feat 1 → Feat 2** for non-masters. Only Guardians (and rare archetypes) enter a stance at level 1, via the Form Feats table. This is a deliberate sharpening of the Guardian's "Form master" identity, but a real change from today's Feat-1 stances.
- **`the-force.md` §Lightsaber Forms is fully rebuilt.** The current 3–4-feat menus are replaced by 4-rung linear chains. Existing chain feats (Cyclone, Hawk-Bat Swoop, Contentious Riposte, etc.) are candidates for slots in the rebuilt chains, not guaranteed survivors.
- **`guardian.md` Form subclasses get the §3 treatment** (add grant table, strip grant-clauses). This is the continuation of the paused Guardian review/revision, now driven by this philosophy.
- **Appendix discipline (per CLAUDE.md):** any trait or condition a rebuilt technique introduces must get an entry in `appendix-traits.md` / `appendix-conditions.md` in the same change.

---

## 6. What this drives next

1. **SQL-dump re-analysis** — mine the dump Form-by-Form for the canonical named techniques, sort them into the four-rung linear shape (stance / A / B / signature) per Form, and re-stat each into the substrate.
2. **Rebuild `the-force.md` §Lightsaber Forms** from that analysis.
3. **Restructure the seven Guardian Form subclasses** per §3.

Each step gets its own plan/implementation cycle; this doc is the lens all three read through.

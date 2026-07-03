# Appendices — Traits & Conditions

**Date:** 2026-07-03
**Status:** Approved
**Type:** Content design. Creates the two reference appendices mandated by [Phase 1 §8](2026-06-13-phase1-core-mechanic-and-traits.md) (the "master trait glossary") and its §8.5 ("the standard condition list is content for a later phase" — this is that phase).
**Upstream:** Phase 1 (trait system, modifier architecture), [feat entry format](2026-06-26-feat-entry-format.md), [activated-ability formats](2026-06-27-activated-ability-formats.md).

---

## 1. Deliverables

Two new player-core chapters (eventual book appendices):

| File | Contents |
|---|---|
| `docs/player-core/appendix-conditions.md` | Intro rules + full alphabetical condition list |
| `docs/player-core/appendix-traits.md` | Intro rules + single alphabetical trait glossary |

Unnumbered kebab filenames (matching `the-force.md`); appendix ordering is a book-assembly concern, not encoded in filenames.

**Source-text rule (user directive):** any condition or trait that exists in the ORC-licensed 2E core rules uses that text, adapted per §4. Project-original entries get original text.

## 2. Conditions appendix

### 2.1 Structure

1. **Intro:** what a condition is; condition **values** (`frightened 2`) and how they decrease; conditions with the same name don't stack (highest value / most severe applies); condition penalties are **status** penalties unless stated otherwise (tying into Phase 1 §4.1); **groups that interlock** get a signpost (death & dying; the detection ladder).
2. **Alphabetical entries**, one per condition. Gained/lost rules and interlocks live in the entry (the entry is canonical).

### 2.2 Roster — ORC set, adapted (36)

blinded, broken, clumsy, concealed, confused, controlled, dazzled, deafened, doomed, drained, dying, encumbered, enfeebled, fascinated, fatigued, fleeing, frightened, grabbed, hidden, immobilized, invisible, observed, off-guard, paralyzed, persistent damage, prone, quickened, restrained, sickened, slowed, stunned, stupefied, unconscious, undetected, unnoticed, wounded.

**Dropped from the ORC set:** *petrified* (never referenced; no setting analog). *Attitude conditions* (friendly/hostile/etc.) — our social engine uses the Disposition/reputation track instead ([Phase 4](2026-06-13-phase4-social-intrigue-engine.md)).

### 2.3 Roster — project conditions (2)

- **Suppressed** — canonical text currently in `classes/soldier.md` ("Suppressed *(condition)*" callout) moves here verbatim-in-substance; the Soldier chapter keeps a summary that defers to the appendix. Note the Soldier's 13th-level feature deepens the penalty — the appendix states the base condition only.
- **Glitching** — currently used by Officer (Lead by Example: Technological targets) and Scoundrel (Sabotage) but only half-defined inline ("a status penalty to its checks and DCs"). The appendix canonicalizes it: **–1 status penalty to checks and DCs; only technological creatures, constructs, and devices can be glitching.** The Sabotage parenthetical gloss then becomes redundant and is trimmed to reference the condition.

### 2.4 Interlocks preserved

unconscious → prone + off-guard chain; dying ↔ wounded ↔ doomed loop; the detection ladder observed / concealed / hidden / undetected / unnoticed (with invisible on top); grabbed → off-guard + immobilized; fatigued/sickened/etc. as written in ORC.

## 3. Traits appendix

### 3.1 Structure

1. **Intro:** what a trait is; **rules-bearing vs. hook** traits (Phase 1 §8.1); bracket notation is used in rules prose, plain Capitalized names in Traits lines (per [[traits-capitalized-frequency-separate]]); the §8.4 governance rule (a trait must be referenced by >1 rule or carry a reusable effect); the taxonomy table (Phase 1 §8.2) reproduced as orientation.
2. **One alphabetical glossary** — not grouped by category (lookup beats taxonomy; the table in the intro covers orientation).

### 3.2 Entry treatment by group

| Group | Treatment | Members |
|---|---|---|
| ORC rules-bearing | Full ORC text, adapted | Attack*, Auditory, Concentrate, Curse, Downtime, Emotion, Exploration, Fear, Flourish, Fortune, Healing, Illusion, Incapacitation, Linguistic, Manipulate, Mental, Misfortune, Move, Poison, Polymorph, Secret, Stance, Visual |
| Project rules-bearing | Original full text | Force + Applications (Alter, Body, Control, Mind, Offense, Sense — **descriptive, never gating**, per [[applications-are-descriptive-not-gating]]), Dark, Light, Tech, Technological, Form, Directive, Premonition, Sustain, Suppressed (rider trait, §3.3) |
| Damage-type hooks | One line each | Acid, Cold, Electricity, Fire, Sonic, Void |
| Class identity | One-line boilerplate | Consular, Guardian, Officer, Scoundrel, Sentinel, Soldier (+ Tech Specialist if referenced — verify during build) |
| Species identity | One-line boilerplate | the 27 species traits + Humanoid, Droid, Construct |

\* *Attack (and any trait referenced by core rules but missing from the usage inventory) is included only if a final implementation sweep confirms it's referenced.*

### 3.3 Name collisions & near-collisions (resolved here)

- **Suppressed** is both a **condition** (on creatures) and a **trait** (on rider effects, carrying the "one [Suppressed] effect per suppressing action" rule from the Soldier sidebar). Both entries exist, each cross-referencing the other. The trait entry becomes the canonical home of the one-rider rule (per [[traits-have-rules-bearing-descriptions]]).
- **Tech vs. Technological** are **both real and distinct**: *Tech* = the Tech Specialist's power-source trait (analog of Force, appears on Modifications); *Technological* = hook trait marking machine-based creatures, devices, and effects (what glitching and Signal Jamming key off). Both defined; the distinction is stated in each entry.

## 4. ORC text adaptation rules

- "spell" → "power"; "spellcasting" → power/ability phrasing; no alignment, divine, or fantasy-species references.
- Remaster (ORC) baseline — *off-guard*, not flat-footed.
- Keep 2E's mechanical values verbatim (our substrate rule [[orc-2e-is-default-substrate]]); adapt only vocabulary and setting flavor.
- **Licensing (carried forward):** reusing ORC text obligates an ORC attribution notice in the published book. Not built now; tracked here.

## 5. Consistency fixes shipped with this change

1. `classes/soldier-fighting-styles.md` — five `**Traits** [Suppressed]` lines use brackets inside a Traits line, against house style. Reformat to `**Traits** Suppressed`.
2. `01-introduction.md:124` — cites "`[once per minute]` cooldown" as an example *trait*; reuse timers are Frequency lines, never traits. Reword the example.
3. `classes/scoundrel-specializations.md` Sabotage — trim the inline gloss of glitching once the appendix owns the definition.
4. `classes/soldier.md` — Suppressed callout becomes a summary deferring to the appendix (text moves, not duplicated).

## 6. Project directive (user request, 2026-07-03)

Add to project `CLAUDE.md`: **whenever new content references a trait or condition that has no appendix entry, add the entry in the same change.** (The prose-level enforcement of Phase 1 §8.4 governance.)

## 7. Out of scope

- Creature-facing conditions/rules not yet referenced by player-core (Phase 7 may extend the lists).
- The ORC attribution/legal appendix itself.
- Any rebalancing of condition values (e.g., the [[bulwark-resistance-playtest-flag]] area) — text consolidation only.

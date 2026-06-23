# Design Spec: player-core Species & Backgrounds chapter

**Date:** 2026-06-22
**Status:** Approved (brainstorming complete)
**Type:** Content writeup + the deferred-content batch (ancestry feats, heritages) + two small authored subsystems (Droid construct rules, Size effects).

## Problem

The [species roster](2026-06-15-species-roster.md) (27 organic species + a heritage-defined Droid) and [backgrounds roster](2026-06-15-backgrounds-roster.md) (36) are Approved, but base-stats-only — they **defer** per-species **Ancestry (Species) Feats** and **Heritages** (both present in the SQL dump's `AncestryFeat` and `Heritage` tables) and never authored **Droid construct rules** or **Size** effects. The publication-finish chapter needs all of it.

## Decisions

**Licensing/naming.** Trademarked Star Wars species/heritage names are kept — this is a personal homebrew on ORC *mechanics*; the ORC/CC-BY governs the rules, not the setting names. (No analog-renaming.)

**File structure** (mirrors the class split):
- `docs/player-core/species.md` — how Species & Heritages work; the **Size** rules; the **Droid construct rules**; then the **27 organic species + Droid** as full entries, each with its **Heritages**.
- `docs/player-core/species-feats.md` — the **per-species Ancestry Feat menus** (access levels 1/5/9/13/17), mined from `AncestryFeat` and re-evaluated.
- `docs/player-core/backgrounds.md` — the **36 backgrounds** (boosts / trained skill / Lore); each names its skill feat (statted later in the general Feats chapter).

**Re-evaluation conventions ("map, don't copy", as with the Force toolkit):**
- Bounded effects only — circumstance bonuses, conditions, or utility; **no flat per-level numbers**; flat values key to the Level Bonus where needed.
- Restated attributes removed (use the relevant skill/Class DC); INT/Class-DC keying where apt.
- Force-flavored ancestry feats that grant powers route to the [Force toolkit](2026-06-15-shared-force-toolkit.md), not class-locked grants.
- Traits Capitalized; reuse timers as a **Frequency** line (per [[traits-capitalized-frequency-separate]]).
- Ancestry feats follow the publication feat-entry template (Name · Feat N · Traits · Prerequisites · effect).

**Authored Droid construct rules** (the roster deferred these): the Droid is a `Construct` — immune to disease, poison, and effects targeting a living mind (most `[mental]`); no Constitution-based effects (its HP uses a fixed value in place of the Con term, TBD-by-the-HP-rule); **healed by Repair (Crafting), not Medicine**; doesn't eat/sleep/breathe; its in-combat recovery analog replaces Catch Your Breath with a Repair-based equivalent. Kept lean and player-facing.

**Authored Size rules** (small framework gap): a brief table — Tiny (reach 0, +1 some Stealth contexts), Small (no combat penalty in our bounded frame; fits tight spaces), Medium (baseline), Large (reach 10 ft, takes more space). Effects bounded and minimal.

**Deferred (need other systems first; clean pointers, no placeholders in the prose):**
- The **4 Force-sensitive backgrounds** (Dathomir Witch, Warden of the Sky, Temple Youngling, Sith Initiate) — pending Force-sensitivity / Force Adept design.
- The **Lore-category taxonomy** (Settlement/Planet/Craft/Science/Org/Engineering/Creature/Species) that powers the "any X Lore" grants — labels stand; taxonomy is a later content pass.
- Background **skill-feat stat blocks** — named in each background, statted in the general **Feats** chapter.

## Sequencing

1. `species.md` (framing + Size + Droid construct + all species entries with heritages).
2. `species-feats.md` (ancestry-feat menus, in batches).
3. `backgrounds.md`.

Each stage committed separately; balance is a relative re-pass (ancestry feats/heritages are flat/bounded, so largely tier-agnostic, per the roster spec's insight).

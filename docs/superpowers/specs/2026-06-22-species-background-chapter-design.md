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
- **Two axes, two scalings (corrected 2026-06-25).** Bounding is **d20-axis only**: keep check/save/DC bonuses to **circumstance +1/+2** (Level Bonus governs the to-hit spine, not feat values). **Damage-axis** values — *resistances and damage riders* — follow **ORC/2E scaling**, because hits scale multiplicatively via striking (1→4 dice) and a Level-Bonus-capped value (max 6) decays against them. So: typed **resistance = half your level (min 1)** (upgrades to full level), damage riders **= your level**, polymorph/battle-form values flat. *Do NOT peg resistances/damage to the Level Bonus* — that conflates the two axes. (Per [[orc-2e-is-default-substrate]]: unspecified rules inherit ORC/2E.)
- Restated attributes removed (use the relevant skill/Class DC); INT/Class-DC keying where apt.
- Force-flavored ancestry feats that grant powers route to the [Force toolkit](2026-06-15-shared-force-toolkit.md), not class-locked grants.
- Traits Capitalized; reuse timers as a **Frequency** line (per [[traits-capitalized-frequency-separate]]).
- Ancestry feats follow the publication feat-entry template (Name · Feat N · Traits · Prerequisites · effect).

**Background entry format (Paizo prose — locked 2026-06-26).** Each background is written as published prose, **not** bolded label-lines, matching the PF2 Player Core / Starfinder 2e house style (model: [Acolyte](https://2e.aonsrd.com/backgrounds/134-acolyte)). Per-entry shape, in order:
1. `### <Name>` header.
2. One descriptive paragraph — the prior life, second person.
3. Blank line, then the **boosts sentence**, verbatim shape: `Choose two attribute boosts. One must be to **<X>** or **<Y>**, and one is a free attribute boost.` — attribute names **bold**; always one constrained pair + one free.
4. Blank line, then the **training + feat sentence**: `You're trained in the <Skill> skill and <Lore>. You gain the <Feat> skill feat.`
   - Skill / Lore / Feat names render **inline (no bold or italic)** — only attribute names carry the keyword signal.
   - The **Force** skill is written "the Force skill" (never "the The Force skill").
   - Fixed Lore → "the `<Name>` Lore skill"; choice Lore → "a/an `<Category>` Lore skill of your choice" (keep the article from the grant).
   - **General-feat exception** (Podracer): "You gain the `<Feat>` general feat."
   - **No** `**Attribute Boosts**` / `**Trained Skills**` / `**Skill Feat**` label-lines.

Entries listed alphabetically. Applied to all 40 entries (currently in `docs/player-core/02-species.md`) on 2026-06-26, commit `91de6b7`.

**Authored Droid construct rules** (the roster deferred these): the Droid is a `Construct` — immune to disease, poison, and effects targeting a living mind (most `[mental]`); no Constitution-based effects (its HP uses a fixed value in place of the Con term, TBD-by-the-HP-rule); **healed by Repair (Crafting), not Medicine**; doesn't eat/sleep/breathe; its in-combat recovery analog replaces Catch Your Breath with a Repair-based equivalent. Kept lean and player-facing.

**Authored Size rules** (small framework gap): a brief table — Tiny (reach 0, +1 some Stealth contexts), Small (no combat penalty in our bounded frame; fits tight spaces), Medium (baseline), Large (reach 10 ft, takes more space). Effects bounded and minimal.

**Deferred (need other systems first; clean pointers, no placeholders in the prose):**
- The **4 Force-sensitive backgrounds** (Dathomir Witch, Warden of the Sky, Temple Youngling, Sith Initiate) — pending Force-sensitivity / Force Adept design.
- **Kel Dor's 7 Force-flavored ancestry feats** (Baran Do Sensitive, Sage's Warning, Electric Judgment, Life Sense, Grand Sage, Storm Caller, Wrath of Dorin) — held out of `species-feats.md` (Kel Dor ships 11 published feats); they grant Force powers/sensitivity, so they join the same deferred Force-content bucket. Restore when Force-sensitivity / Force Adept is designed. *(Only Force-feat-heavy species in the roster; all others ported in full.)*
- The **Lore-category taxonomy** (Settlement/Planet/Craft/Science/Org/Engineering/Creature/Species) that powers the "any X Lore" grants — labels stand; taxonomy is a later content pass.
- Background **skill-feat stat blocks** — named in each background, statted in the general **Feats** chapter.

## Sequencing

1. `species.md` (framing + Size + Droid construct + all species entries with heritages).
2. `species-feats.md` (ancestry-feat menus, in batches).
3. `backgrounds.md`.

Each stage committed separately; balance is a relative re-pass (ancestry feats/heritages are flat/bounded, so largely tier-agnostic, per the roster spec's insight).

# Manifest — the Universal Action for Force Powers

**Status:** Approved (design), pending implementation
**Date:** 2026-07-05
**Type:** Core-rules addition + rename. Promotes **Manifest** from an undefined verb to the system's universal activity for using a Force power (the ORC/2E *Cast a Spell* analog), and renames the Consular's level-1 class feature that previously squatted on the name.
**Upstream:** [Class — Consular](2026-06-19-class-consular.md) (§4 "The Verb — Manifest" is amended by this spec), [Force toolkit](2026-06-15-shared-force-toolkit.md), [Consular Mandate rework](2026-07-05-consular-mandate-rework.md).
**Downstream:** `docs/player-core/the-force.md` (new action definition + two rewordings), `docs/player-core/classes/consular.md` (feature rename + cross-refs + Key Terms).

---

## 1. Problem

"Manifest" is used as a rules verb throughout the corpus — 37 occurrences across `the-force.md`, `consular.md`, and `guardian-forms.md` ("when you Manifest a Control power…", "after you Manifest a Force power…") — but no rule defines Manifesting. The only thing named Manifest is the Consular's level-1 class feature, which actually grants the deep Attunement pool and powers known: a pre-selected class verb shoehorned into the text without a real function. Meanwhile `the-force.md` §How Force Powers Work never defines *any* action for using a power.

**The fix:** define Manifest once, universally, as the activity of using a Force power; rename the Consular feature to what it actually does.

## 2. The Manifest Action (lean — Approach A)

New subsection at the **top** of `the-force.md` §How Force Powers Work (before "Attunement"), heading `### Manifest — using a power`, defining the universal activity:

> **Manifest** `[varies]`
> **Traits** Concentrate, Force
> **Requirements** You know the power, and you can pay its Attunement cost.
> ———
> You channel the Force into effect. Manifesting takes the actions shown in the power's header (`[one-action]`, `[two-actions]`, `[three-actions]`, `[reaction]`, or a longer time), spends the power's Attunement cost, and gains the power's traits. Wherever a rule says you "use" a Force power, you Manifest it.

- **Universal:** every Force user Manifests — Guardian, Sentinel, Consular, archetype dabbler. The Consular's distinction is *depth* (pool, repertoire), not exclusive ownership of the verb. All 30+ existing verb usages become rules-correct with no rewording.
- **Deliberately lean (Approach A, decided 2026-07-05):** no component system, no disruption/manifest-defensively subsystem — ORC 2E's verbal/somatic machinery has no analog here and nothing in the corpus references one. The Concentrate trait (existing appendix entry) carries the fascinated/focus interaction.
- **Existing rules unchanged:** reactions, Sustain, Push, Frequency timers, and Attunement costs all read as before; the action definition is the peg they hang on.
- The section's opening resource line becomes "**Manifesting a power spends Attunement**…" so the pool paragraph hangs off the defined verb.

## 3. Consular Feature Rename

- `## Manifest` (L1: pool `3 + Level Bonus`, Center restores 3, powers known) → **`## Deep Reservoir`** (the design spec's own internal name for the mechanic). Rules text unchanged apart from the heading.
- **Class Features table** (L1 row): "Manifest, Telekinetic Impact, Mandate, …" → "Deep Reservoir, Telekinetic Impact, Mandate, …".
- **Key Terms:** the *Manifest* entry becomes a pointer to the universal action ("**Manifest**. The universal activity for using a Force power — spend its actions and Attunement; see **The Force**."); *Repertoire* entry unchanged.
- **Feature-pointer sweep:** any "(see *Manifest*)" italic cross-reference that means the L1 feature (e.g., the Mandates sidebar's "your broad access (see *Manifest*)") → "(see *Deep Reservoir*)". Verb usages ("when you Manifest…") are untouched.
- **Names that stay:** *Heightened Manifest* (L5 feature) and the feat line (*Empower / Twin / Quickened / Remote Manifest*, *Sustaining Will*, etc.) — all read correctly, indeed better, against a defined action.

## 4. the-force.md Touch-ups

- §Acquiring powers, the parenthetical "…and the verb you channel them through (the Consular's deep Manifest, the Guardian's blade, the Sentinel's premonitions)" → reworded so the verb isn't class-owned, e.g. "…and how your class channels them (the Consular's deep reservoir, the Guardian's blade-work, the Sentinel's premonitions)."
- The Guardian-synergy lines already phrased "after you Manifest a Force power" (Niman, Guardian Mastery) become rules-correct as written — no edits.

## 5. Spec Maintenance

- `2026-06-19-class-consular.md` §4 ("The Verb — Manifest") gets a short amendment note (mirroring the §5 supersession style): Manifest universalized as the system-wide action 2026-07-05; the Consular L1 feature is now **Deep Reservoir**; §4.1's framework (pool depth, broad access, CHA Class DC) is unchanged in substance.
- This spec's status flips to Implemented at the end of the pass.

## 6. Non-goals

- No component/disruption subsystem (Approach B rejected — YAGNI).
- No rewording of other class files' "use a power" phrasing — the action definition makes "use" and "Manifest" synonyms by rule.
- No change to Attunement costs, power action costs, Push, or any Mandate content.

## 7. Verification

- `the-force.md`: Manifest block present at the top of §How Force Powers Work; Concentrate trait referenced (appendix entry exists — no closed-index work).
- `consular.md`: zero remaining occurrences of Manifest *as a feature name* (heading, features table, Key Terms, italic feature-pointers); verb usages untouched.
- Corpus grep "Manifest" — every remaining hit is either the universal action, a verb usage, or a compound ability/feat name (*Heightened Manifest*, *Empower Manifest*, …).

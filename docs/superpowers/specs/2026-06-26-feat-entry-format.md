# Feat Entry Format (publication standard)

**Date:** 2026-06-26
**Status:** Approved (codifies the de-facto house style already used across all feat files)
**Type:** Presentation standard. Governs how **every feat** is printed — class feats, species/ancestry feats, general & skill feats, and Lightsaber Form feats (anything with a `**Feat N**` line) in `docs/player-core/`. Activated abilities that are **not** feats — class/subclass **Actions**, **Force Powers**, and **Tech Modifications** — follow the companion [activated-ability formats](2026-06-27-activated-ability-formats.md), which inherits the shared core (action token, Traits, the `**Effect**` rule, degrees) from this doc.
**Model:** PF2 Player Core / Starfinder 2e *printed* feat entries (e.g. [Assurance](https://2e.aonsrd.com/feats/763-assurance)). Note the Archives-of-Nethys page renders **every** field with a bold label (`Traits:`, `Effect:`, `Special:`) — that is database display, **not** the print style we follow. See §4.

---

## 1. The locked template

Render the fields that apply, **in this exact order**; omit a field only when genuinely not applicable, and never silently reorder.

```
### <Name>  [<action-cost>]            ← glyph token only if the feat has an activation cost
**Feat <N>** · **Traits** <Trait, Trait, …>
**Prerequisites** <…>                  ← only if gated
**Frequency** <…>                      ← only if reuse-limited
**Trigger** <…>                        ← only if a reaction / triggered free action
**Requirements** <…>                   ← only if a precondition must hold
**Cost** <N> <resource>                ← only if it spends a resource (e.g. 1 Attunement)
<effect text>                          ← plain prose for simple/passive feats (NO label)…
**Effect** <effect text>               ← …OR labeled — see §3
**Critical Success** <…>               ← any roll/save-based feat spells out the
**Success** <…>                            applicable degrees, in this order
**Failure** <…>
**Critical Failure** <…>
**Special** <…>                        ← repeatable / misc notes; ALWAYS last
```

The header glyph and the `**Feat N** · **Traits** …` line are **mandatory** on every entry. Everything between Traits and the effect is optional and appears only when applicable.

## 2. Field rules

- **Name & level.** `### <Name>` as its own header. The level is the `**Feat N**` token on the next line, never in the header.
- **Action-cost token.** A markdown stand-in for Paizo's action glyphs, placed after the name with two leading spaces. Allowed tokens: `[one-action]`, `[two-actions]`, `[three-actions]`, `[reaction]`, `[free-action]`. Omit entirely for passive feats and feats with no activation. (At true print finish these tokens become the ◆ ◆◆ ◆◆◆ ⟲ ◇ glyphs.)
- **Traits.** All traits **Capitalized**; comma-separated; on the `**Feat N** · **Traits** …` line. Reuse timers are a **Frequency** line, **never** a trait. (Per [[traits-capitalized-frequency-separate]].)
- **Prerequisites.** Name the exact gate (a prior feat, a proficiency, an attribute). If a feat requires another feat, the prerequisite must be that feat's exact name.
- **Cost.** The project resource spend (Attunement, Focus, etc.) — `**Cost** 1 Attunement`. This is distinct from action cost (the header glyph).
- **Special.** Repeatability and other miscellaneous notes go in a **`**Special**`** line, placed **last** (after the effect and any degrees of success) — matching the printed book. Standard repeatable wording: "You can select this feat multiple times. Each time, choose a different … and gain the benefits …" Do **not** fold these into the effect prose.
- **No restated key attribute.** A feat that uses a Class DC / class verb does not restate the keying attribute — it's already baked in. (Per [[class-dc-no-attribute-restate]].)
- **Bounded values.** Feat bonuses are **circumstance +1/+2**, conditions, or new options — never runaway numbers, and never pegged to the Level Bonus. Damage-axis riders (resistances, damage adds) follow ORC/2E scaling. (Per [[orc-2e-is-default-substrate]].)

## 3. When to label `**Effect**`

Use the **`**Effect**`** label when — and only when — the entry has any **activation notation**: a **Frequency**, **Trigger**, **Requirements**, or **Cost** line. The label separates those activation conditions from the description of what happens.

**Otherwise write the effect as plain prose with no label** — passive feats, plain actions, and prerequisite-only feats get no `**Effect**` label, **even when the effect has degrees of success** (the degrees simply follow the prose). **Prerequisites** and degrees of success **alone** do **not** force an `**Effect**` label; only the four activation lines do.

## 4. Conventions vs. the printed book / Archives-of-Nethys

What we follow from the **printed** Paizo entry (confirmed against the printed Assurance capture): `**Special**` is a real labeled line placed last (§2); a simple feat's effect is **plain prose with no `Effect:` label**; traits sit in a band by the name.

What we drop or adapt:
- **No blanket `Effect:` label.** AoN's database view labels every field; the print and this standard label `**Effect**` only per §3.
- **`Traits` is a run-in**, not a standalone block — it shares the `**Feat N** · **Traits** …` line (we don't render trait pills in markdown).
- **`Source` / page lines are omitted** — the printed book's "Source Player Core pg. X" line has no analog in a single-book homebrew (this *is* the source).

## 5. Worked conversion (AoN → house style)

> **AoN renders:** *Assurance* `Feat 1` — **Traits:** Fortune, General, Skill · **Prerequisites:** trained in at least one skill · **Effect:** … · **Special:** You can select this feat multiple times…
>
> **House style:**
> ```
> ### Assurance
> **Feat 1** · **Traits** Fortune, General, Skill
> **Prerequisites** trained in at least one skill
> Even in the worst circumstances, you can perform basic tasks. Choose a skill you're trained in. You can forgo rolling a skill check for that skill to instead receive a result of 10 + your proficiency bonus (do not apply any other bonuses, penalties, or modifiers).
> **Special** You can select this feat multiple times. Each time, choose a different skill and gain the benefits for that skill.
> ```
> No action glyph (no activation); prerequisite present but **no activation notation** (no Frequency/Trigger/Requirements/Cost), so the effect is plain prose with **no** `**Effect**` label even though degrees could apply; the repeatable note is a **Special** line, placed last (matching the printed book).

A second worked example — an activation-notation, degree-based feat (from the [Human feats](../../player-core/02-species.md)). Note **Prerequisites precedes Frequency** (locked order, §1), and the **Frequency** line forces the `**Effect**` label:

```
### Aggressive Negotiations  [two-actions]
**Feat 9** · **Traits** Human, Auditory, Linguistic, Mental
**Prerequisites** trained in Diplomacy or Intimidation
**Frequency** once per 10 minutes
**Effect** You shout down or charm your foes mid-fight. Attempt a Diplomacy or Intimidation check against the Will DC of each enemy within 30 feet.
**Critical Success** The target is stunned 1.
**Success** The target is off-guard until the start of your next turn.
**Failure** The target is unaffected.
```

## 6. Quick checklist

- [ ] `### Name` + (optional) action token; `**Feat N** · **Traits** …` line present
- [ ] Fields in locked order (§1); none silently reordered or dropped
- [ ] Traits Capitalized; reuse timer is **Frequency**, not a trait
- [ ] `**Effect**` label present iff activation notation (Frequency / Trigger / Requirements / Cost) present (§3)
- [ ] Degrees of success, when used, in Crit-Success → Crit-Failure order
- [ ] Repeatable / misc notes in a `**Special**` line, placed last
- [ ] Values bounded (circ +1/+2); no restated key attribute

# Activated-Ability Entry Formats — Actions, Powers, Modifications

**Date:** 2026-06-27
**Status:** Approved (2026-06-27; both §6 normalization choices approved)
**Type:** Presentation standard. Companion to the [feat-entry format](2026-06-26-feat-entry-format.md). Governs every **activated-ability stat block that is not a feat**: class/subclass-granted **Actions** (Directives, signature strikes, etc.), **Force Powers** (`the-force.md`), and **Tech Modifications** (`tech-specialist-modifications.md`).
**Model:** PF2/SF2 printed action, spell, and item-activation blocks, adapted to this game's resources (Attunement, the Tech three-mode rig).

---

## 1. The shared core (inherited from the feat-entry format)

All three profiles below inherit these rules from the [feat-entry format](2026-06-26-feat-entry-format.md) — they are **not** restated per profile:

- **Action-cost token** — `[one-action]`, `[two-actions]`, `[three-actions]`, `[reaction]`, `[free-action]`; markdown stand-in for the glyphs.
- **Traits** — all **Capitalized**, comma-separated; reuse timers are a **Frequency** line, never a trait. (Per [[traits-capitalized-frequency-separate]].)
- **`**Effect**` label rule (§3 there)** — present iff the block has activation notation (**Frequency / Trigger / Requirements / Cost**); otherwise the effect is plain prose.
- **Degrees of success** — `**Critical Success** / **Success** / **Failure** / **Critical Failure**`, in that order, only the applicable ones.
- **Bounded values; no restated key attribute** — circumstance +1/+2 on the d20 axis; damage-axis riders follow ORC/2E scaling. (Per [[orc-2e-is-default-substrate]], [[class-dc-no-attribute-restate]].)

What differs per profile is **the header (where the level goes)** and **which extra fields apply**. Those are the rest of this doc.

## 2. Profile A — Actions (class & subclass grants)

An **Action** is an activated ability handed out by a class feature or subclass feature (a Directive, a signature Strike, a capstone trick). It is **not** chosen like a feat, so it has **no `**Feat N**` line and no level token of its own** — the granting feature's `### …` heading already states the level. The stat block is a **run-in**: the name is bold inline (not its own heading), because it sits under the feature that grants it.

```
### <Granting Feature>
**(<N>th level)** <prose explaining what the feature grants> …

**<Ability Name>**  [<action>]  · **Traits** <Trait, Trait, …>
**Frequency** …            (optional)
**Trigger** …              (optional; reactions)
**Requirements** …         (optional)
**Cost** …                 (optional; a resource the class spends)
**Effect** <the body>      (**Effect** label required — activation notation is present by definition)
**Critical Success / Success / Failure / Critical Failure**   (if roll/save-based)
```

*Example (Scoundrel capstone grant):*
```
**Suggest**  [two-actions]  · **Traits** Scoundrel, Linguistic, Mental
**Frequency** once per minute
**Effect** One creature within 30 feet that can understand you attempts a Will save against your Scoundrel class DC.
**Critical Success** The target is unaffected and knows you tried to manipulate it.
**Success** The target is unaffected.
**Failure** The target follows a suggested course of action (one that isn't obviously self-destructive) for 1 round.
**Critical Failure** As Failure, but for up to 1 minute or until the suggestion would clearly endanger it.
```

**Rules specific to Actions:**
- The **level lives on the granting feature**, not inside the ability block. Do **not** glue a `**(Nth level)**` marker onto the `**Effect**` line (§6 normalization).
- Run-in Traits separator is **` · **Traits**`** (a spaced middot, then a fresh bold) — matching feats and powers (§6 normalization; current files vary).
- Saves resolve against the relevant **class DC** (named once, not re-derived from the attribute).

## 3. Profile B — Powers (Force powers)

A **Power** is a Force ability learned from the shared Force toolkit. It is leveled like a spell, so the **level goes in the header as `· Power <N>`**, and **Traits sit on their own line** beneath (the name is a real heading).

```
### <Name>  [<action>]  · Power <N>
**Traits** <Force, …>
**Cost** <N> Attunement | none          ( ; **Frequency** … may share this line)
**Range** <range>; **Targets** <targets>     ┐ related fields may share one line,
**Area** <area>; **Defense** <save>          ┘ joined by "; "
**Defense** <save>                       (basic <Save> = degrees omitted; bare <Save> = spell out degrees)
**Trigger** …                            (reactions)
**Duration** <duration> (Sustain)        (Sustain noted in parentheses)
**Effect** <the body; inline die-scaling "Increase the damage by one die at 11th and 17th levels">
**Critical Success / Success / Failure / Critical Failure**   (only when the Defense is a NON-basic save)
**Push (+<N> Attunement)** <augment>     (spend extra Attunement for a stronger effect; repeatable field)
```

*Example:*
```
### Dominate Mind  [two-actions]  · Power 9
**Traits** Force, Control, Mental
**Cost** 3 Attunement; **Frequency** once per minute
**Range** 30 feet; **Targets** 1 creature
**Defense** Will; **Duration** up to 1 minute (Sustain)
**Effect** You seize a creature's will as your own.
**Critical Success** The target is unaffected and is temporarily immune for 1 minute.
**Success** The target resists, but is **stunned 1**.
**Failure** You control the target for 1 round, dictating its actions; it resists any order that would clearly harm it.
**Critical Failure** As failure, but you may Sustain the effect for up to 1 minute.
**Push (+1 Attunement)** The target gets no new save the first time you direct it to attack one of its own allies.
```

**Rules specific to Powers:**
- **`**Cost**` is the Attunement spend** (or `none` for a free power) — this is the Power's analog of a spell's resource, distinct from the action cost in the header.
- **`**Defense**`** names the save the target rolls. **`basic <Save>`** uses the standard basic-save outcomes, so **omit the degrees block** and put the damage inline (`… takes 2d6 electricity damage (basic Reflex)`). A **bare** save (`Will`, `Fortitude`) means non-standard outcomes — **spell out the degrees**.
- **Combined-field lines:** `Range`+`Targets`, `Area`+`Defense`, `Defense`+`Duration`, and `Cost`+`Frequency` may each share one line joined by `; `. One field per concept; never merge unrelated ones.
- **`**Push (+N Attunement)**`** is the augment rider (this game's "heightening by spending more"): a labeled line after the effect/degrees; a power may have more than one.
- **Scaling** is written inline in the Effect ("Increase the damage by one die at 5th, 11th, and 17th levels") — no separate Heightened line.
- *(Lightsaber Form feats also live in `the-force.md` but are **feats** — `**Feat N**`, with a `**<School> Mastery**` rider — and follow the [feat-entry format](2026-06-26-feat-entry-format.md), not this Power profile.)*

## 4. Profile C — Modifications (Tech Specialist)

A **Modification** is a Tech gadget with a fixed **three-mode** structure. The level goes in the header as `· Modification <N>`; the action cost rides **inline in the `**Activate**` line**.

```
### <Name> · Modification <N>
**Traits** <Tech, …>
**Standby** <the always-on passive while installed>
**Activate** [<action>] <the active effect; "(basic <Save>)" inline; at-will unless noted; vs. Tech class DC>
**Overclock** <the boosted version: bigger dice + Intelligence modifier + an added condition/area; then the Overclock flat check>
```

*Example:*
```
### Overload Logic · Modification 1
**Traits** Tech, Electricity
**Standby** You can wirelessly Slice or Disable a Device at up to 15 feet.
**Activate** [two-actions] One creature within 30 feet takes 1d6 electricity damage (basic Reflex).
**Overclock** Step the damage die to d8 and add your Intelligence modifier; the target is also clumsy 1 until the start of your next turn.
```

**Rules specific to Modifications:**
- The **three mode-labels `**Standby**` / `**Activate**` / `**Overclock**` are mandatory and always in that order.** They replace the generic Effect/degrees block; degrees, when needed, are written inline via `(basic <Save>)`.
- Only **Overclock** adds the **Intelligence** modifier; the base Activate adds no attribute. Overclock triggers the **Overclock flat check** (DC 15).
- Damage Modifications gain **+1 die at 5th, 11th, 17th** (stated once in the file's "Reading a Modification" preamble, not per entry).

## 5. Field glossary (used above)

| Field | Meaning | Profiles |
|---|---|---|
| **Cost** | Resource spent — **Attunement** (Powers), or a class resource (Actions) | A, B |
| **Range / Area / Targets** | Reach, shape, and legal targets | B |
| **Defense** | The save the target rolls; `basic <Save>` ⇒ omit degrees | B |
| **Duration** | How long it lasts; `(Sustain)` if sustainable | B |
| **Push (+N Attunement)** | Augment by spending extra Attunement | B |
| **Standby / Activate / Overclock** | The three Tech modes | C |
| **Frequency / Trigger / Requirements** | Activation notation (shared core) | A, B |

## 6. Normalization decisions (the changes from current files)

These are the only places existing content diverges; adopting this spec means a later cleanup pass:
1. **Traits separator for Actions** → unify on `· **Traits**` (current files use `**·  Traits**`, middot inside the bold, double-spaced).
2. **Level marker for Actions** → keep the level on the granting `### Feature` only; remove inline `**(Nth level)**` prefixes glued to `**Effect**`.
3. Everything else (Powers, Modifications) is **documentation of the existing convention** — no content change expected beyond incidental fixes the audit surfaces.

## 7. Checklist

- [ ] Correct profile chosen (Action / Power / Modification) by where the ability comes from
- [ ] Level placed per profile (granting feature for Actions; `· Power N` / `· Modification N` header otherwise)
- [ ] Shared core honored: action token, Capitalized Traits, `**Effect**` iff activation notation, degree order
- [ ] Power: `basic` save ⇒ no degrees + inline damage; bare save ⇒ degrees; `Push (+N Attunement)` after the body
- [ ] Modification: Standby/Activate/Overclock present and ordered; action cost inline in Activate
- [ ] No restated key attribute; values bounded

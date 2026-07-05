# Consular Mandate Rework Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Restructure the six Consular Mandates in player-core so each L1 entry holds a core mechanic plus a level-gated Mandate Powers table, with real mechanics at 3/7/11/15/19; sync the specs and fix three adjacent Level Bonus pegs.

**Architecture:** Docs-only change. `docs/player-core/classes/consular.md` is the deliverable (Mandate framing + six Mandate sections + three feat fixes); `docs/player-core/appendix-conditions.md` gains the Off-Balance entry (closed-index directive); three spec files get supersession/cross-reference notes. Design source of truth: `docs/superpowers/specs/2026-07-05-consular-mandate-rework.md`.

**Tech Stack:** Markdown, git. No build or test suite — verification is grep sweeps and section re-reads.

## Global Constraints

- **Closed indexes (CLAUDE.md):** any trait/condition referenced by new content must have an appendix entry in the same change. Off-Balance is new → Task 6 adds it. Clumsy and off-guard already exist.
- **No Level Bonus pegs for damage/resistance** — use level-based flat values (`your level`, `half your level`).
- **No designer meta in player text** (no "engine", "apex", "capstone", "rider").
- **Traits Capitalized; reuse timers are a `**Frequency**` line, not a trait.**
- **Class DC text never restates the key attribute.**
- **Don't restate action cost / Frequency / traits in ability prose** — the structured fields encode them.
- Edit with the Edit tool (no whole-file rewrite scripts — EOL churn).
- Line numbers below are from the pre-change file; after Task 2 they shift. Anchor edits on the quoted text, not line numbers.

---

### Task 1: Player-core framing text (Mandate feature + Mandates preamble)

**Files:**
- Modify: `docs/player-core/classes/consular.md:136-138` (the `## Mandate` class feature)
- Modify: `docs/player-core/classes/consular.md:202-204` (the `## Consular Mandates` preamble paragraph)

**Interfaces:**
- Produces: the "Mandate Powers" table convention that Tasks 2–7 rely on (powers added to repertoire free at listed level, Attunement cost unchanged).

- [ ] **Step 1: Replace the Mandate class feature text**

Old text (under `## Mandate`):

```markdown
**(1st level)** Every Consular commits to a **Mandate** — a devotion to one of the six Applications that grants its iconic power for free at 1st level, a signature benefit, and deeper command of that Application at 3rd, 7th, 11th, 15th, and 19th levels.
```

New text:

```markdown
**(1st level)** Every Consular commits to a **Mandate** — a devotion to one of the six Applications. Your Mandate grants a signature 1st-level benefit and a set of **Mandate powers** added to your repertoire as you gain levels, and it deepens your command of its Application with new abilities at 3rd, 7th, 11th, 15th, and 19th levels.
```

- [ ] **Step 2: Replace the Consular Mandates preamble paragraph**

Old text (under `## Consular Mandates`, before the sidebar):

```markdown
Choose one of the six Mandates below when you make your Consular (see the *Mandate* class feature). Each names powers it grants you (their full rules are in **[The Force](the-force.md)**); a granted power enters your repertoire for free, but you still spend Attunement to Manifest it as normal.
```

New text:

```markdown
Choose one of the six Mandates below when you make your Consular (see the *Mandate* class feature). Each Mandate opens with its **Mandate Powers** table: you add each listed power to your repertoire for free when you reach its listed level (their full rules are in **[The Force](the-force.md)**), but you still spend Attunement to Manifest it as normal.
```

The sidebar ("A Mandate Is Emphasis") is unchanged.

- [ ] **Step 3: Commit**

```bash
git add docs/player-core/classes/consular.md
git commit -m "player-core: Consular Mandate framing for the powers-table structure"
```

---

### Task 2: Mandate of Telekinesis

**Files:**
- Modify: `docs/player-core/classes/consular.md:211-237` (the `### Mandate of Telekinesis` section, from the heading to the `---` before `### Mandate of Visions`)

- [ ] **Step 1: Replace the section body**

Replace everything from `### Mandate of Telekinesis` down to (not including) the `---` separator before `### Mandate of Visions` with:

```markdown
### Mandate of Telekinesis

*The Force as a thousand unseen hands.* You move, lift, throw, and crush — the master of kinetic control.

**Mandate Powers**

| Level | Power |
|:---:|---|
| 1st | Force Push |
| 7th | Kinetic Slam |
| 11th | Force Hold |
| 15th | Force Wave |
| 19th | Telekinetic Singularity |

#### Telekinetic Adept

**(1st level)** Whenever you deal damage with an Alter power or with Telekinetic Impact, you push the target 5 feet.

#### Heavy Lifter

**(3rd level)** Your telekinesis grips the immovable. Your Telekinetic Grasp can lift objects of up to double the Bulk you could normally lift, and the distances you force creatures to move with Alter powers increase by 5 feet.

#### Kinetic Crush

**(7th level)** A creature you move with forced movement is **off-guard** until the start of your next turn, and if you force it into an obstacle or another creature, it takes bludgeoning damage equal to your level.

#### Crushing Grip

**(11th level)** Once per round, when a creature attempts a check to escape or end one of your Alter effects, you can tighten your grip: it rolls twice and takes the worse result (a misfortune effect).

#### Gravity Well  [reaction]

**(15th level)** **Trigger** A creature within 30 feet begins a move action.
**Effect** You seize it mid-stride. The creature attempts a Fortitude save against your Class DC; on a failure, its movement is halved until the end of its turn and you redirect the first 10 feet of that movement in a direction you choose. In addition, whenever you force a creature to move with your powers, you can drive it upward or over an edge.

*(Note: the "upward or over an edge" sentence is retained here rather than moved to general forced-movement rules — player-core has no general combat-rules chapter yet to receive it.)*

#### Singularity

**(19th level)** Your Telekinetic Adept push increases to 10 feet, and once per round it can also knock the target prone. In addition, once per round, after you see the result of an Alter power you Manifest, you can apply its Push upgrade without spending the extra Attunement, even if you've already applied a Push upgrade for free this turn.
```

- [ ] **Step 2: Verify no grant text remains in the features**

Run: `grep -n "repertoire" docs/player-core/classes/consular.md | sed -n '1,20p'` — within the Telekinesis section, "repertoire" must appear only in the preamble sentence, not in any `####` feature.

- [ ] **Step 3: Commit**

```bash
git add docs/player-core/classes/consular.md
git commit -m "player-core: rework Mandate of Telekinesis (powers table + mechanics)"
```

---

### Task 3: Mandate of Visions

**Files:**
- Modify: `docs/player-core/classes/consular.md` (the `### Mandate of Visions` section)

- [ ] **Step 1: Replace the section body**

Replace everything from `### Mandate of Visions` down to (not including) the `---` before `### Mandate of Serenity` with:

```markdown
### Mandate of Visions

*You fight a half-second ahead of everyone else.* Foresight is your shield and your squad's.

**Mandate Powers**

| Level | Power |
|:---:|---|
| 1st | Precognitive Parry |
| 7th | Guidance of the Force |
| 11th | Master Precognition |
| 15th | True Sight |
| 19th | Foresight |

#### Seer

**(1st level)** You can't be made **off-guard** by creatures of your level or lower, and you gain a +1 status bonus to initiative rolls.

#### Forewarned

**(3rd level)** Your premonitions guard the whole squad. When you roll initiative, you and each ally within 30 feet can't be made off-guard during the first round of combat.

#### Read the Currents

**(7th level)** In a social encounter, you can Read the Room using The Force, and when you succeed, you also learn one of the opposing side's Levers or Guards. In addition, once per social encounter, you can glimpse an opponent's immediate intent: the GM tells you which action it will take on its next turn.

#### Battle Precognition  [reaction]

**(11th level)** **Trigger** An ally you can see attempts a saving throw.
**Effect** You call the warning a half-second early. The ally rolls twice and takes the better result (a fortune effect).

#### Peerless Seer

**(15th level)** No creature can make you off-guard, and your Forewarned feature also grants the allies it protects your +1 status bonus to initiative rolls.

#### Foresight

**(19th level)** You are permanently under the effect of your Foresight power, without spending Attunement or Sustaining it.
```

- [ ] **Step 2: Commit**

```bash
git add docs/player-core/classes/consular.md
git commit -m "player-core: rework Mandate of Visions (powers table + mechanics)"
```

---

### Task 4: Mandate of Serenity

**Files:**
- Modify: `docs/player-core/classes/consular.md` (the `### Mandate of Serenity` section)

- [ ] **Step 1: Replace the section body**

Replace everything from `### Mandate of Serenity` down to (not including) the `---` before `### Mandate of Vitality` with:

```markdown
### Mandate of Serenity

*The still center that turns the storm.* You ward yourself and your allies against the galaxy's violence.

**Mandate Powers**

| Level | Power |
|:---:|---|
| 1st | Force Barrier |
| 3rd | Energy Absorption |
| 7th | Battle Focus |
| 11th | Force Cloak |
| 15th | Force Reflection |
| 19th | Wall of Light |

#### Eye of Calm

**(1st level)** Whenever you Manifest a Control power, you gain temporary Hit Points equal to your level until the start of your next turn.

#### Tutaminis

**(3rd level)** The energy resistance you gain from Control powers increases by 2.

#### Becalming Presence

**(7th level)** In a social encounter, you can Defuse using The Force, and the first time your side would lose Composure each exchange, reduce the loss by 1.

#### Unclouded Mind

**(11th level)** While you have at least 1 Attunement remaining, you gain a +1 status bonus to saves against fear and mental effects. In addition, your Eye of Calm also triggers whenever you Center.

#### Aegis

**(15th level)** Your defensive Control powers can target an ally within 30 feet instead of yourself. When one does, that ally gains your Eye of Calm's temporary Hit Points instead of you.

#### Still Point  [three-actions]

**(19th level)** **Frequency** once per day
**Effect** A perfect calm radiates from you in a 20-foot emanation, which you can Sustain for up to 1 minute. You and allies in the emanation gain temporary Hit Points equal to your level at the start of each of your turns, and allies in it share your Unclouded Mind bonus.
```

- [ ] **Step 2: Commit**

```bash
git add docs/player-core/classes/consular.md
git commit -m "player-core: rework Mandate of Serenity (powers table + mechanics)"
```

---

### Task 5: Mandate of Vitality

**Files:**
- Modify: `docs/player-core/classes/consular.md` (the `### Mandate of Vitality` section)

- [ ] **Step 1: Replace the section body**

Replace everything from `### Mandate of Vitality` down to (not including) the `---` before `### Mandate of Dominance` with:

```markdown
### Mandate of Vitality

*The Force gives, as well as takes.* You are the galaxy's foremost healer.

**Mandate Powers**

| Level | Power |
|:---:|---|
| 1st | Vital Transfer |
| 3rd | Force Surge |
| 7th | Force Valor |
| 11th | Force Revivify |
| 15th | Force Enlightenment |
| 19th | Force Resurrection |

#### Life-Giver

**(1st level)** Whenever a Force power you Manifest restores Hit Points to a creature, that creature also gains temporary Hit Points equal to your level.

#### Surge

**(3rd level)** While a Body power of yours is active, you gain a +10-foot status bonus to Speed and ignore difficult terrain.

#### Vigor

**(7th level)** When you restore Hit Points to a creature, you can also reduce the value of one condition affecting it by 1.

#### Wellspring

**(11th level)** When your party rests under your care, each ally recovers additional Hit Points equal to your level. In addition, once per day per creature, you can attempt a The Force check against the DC of a poison or disease afflicting it; on a success, the affliction's stage decreases by 1 (by 2 on a critical success).

#### Overflowing Life

**(15th level)** Once per round, when you restore Hit Points to a creature with a Force power, one other creature within 10 feet of it regains half that amount. Your Life-Giver feature applies to both creatures.

#### Fountain of Life

**(19th level)** Once per round, a power you Manifest that restores Hit Points costs 1 less Attunement, and the temporary Hit Points from your Life-Giver feature last until expended.
```

- [ ] **Step 2: Commit**

```bash
git add docs/player-core/classes/consular.md
git commit -m "player-core: rework Mandate of Vitality (powers table + mechanics)"
```

---

### Task 6: Mandate of Dominance + Off-Balance condition entry

The Whispered Doubt feature references the **Off-Balance** condition, which has no appendix entry — per the closed-index directive both edits land in this task.

**Files:**
- Modify: `docs/player-core/classes/consular.md` (the `### Mandate of Dominance` section)
- Modify: `docs/player-core/appendix-conditions.md:101` (insert Off-Balance alphabetically, immediately before `### Off-Guard`)

- [ ] **Step 1: Replace the Dominance section body**

Replace everything from `### Mandate of Dominance` down to (not including) the `---` before `### Mandate of Destruction` with:

```markdown
### Mandate of Dominance

*The will is the strongest weapon, and yours bends others.* You read minds, sow terror, and seize control — the Force's master mentalist.

**Mandate Powers**

| Level | Power |
|:---:|---|
| 1st | Mind Trick |
| 3rd | Force Fear |
| 7th | Mind Probe, Force Disruption |
| 11th | Dominate Mind |
| 15th | Mass Mind Trick |
| 19th | Mind Fracture, Sever Force |

#### Mind's Eye

**(1st level)** You sense the surface emotions of creatures within 30 feet (an imprecise sense), and you gain a +1 status bonus to Deception, Diplomacy, and Intimidation checks against creatures whose emotions you can sense.

#### Fearmonger

**(3rd level)** The frightened condition you impose with Force powers is slow to fade: its value doesn't decrease at the end of the target's first turn.

#### Whispered Doubt  [one-action]

**(7th level)** **Traits** Force, Mental
**Requirements** You are in a social encounter.
**Effect** You slip a thread of doubt beneath an opponent's certainty. Attempt a The Force check against the opponent's Will DC.

- **Critical Success** The opponent is **Off-Balance**, and its Resolve decreases by 1.
- **Success** The opponent is **Off-Balance**.
- **Critical Failure** It feels the intrusion and hardens, gaining a Guard against your next appeal.

#### Puppeteer

**(11th level)** Once per round, when a creature critically fails a save against one of your Mind powers, it immediately spends its reaction (if it has one available) to Stride or Strike; you choose the path or the target.

#### Looming Will

**(15th level)** Your will fills a room before you speak. When a social encounter begins, choose one: the opposing side's starting Resolve decreases by 2, or your side's starting Composure increases by 2.

#### Shatter Will

**(19th level)** **Frequency** once per minute
**Effect** When a creature fails, but doesn't critically fail, its save against one of your Mind powers, you can force it to critically fail instead. Against a creature of higher level than you, this can't worsen the outcome of a power with the Incapacitation trait.
```

- [ ] **Step 2: Insert the Off-Balance condition entry**

In `docs/player-core/appendix-conditions.md`, immediately before `### Off-Guard` (line 101), insert:

```markdown
### Off-Balance
You've been wrong-footed in a social exchange, leaving an opening your opposition can exploit. The next appeal made against you or your side gains a +1 circumstance bonus to its check, and the condition then ends. Off-Balance also ends at the end of the exchange in which you gained it.

```

(Original entry — Off-Balance is a Phase 4 social condition, not ORC 2E material.)

- [ ] **Step 3: Verify the closed index is satisfied**

Run: `grep -n "Off-Balance" docs/player-core/appendix-conditions.md docs/player-core/classes/consular.md`
Expected: one entry heading in the appendix, references in the Whispered Doubt feature.

- [ ] **Step 4: Commit**

```bash
git add docs/player-core/classes/consular.md docs/player-core/appendix-conditions.md
git commit -m "player-core: rework Mandate of Dominance; add Off-Balance condition"
```

---

### Task 7: Mandate of Destruction

**Files:**
- Modify: `docs/player-core/classes/consular.md` (the `### Mandate of Destruction` section)

- [ ] **Step 1: Replace the section body**

Replace everything from `### Mandate of Destruction` down to (not including) the `---` before `## Consular Feats` with:

```markdown
### Mandate of Destruction

*The Force unleashed, raw and merciless.* You are an artillery of will.

**Mandate Powers**

| Level | Power |
|:---:|---|
| 1st | Force Shock |
| 7th | Force Lightning |
| 11th | Chain Lightning |
| 15th | Force Storm |
| 19th | Force Destruction |

#### Force Artillery

**(1st level)** Whenever you deal damage to a creature with an Offense power or with Telekinetic Impact, that creature is **clumsy 1** until the start of your next turn. An area power applies this to every creature it damages.

#### Overload

**(3rd level)** Once per turn, you can apply the Push upgrade of an Offense power without spending the extra Attunement, even if you've already applied a Push upgrade for free this turn.

#### Arc Lightning

**(7th level)** Your single-target Offense powers arc to a second creature within 10 feet of the first, dealing it splash damage equal to your level.

#### Storm-Caller

**(11th level)** The cones and lines of your Offense powers increase one size step.

#### Scoured Ground

**(15th level)** Your area Offense powers leave the ground burning: until the start of your next turn, a creature that enters the area or ends its turn there takes damage equal to your level, of the same damage type as the power.

#### Annihilation

**(19th level)** Once per round, when an Offense power you Manifest reduces a creature to 0 Hit Points, you regain 1 Attunement.
```

- [ ] **Step 2: Commit**

```bash
git add docs/player-core/classes/consular.md
git commit -m "player-core: rework Mandate of Destruction (clumsy 1 artillery, level-based splash)"
```

---

### Task 8: Feat substrate fixes (Level Bonus pegs)

**Files:**
- Modify: `docs/player-core/classes/consular.md:461` (Crushing Grasp feat)
- Modify: `docs/player-core/classes/consular.md:552` (Warding Zone feat)

- [ ] **Step 1: Fix Crushing Grasp**

Old: `takes bludgeoning damage equal to your Level Bonus each time it fails to escape.`
New: `takes bludgeoning damage equal to half your level each time it fails to escape.`

(Matches the Crushing Pressure feat's half-level recurring damage.)

- [ ] **Step 2: Fix Warding Zone**

Old: `allies within it gain resistance to physical and energy damage equal to your Level Bonus.`
New: `allies within it gain resistance to physical and energy damage equal to half your level.`

- [ ] **Step 3: Sweep for remaining pegs**

Run: `grep -n "Level Bonus" docs/player-core/classes/consular.md`
Expected remaining hits ONLY: the Class Features table header column (line ~96) and the Manifest pool formula ("3 + your Level Bonus", line ~123). Any other hit that pegs damage, resistance, or a similar scaling value to Level Bonus: change it to `your level` (one-shot values) or `half your level` (recurring/passive values) and note it in the commit message.

- [ ] **Step 4: Commit**

```bash
git add docs/player-core/classes/consular.md
git commit -m "player-core: Consular feats — level-based values replace Level Bonus pegs"
```

---

### Task 9: Spec maintenance (supersession + cross-references)

**Files:**
- Modify: `docs/superpowers/specs/2026-06-19-class-consular.md:104-174` (§5) and the §7 list
- Modify: `docs/superpowers/specs/2026-06-13-phase4-social-intrigue-engine.md:167` (§13 first bullet)

- [ ] **Step 1: Supersede §5 of the class spec**

In `2026-06-19-class-consular.md`, replace the §5 heading, intro paragraph, and all six Mandate subsections (`### 5.1` through `### 5.6`, i.e., everything between the `## 5. Subclasses…` heading and the `**Cross-balance & §4.1 notes.**` paragraph) with:

```markdown
## 5. Subclasses — Mandates (six, one per Force school; reworked 2026-07-05)

**Superseded:** the original Mandate tables (designed 2026-06-19) made power grants the bulk of each subclass. The current design lives in **[Consular Mandate rework](2026-07-05-consular-mandate-rework.md)**: each L1 entry is a core mechanic plus a level-gated Mandate Powers list, and every 3/7/11/15/19 slot is a real mechanic (with out-of-combat features placed organically — Dominance carries the first class-specific social verb). Branching (L1, the 1/3/7/11/15/19 ◆ cadence) and one-Mandate-per-school are unchanged.
```

Keep the `**Cross-balance & §4.1 notes.**` paragraph as is (its `[incapacitation]`/`[dark]`/granted-powers-cost-Attunement rulings still apply).

- [ ] **Step 2: Update §7 Carried Forward in the class spec**

Change the line:

```markdown
- ~~**§5 Mandates** — six~~ — **DONE (2026-06-19):** Telekinesis/Visions/Serenity/Vitality/Dominance/Destruction, one per school.
```

to:

```markdown
- ~~**§5 Mandates** — six~~ — **DONE (2026-06-19)**, then **reworked (2026-07-05)**: grants consolidated into level-gated lists, every feature slot a mechanic — see [Consular Mandate rework](2026-07-05-consular-mandate-rework.md).
```

- [ ] **Step 3: Note the social-verb payment in the Phase 4 spec**

In `2026-06-13-phase4-social-intrigue-engine.md` §13, change:

```markdown
- **Class-specific social verbs & encounter pools** (e.g., a face's signature appeals) → Phase 5.
```

to:

```markdown
- **Class-specific social verbs & encounter pools** (e.g., a face's signature appeals) → Phase 5. *(First delivered 2026-07-05: the Consular Dominance Mandate's **Whispered Doubt** — see the [Consular Mandate rework](2026-07-05-consular-mandate-rework.md).)*
```

- [ ] **Step 4: Commit**

```bash
git add docs/superpowers/specs/2026-06-19-class-consular.md docs/superpowers/specs/2026-06-13-phase4-social-intrigue-engine.md
git commit -m "specs: supersede Consular spec §5; note first social verb in Phase 4 §13"
```

---

### Task 10: Verification sweep and status flip

**Files:**
- Modify: `docs/superpowers/specs/2026-07-05-consular-mandate-rework.md:3` (status line)

- [ ] **Step 1: Grant-text sweep**

Run: `grep -n "to your repertoire" docs/player-core/classes/consular.md`
Expected: exactly two hits — the Consular Mandates preamble and the Manifest feature's powers-known text. Zero hits inside any `####` Mandate feature.

- [ ] **Step 2: Peg sweep**

Run: `grep -n "Level Bonus" docs/player-core/classes/consular.md`
Expected: only the Class Features table header and the Manifest pool formula (plus any hits deliberately retained in Task 8 Step 3).

- [ ] **Step 3: Condition/trait closed-index sweep**

Run: `grep -n "clumsy\|Off-Balance\|off-guard\|misfortune\|fortune" docs/player-core/classes/consular.md`
Confirm every condition referenced by the new Mandate text (clumsy, Off-Balance, off-guard) has an appendix entry: `grep -n "^### " docs/player-core/appendix-conditions.md` must list Clumsy, Off-Balance, Off-Guard.

- [ ] **Step 4: Read the full Mandates section once, top to bottom**

Read `docs/player-core/classes/consular.md` from `## Consular Mandates` to `## Consular Feats`. Check: six sections, each = flavor line → Mandate Powers table → six `####` features at 1/3/7/11/15/19; no designer meta; Frequency/Trigger/Effect fields formatted like the file's feat blocks.

- [ ] **Step 5: Flip the rework spec status**

In `2026-07-05-consular-mandate-rework.md`, change:

```markdown
**Status:** Approved (design), pending implementation
```

to:

```markdown
**Status:** Implemented (2026-07-05) — see `docs/player-core/classes/consular.md`
```

- [ ] **Step 6: Final commit**

```bash
git add docs/superpowers/specs/2026-07-05-consular-mandate-rework.md
git commit -m "specs: mark Consular Mandate rework implemented"
```

# Manifest Universal Action Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Define Manifest as the system-wide action for using a Force power (the ORC/2E Cast a Spell analog) and rename the Consular's level-1 Manifest feature to Deep Reservoir.

**Architecture:** Docs-only change across three files: `docs/player-core/the-force.md` gains the action definition (plus two rewordings so the verb isn't class-owned), `docs/player-core/classes/consular.md` gets the feature rename with a four-site cross-reference sweep, and the class spec's §4 gets an amendment note. Design source of truth: `docs/superpowers/specs/2026-07-05-manifest-universal-action.md`.

**Tech Stack:** Markdown, git. No tests — verification is grep sweeps.

## Global Constraints

- **Verb usages are untouchable:** every "you Manifest a power"-style sentence in the corpus becomes rules-correct via the new action definition — do NOT reword them. Only *feature-name* references change.
- **Names that stay:** *Heightened Manifest* (L5 feature) and all feat names (*Empower/Twin/Quickened/Remote Manifest*).
- **No new traits/conditions:** Concentrate already has an appendix entry; Manifest is an action, not a trait — no closed-index work.
- **No designer meta in player text** (no "engine", "apex", "capstone", "rider").
- Edit with the Edit tool (no whole-file rewrite scripts — EOL churn). Anchor on quoted text, not line numbers.

---

### Task 1: the-force.md — the Manifest action + rewordings

**Files:**
- Modify: `docs/player-core/the-force.md:30-34` (insert subsection after the `## How Force Powers Work` heading; reword the Attunement opening line)
- Modify: `docs/player-core/the-force.md:56` (the "Acquiring powers" parenthetical)

**Interfaces:**
- Produces: the `### Manifest — using a power` subsection that consular.md's Key Terms entry (Task 2) points readers at.

- [ ] **Step 1: Insert the Manifest subsection**

Immediately after the line `## How Force Powers Work` (and its following blank line), insert — so that it precedes `### Attunement — your focus in the fight`:

```markdown
### Manifest — using a power

Every Force power is used the same way: you **Manifest** it.

> **Manifest**  `[varies]`
> **Traits** Concentrate, Force
> **Requirements** You know the power, and you can pay its Attunement cost.
> ———
> You channel the Force into effect. Manifesting takes the actions shown in the power's header (`[one-action]`, `[two-actions]`, `[three-actions]`, `[reaction]`, or a longer time), spends the power's Attunement cost, and gains the power's traits. Wherever a rule says you "use" a Force power, you Manifest it.

```

- [ ] **Step 2: Reword the Attunement opening line**

Old text (start of the `### Attunement — your focus in the fight` paragraph):

```markdown
Using powers spends **Attunement**, a pool that refreshes **each encounter**
```

New text:

```markdown
Manifesting a power spends **Attunement**, a pool that refreshes **each encounter**
```

(Only the first three words change; the rest of the paragraph is untouched.)

- [ ] **Step 3: Reword the "Acquiring powers" parenthetical**

Old text (one sentence inside the `### Acquiring powers — bought, not granted` paragraph):

```markdown
What your class provides is your *framework* and *emphasis*: how many powers you start with, which Applications come easily, and the verb you channel them through (the Consular's deep Manifest, the Guardian's blade, the Sentinel's premonitions).
```

New text:

```markdown
What your class provides is your *framework* and *emphasis*: how many powers you start with, which Applications come easily, and how you channel them (the Consular's deep reservoir, the Guardian's blade-work, the Sentinel's premonitions).
```

- [ ] **Step 4: Verify**

Run: `grep -n "Manifest" docs/player-core/the-force.md`
Expected: the new subsection's occurrences, plus the existing Guardian-synergy verb usages ("after you Manifest a Force power" etc.) — and zero remaining occurrences of "the Consular's deep Manifest".

- [ ] **Step 5: Commit**

```bash
git add docs/player-core/the-force.md
git commit -m "player-core: define Manifest as the universal action for Force powers"
```

---

### Task 2: consular.md — Deep Reservoir rename + cross-reference sweep

**Files:**
- Modify: `docs/player-core/classes/consular.md` (four rename sites + one plural fix; line numbers as of this writing: 21, 98, 121-125, 207)

**Interfaces:**
- Consumes: the universal Manifest action defined in Task 1 (the Key Terms entry points at The Force chapter).

- [ ] **Step 1: Update the Key Terms entry**

Old text:

```markdown
**Manifest**. To use a Force power — to spend the actions and Attunement and make it real.
```

New text:

```markdown
**Manifest**. The universal activity for using a Force power — spend its actions and Attunement and make it real (see **The Force**).
```

- [ ] **Step 2: Rename the feature in the Class Features table (level 1 row)**

Old text:

```markdown
| 1 | +2 | Manifest, Telekinetic Impact, Mandate, class feat, species feat |
```

New text:

```markdown
| 1 | +2 | Deep Reservoir, Telekinetic Impact, Mandate, class feat, species feat |
```

(The level 5 row's "Heightened Manifest" is NOT changed.)

- [ ] **Step 3: Rename the feature heading and fix the stale singular**

Old text (the full feature, two paragraphs under the heading):

```markdown
## Manifest

**(1st level)** You gain a pool of Attunement points equal to **3 + your Level Bonus** and your **Center** action restores **3 Attunement** instead of 2.

At 1st level, in addition to the power your **Mandate** grants you, you gain **four** level 1 Force powers.
```

New text:

```markdown
## Deep Reservoir

**(1st level)** You gain a pool of Attunement points equal to **3 + your Level Bonus** and your **Center** action restores **3 Attunement** instead of 2.

At 1st level, in addition to the powers your **Mandate** grants you, you gain **four** level 1 Force powers.
```

(Two changes: the heading, and "the power your Mandate grants you" → "the powers your Mandate grants you" — stale singular from before Mandates granted a powers table. The rest of the paragraph after "Force powers." continues unchanged.)

- [ ] **Step 4: Update the Mandates sidebar pointer**

Old text:

```markdown
> A Mandate deepens one Application, but it never walls off the others — your broad access (see *Manifest*) still lets you learn powers from any Application.
```

New text:

```markdown
> A Mandate deepens one Application, but it never walls off the others — your broad access (see *Deep Reservoir*) still lets you learn powers from any Application.
```

- [ ] **Step 5: Verify the classification sweep**

Run: `grep -n "Manifest" docs/player-core/classes/consular.md`
Expected: every remaining hit is a verb usage ("you Manifest a power…"), the Key Terms entry, or a compound name (*Heightened Manifest*, *Empower Manifest*, *Remote Manifest*, *Quickened Manifest*, *Twin Manifest*). Zero hits where "Manifest" alone names the L1 feature: specifically no `## Manifest` heading, no "Manifest," in the level-1 table row, and no "(see *Manifest*)".
Also run: `grep -n "Deep Reservoir" docs/player-core/classes/consular.md`
Expected: the new heading, the table row, and the sidebar pointer (3 hits). Note: if a "Deep Reserve" FEAT hit appears, that is a different, pre-existing feat — leave it alone.

- [ ] **Step 6: Commit**

```bash
git add docs/player-core/classes/consular.md
git commit -m "player-core: rename Consular Manifest feature to Deep Reservoir"
```

---

### Task 3: Spec maintenance + acceptance sweep

**Files:**
- Modify: `docs/superpowers/specs/2026-06-19-class-consular.md:75-77` (§4 amendment note)
- Modify: `docs/superpowers/specs/2026-07-05-manifest-universal-action.md:3` (status flip)

- [ ] **Step 1: Add the §4 amendment note to the class spec**

Old text:

```markdown
## 4. The Verb — Manifest

A typical Consular turn:
```

New text:

```markdown
## 4. The Verb — Manifest *(universalized 2026-07-05)*

**Amended:** Manifest is now the system-wide action for using any Force power (the Cast a Spell analog) — see **[Manifest universal action](2026-07-05-manifest-universal-action.md)**. The Consular's L1 feature is renamed **Deep Reservoir**; §4.1's framework below (pool depth, broad access, CHA Class DC) is unchanged in substance.

A typical Consular turn:
```

- [ ] **Step 2: Corpus acceptance sweep**

Run: `grep -rn "deep Manifest" docs/` — expected: zero hits in player-core (spec-file hits describing the old design are acceptable).
Run: `grep -n "### Manifest — using a power" docs/player-core/the-force.md` — expected: 1 hit.
Run: `grep -n "## Deep Reservoir" docs/player-core/classes/consular.md` — expected: 1 hit.

- [ ] **Step 3: Flip the design spec status**

Old text:

```markdown
**Status:** Approved (design), pending implementation
```

New text:

```markdown
**Status:** Implemented (2026-07-05) — see `docs/player-core/the-force.md` §Manifest and `docs/player-core/classes/consular.md` §Deep Reservoir
```

- [ ] **Step 4: Commit**

```bash
git add docs/superpowers/specs/2026-06-19-class-consular.md docs/superpowers/specs/2026-07-05-manifest-universal-action.md
git commit -m "specs: amend Consular spec §4 for the universalized Manifest action"
```

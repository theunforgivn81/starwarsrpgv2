# Star Wars RPG (working title)

A tabletop role-playing game system set in the Star Wars universe, designed to fuse the **tactical depth and structure of Pathfinder 2E / Starfinder 2E** with the **bounded accuracy of D&D 5E** — and then deliberately remove the two pillars most d20 systems lean on: the **daily resource clock** and the **dedicated healer**.

> **Status:** Early design. The engine layer (Phase 1) is complete. We are building the system bottom-up, one fully-specified design layer at a time, each ratified and committed before the next begins.

---

## What this game is

| | |
|---|---|
| **Setting** | Star Wars (rules engine only at this stage — see [Licensing](#licensing--content-sourcing)) |
| **Lineage** | PF2E/SF2E **structure** × D&D 5E **bounded accuracy** |
| **Power band** | Full spectrum — an all-scoundrel table and an all-Jedi table are both fully viable at the same power level |
| **First-class pillars** | Ground combat + social/intrigue (sharing one resolution engine) |
| **Complexity** | High (crunchy), but the budget is spent on the core loop first; supporting systems stay deliberately light |
| **The novelty** | No daily resource clock and no mandatory healer — power comes from *renewable* options (action economy + cooldowns), not a daily pool |

### Borrowed from Pathfinder / Starfinder 2E
- A **universal trait system** — machine-readable metadata on every entity (classes, feats, gear, creatures, actions), making prerequisites and conditions into data rather than prose.
- **Attributes as raw modifiers** (no scores, no separate +/- step).
- **Proficiency ranks** (untrained → legendary) granting scaling competence.
- **Four-degree outcomes** (critical success / success / failure / critical failure) based on beating or missing a DC by 10.
- A **three-action economy** with free actions and one reaction per round.
- **Bonus types constrained** to circumstance, status (and a tightly capped item bonus).
- A progression philosophy of **meaningful choices at every level** — no dead levels, no two same-class characters feeling identical.
- Every class has a **gameplay "verb"** — an active mechanic, never just numerical bonuses.

### Borrowed from D&D 5E
- **Bounded accuracy.** Proficiency uses `1 + (level ÷ 4)` rather than full level; challenge DCs don't scale with party level; enemies scale mostly through **hit points and abilities**, not through ever-climbing attack/defense numbers.

### Unique to this system
- **No baseline daily-resource clock.** Abilities are balanced by action-economy cost and time-based cooldowns; per-day frequencies are reserved sparingly for high-level abilities, never as a pacing engine.
- **No traditional spellcasters.** Force users are classes with active verbs, balanced horizontally against martials — so the system never assumes a "cleric" is present for healing or utility.

---

## Design pillars

Every rule is tested against these five falsifiable commitments (full text in the [design philosophy](docs/superpowers/specs/2026-06-13-star-wars-rpg-design-philosophy.md)):

1. **Bounded participation** — a lower-level character can still meaningfully act in a higher-level encounter; the gap is in *options and resilience*, not whether dice can connect.
2. **No mandatory seats** — every party function (damage, durability, healing, face, tech) is reachable by multiple classes, skills, or gear.
3. **Every class has a verb** — an active mechanic that changes how its turns play, never just "+X to a roll."
4. **Choices that change play, not just math** — every level grants a decision that alters *how* you play; no dead levels.
5. **Engage the challenge, don't delete it** — the system prefers abilities that let you *do something cool during* a challenge over abilities that *bypass* it.

### The core loop
Both first-class pillars share one resolution engine and one action grammar:
- **Combat:** assess the board → spend three actions among genuinely different good options → resolve on four degrees → enemies respond.
- **Social/intrigue:** read the people → spend actions/leverage to shift a tracked social state → resolve on the same four degrees → factions respond.

Starships, vehicles, and exploration are **supporting systems** that reuse this engine with thin bespoke rules.

---

## The core tensions (and how we're resolving them)

Fusing two systems with opposite math creates deliberate tensions. These are tracked and resolved as design progresses:

| # | Tension | Resolution |
|---|---|---|
| **T1** | Bounded accuracy vs. PF2E proficiency scaling | Proficiency ranks gate *quality*, not raw to-hit. Numeric component is small: `1 + lvl//4` plus **+1 per rank**. *(Resolved in Phase 1.)* |
| **T2** | Four-degree crits (beat by 10) vs. flat bounded math | The level term applies **symmetrically** to offense and defense, so it cancels on-level — keeping crit frequency **constant across all 20 levels**. *(Resolved in Phase 1.)* |
| **T3** | No daily resources vs. crunchy class depth | Cooldowns + action-economy are the resource; consumables (money-gated) are the only expendable. *(Formalized in Phase 3.)* |
| **T4** | No spellcasters vs. iconic Force fantasy | Force users are verb-having classes with a broad, cooldown-gated, trait-gated toolkit — never slot-casters. *(Resolved in Phase 5.)* |
| **T5** | Horizontal balance vs. Jedi-vs-farmer power fantasy | Niche over tier: balanced in *contribution*, differentiated in *arena and method*. *(Structured in Phase 5; final balance at Gate A.)* |

---

## Where we are: the build roadmap

The system is built as a dependency cascade, racing to a **playable vertical slice** before any content is mass-produced. Full detail in the [build roadmap](docs/superpowers/plans/2026-06-13-star-wars-rpg-build-roadmap.md).

| Phase | Layer | Status |
|---|---|---|
| **0** | **Design philosophy** — pillars, core loop, budget, audience, scope, tensions, licensing | ✅ **Complete** |
| **1** | **Core mechanic & trait system** — resolution engine, scaling spine, four degrees, action economy, trait framework | ✅ **Complete** |
| **2** | **Character framework** — attributes, skills, derived stats (HP/defenses), class-agnostic recovery | ✅ **Complete** |
| **3** | **Progression chassis** — level cadence, cooldown/resource model, multiclassing | ✅ **Complete** |
| **4** | **Social / intrigue engine** — the co-equal first-class pillar | ✅ **Complete** |
| **5** | **Class design + Force subsystem** — vertical slice (4 classes to L5) | ✅ **Complete** |
| **6** | **Equipment & economy** | ✅ **Complete** |
| **7** | **Creatures & challenge framework** | ✅ **Complete** |
| — | **Milestone: playable vertical slice** ✅ → balance analysis (Gate A) ✅ → **table playtest** | ⏭️ **Next** |
| 8 | **Content expansion** + light supporting systems (starships, exploration) — *in progress: [Species](docs/superpowers/specs/2026-06-15-species-roster.md) (28) · [Backgrounds](docs/superpowers/specs/2026-06-15-backgrounds-roster.md) (36)* | 🔨 **Started** |
| 9 | Rules-writing consolidation → Framework 1.0 | ⬜ Planned |

### What's locked so far (Phase 1 engine)
- **Resolution:** `d20 + Proficiency + Attribute + situational` vs DC; four degrees with natural-20/1 stepping a degree.
- **Proficiency:** Level term `1 + (lvl ÷ 4)` (range 1–6) + Rank term (untrained 0 → legendary 4). Untrained adds nothing; the level term is symmetric across offense and defense.
- **Bonuses:** circumstance / status / item types (no stacking within a type); Multiple Attack Penalty −4 / −8 (agile −3 / −6).
- **Gear math:** item potency is an *optional bounded edge* (+3 cap), not a tax; weapon upgrades primarily scale damage dice.
- **Economy:** three actions, one reaction, free actions; **no daily resource pools**.
- **Engagement:** **ranged is the default** (the balance baseline); melee is deadlier but riskier — a melee Strike provokes a **Reactive Shot** from an armed target (the genre trope flipped: the gunner punishes the swordsman). Force deflection / stealth are the counters.
- **Traits:** universal keyword-tag system with an eight-category taxonomy and an anti-sprawl governance rule.

Full detail: [Phase 1 spec](docs/superpowers/specs/2026-06-13-phase1-core-mechanic-and-traits.md).

### What's locked so far (Phase 2 character framework)
- **Identity:** Species + Class + Background slots.
- **Attributes:** six, modifier-only, classic names (STR/DEX/CON/INT/WIS/CHA); key stat caps +3 at creation, +6 lifetime. DEX de-fanged (initiative → Perception, armor Dex-cap); CHA elevated by the social pillar.
- **Skills:** 14 core skills (ranked proficiency) plus the open **Lore family** (narrow specializations) and separate Perception; broad knowledge skills (Society, Nature, Computers, Repair) carry default Recall Knowledge. **No "Use the Force" skill** (Force is class actions, not a skill).
- **Saves:** Fortitude/CON, Reflex/DEX, Will/WIS.
- **Recovery:** time-gated, not class- or daily-gated — a free *Catch Your Breath* floor (~½ HP) means no mandatory healer; tension comes from denying time.
- **Creation:** bundled decisions + a quick-build per class for a high floor.

Full detail: [Phase 2 spec](docs/superpowers/specs/2026-06-13-phase2-character-framework.md).

### What's locked so far (Phase 3 progression chassis)
- **Levels 1–20**, four tiers (Fringe / Sector / Galactic / Legend).
- **No dead levels:** every level grants a feat or feature (separate class / skill / general / species feat budgets so combat can't crowd out skill picks).
- **Advancement:** pillar-neutral XP (any challenge pays by difficulty) with a milestone toggle.
- **Attribute boosts** at 5/10/15/20 (cap +6); **rank gates** Expert 3 / Master 7 / Legendary 15.
- **Resource model (T3):** action cost + time-based cooldowns (`[once per minute]` ≈ once per fight, `[once per hour]`, trigger-recharge) + legal encounter-scoped pools; no baseline daily clock (per-day reserved sparingly for high level).
- **Multiclassing:** Archetype Dedication (grafting via class feats) — no 1-level dips; the on-ramp for limited Force access.

Full detail: [Phase 3 spec](docs/superpowers/specs/2026-06-13-phase3-progression-chassis.md).

### What's locked so far (Phase 4 social/intrigue engine)
- **Symmetric two-meter duel:** the party empties the opponent's **Resolve** to win them over; the NPC empties the party's **Composure** (Will-derived + situational) to make them cave — both sides *actively attack*.
- **Shares the combat engine** (four degrees, three actions, Will DC, traits) — mastery transfers, no parallel math.
- **Offensive appeals are 2-action** (Make a Case / Press); 1-action supports (Read the Room, Find an Opening, Defuse, Aid, Leverage an Asset) make it a **whole-party activity** — no mandatory "face."
- **Levers & Guards** are situational, not assumed; **escalation bridge** flips a scene to combat carrying social state as conditions.
- **Multi-party** via a single sliding **Favor track** (debate/trial/auction handled as variants).

Full detail: [Phase 4 spec](docs/superpowers/specs/2026-06-13-phase4-social-intrigue-engine.md).

### What's locked so far (Phase 5 class design + Force — vertical slice)
- **Class chassis:** one key attribute (no MAD), HP tiers 6/8/10, a Legendary "proficiency signature" as identity, subclass at L1 (3/7/11/15/19 cadence), a quick-build each.
- **Force subsystem (T4 resolved):** known powers, not slots; **0-cost powers are non-combat utility only** (object telekinesis, senses) while **every combat Force effect costs Attunement** (free combat baseline = weapon + Deflection); an **Attunement** per-encounter pool (`2+L`) refuelled by **Center** and amplified by **Push** (new effects only — numbers auto-scale); five disciplines; **Deflection** universal but Guardian-mastered; `[light]`/`[dark]` trait hooks (full corruption later).
- **Four classes to L5 with distinct verbs:** Soldier (**Suppress**), Scoundrel (**Exploit**), Guardian (**Force Flow + Deflect**), Technician (**Deploy**) — niche-over-tier (T5), no two share a typical turn.
- **Condition list** opened (Off-Guard, Suppressed, Frightened, Prone + social conditions).

Full detail: [Phase 5 spec](docs/superpowers/specs/2026-06-13-phase5-class-design-and-force.md).

### What's locked so far (Phase 6 equipment & economy)
- **Gear is not a power treadmill:** potency stays optional/non-baked, so **credits buy interesting things** (mods, ships, contacts, social Leverage assets), not +X.
- **Weapons:** ranged blaster baseline; **melee adds attribute to damage, ranged doesn't** (ranged scales via weapon specialization); lightsaber `[finesse]`/`[deadly]`, `[Force]`-gated. Transferable **mods** carry damage-dice scaling.
- **Armor:** AC base + Dex-cap by category (crossover ~DEX +3/+4); robed Force users get an unarmored-defense feature.
- **Consumables:** stimpacks (potent first use, **stim tolerance** anti-chain), grenades as the AoE expendable; balance assumes zero use.
- **Economy:** rarity gates access/effects not power; **ship/lifestyle upkeep** is the money sink; each class has a distinct **wealth identity** (Force users buy crystals + holocrons that grant *options*, not numbers).

Full detail: [Phase 6 spec](docs/superpowers/specs/2026-06-13-phase6-equipment-and-economy.md).

### What's locked so far (Phase 7 creatures & challenge — slice complete)
- **Creatures built to a benchmark on the L-spine:** higher attack / lower AC than same-level PCs, so on-level hit/crit rates are **constant at every level** — enemies threaten via **HP + damage + abilities**, never climbing to-hit (the bounded-accuracy thesis, demonstrated).
- **Lethality dial:** standard ~15% of a PC's HP/round, boss ~30%; melee/crits spike above.
- **Roles** (minion→boss); **boss model** = Boss Actions on PC turns + HP-threshold phases + condition-resilience (downgrade, not immunity) + nova check.
- **Unified stat block** carries combat *and* Phase 4 social-defense numbers (Want / Off-ramp / Leverage), so NPCs are statted for both pillars.
- **Slice roster** (Gang Thug → Inquisitor boss); the Inquisitor *deflects blaster bolts* — turning the party's ranged default off and teaching §11 from the enemy side.

Full detail: [Phase 7 spec](docs/superpowers/specs/2026-06-13-phase7-creatures-and-challenge.md).

### System review (post-slice)
A full `ttrpg-system-review` of Phases 0–7 found **no Critical show-stoppers** (no loops/contradictions). Seven Significant load-bearing gaps were resolved in the [connective-tissue remediation](docs/superpowers/specs/2026-06-13-connective-tissue-and-review-remediation.md): stealth/detection, dying/wounded, and initiative (adopted from Paizo ORC); Scene-vs-Encounter keywords; reaction timing & MAP; Force-powers-in-social; and trait-immunity semantics. Six cosmetic issues are parked for later.

### Gate A — balance validation
The [Gate A balance analysis](docs/superpowers/specs/2026-06-13-gateA-balance-validation.md) **passes**: bounded-accuracy math computes (identical 60% hit / 10% crit at L1 and L5), MAP −4/−8 isn't spam-dominant (3rd Strike ~18% of round DPR), the boss model restores a ~2.4:1 action ratio and survives the nova check, and the four classes hold contribution parity. It pins the deferred numbers (DC ladder, lethality, benchmark/creature tables) and converts the T1 watch-item into a content directive: **keep +1/rank, author rank-gated *effects*** so expertise is felt through capability, not bigger numbers.

### Playtest smoke test (Mode B)
A Mode B adversarial [playtest simulation](docs/superpowers/playtests/2026-06-13-playtest-docking-bay-ambush.md) ("Docking Bay Ambush") ran the slice turn-by-turn. **No Critical issues**, and **all four Major findings are now resolved**: F1 the Inquisitor's anti-ranged signature backfired → redesigned with a paired anti-cluster AoE + Phase-2 mode flip, plus a new "close the engagement loop" creature guideline; F2 Reactive Shot now covers gunners within 10 ft of a meleer; F3 the at-will forced-movement exploit → offensive Force costs Attunement + a system-wide stop-at-edge rule (at-will mundane forced movement lives on Athletics Shove/Reposition, melee+MAP); F6/F7 the Attunement and stim numbers are locked and runnable. F4/F5 (drone economy/turn rules) are resolved via a general **Commanded Actor** framework (companions/summons/adds take no actions unless Commanded — 1 action → 2 weaker actions, on your turn, no own initiative).

### Mode A gate (high-fidelity playtest)
A [Mode A subagent-table playtest](docs/superpowers/playtests/2026-06-14-playtest-modeA-docking-bay-gate.md) (GM agent with full specs; four **blind** adversarial player agents) re-ran the docking-bay encounter for 2 rounds. **No Critical issues — the F1–F7 fixes held under blind play** (Reactive Shot, the pit anti-cheese tested from three angles, and the drone economy all behaved). It surfaced three new **Major** findings the all-knowing passes missed: **MA1** the boss's *Deflect Blaster Bolts* has no defined value and the working number (−10) makes it immune to small-die ranged; **MA2** the Inquisitor's anti-cluster Repulse *scatters its own melee targets* (its two signatures are tactically self-interfering); **MA3** the adds collapse in 2 rounds, exposing the solo-boss action economy. Plus a stack of rules-writing/undefined-number Minors. Untested: the Phase-2 mode flip and the solo-boss endgame.

### Skill actions
The [Skill Actions spec](docs/superpowers/specs/2026-06-14-skill-actions.md) defines what each of the 14 skills *does* — adapted from the **Starfinder 2E** action set (ORC), cut to our skills, with the tech split (Computers = slicing, Thievery = mechanical, Repair = fabrication) and the CHA skills running dual-mode (exploration actions + Phase 4 social appeals). Four-degree outcomes on the tactical actions are the anchors for the rank effects below.

### Rank-gated effects (Gate A T1 directive — done)
The [rank-gated-effects spec](docs/superpowers/specs/2026-06-14-rank-gated-effects.md) makes expertise *felt through capability, not bigger numbers* — fulfilling the Gate A directive. Under a binding **gating philosophy** (permission open, outcome gated: anyone may *attempt* nearly any action; rank improves the *result*, with hard locks only on a few flagged `[trained-required]` actions), Expert/Master/Legendary grant new degree outcomes, action modes, success riders, and removed proficiency-limits — all purely additive (no lockouts). Effects attach to the skill/proficiency (whoever reaches the rank), not the class. Remaining before a Mode A gate: the ammo cosmetic (C2).

---

## Repository structure

```
.
├── README.md                          ← you are here
├── docs/
│   └── superpowers/
│       ├── specs/                     ← design specifications (the "what" and "why")
│       │   ├── 2026-06-13-star-wars-rpg-design-philosophy.md
│       │   ├── 2026-06-13-phase1-core-mechanic-and-traits.md
│       │   ├── 2026-06-13-phase2-character-framework.md
│       │   ├── 2026-06-13-phase3-progression-chassis.md
│       │   ├── 2026-06-13-phase4-social-intrigue-engine.md
│       │   ├── 2026-06-13-phase5-class-design-and-force.md
│       │   ├── 2026-06-13-phase6-equipment-and-economy.md
│       │   ├── 2026-06-13-phase7-creatures-and-challenge.md
│       │   ├── 2026-06-13-connective-tissue-and-review-remediation.md
│       │   ├── 2026-06-13-gateA-balance-validation.md
│       │   ├── 2026-06-14-skill-actions.md
│       │   ├── 2026-06-14-rank-gated-effects.md
│       │   ├── 2026-06-15-creation-slot-contributions.md
│       │   ├── 2026-06-15-species-roster.md
│       │   └── 2026-06-15-backgrounds-roster.md
│       └── plans/                     ← build roadmaps and implementation plans (the "in what order")
│           └── 2026-06-13-star-wars-rpg-build-roadmap.md
└── starwarsrpgv2.code-workspace
```

Each phase produces a spec under `docs/superpowers/specs/`, is ratified before the next begins, and is committed to git so every design decision is versioned.

---

## How we work

Design proceeds **one layer at a time**, collaboratively:
1. A layer is designed against the pillars and tensions above, surfacing every real decision as an explicit fork with a recommendation.
2. Decisions are ratified, then written into a spec document and committed.
3. The next dependent layer begins.

Numbers flagged *(Gate A)* in the specs are provisional pending a balance-analysis pass once the vertical slice exists; structure is fixed, some values are tunable through playtest.

---

## Licensing & content sourcing

This is a **binding project constraint** (see philosophy spec §0). Rules content is drawn **only** from material the original publishers have released for open community use, with required attribution:

- **Paizo (PF2E / SF2E):** content released under the **ORC License** (Open RPG Creative License).
- **Wizards of the Coast (D&D 5E):** content in the **SRD 5.1 / 5.2**, released under **CC-BY-4.0**.

Game *mechanics* are not copyrightable, but specific *text* and *named creative content* are — so mechanics are paraphrased in our own words and verbatim text is pulled only from openly-licensed sources, with attribution.

> **Separate, unsolved concern:** the **Star Wars setting** is Disney/Lucasfilm intellectual property and is *not* covered by these open RPG licenses. This project currently governs the **rules engine** only; any setting/IP usage is a distinct decision to be made before public distribution.

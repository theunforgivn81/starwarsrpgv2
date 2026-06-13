# Star Wars RPG — Design Philosophy

**Status:** Approved (philosophy layer)
**Date:** 2026-06-13
**Scope of this document:** The five design commitments every later mechanic is tested against. Mechanics are deliberately *not* resolved here — see "Next Steps."

---

## Lineage (one-line summary)

PF2E/SF2E **structure** (universal traits, proficiency ranks, four-degree success, three-action economy, status/circumstance bonuses only, attributes-as-modifiers) crossed with D&D 5E **bounded accuracy**, with two pillars most d20 systems rely on deliberately removed: the **daily resource clock** and the **dedicated healer**.

---

## 1. Design Pillars

Each pillar is falsifiable — the rule it *rejects* is named in italics.

1. **Bounded participation.** A character several levels below an encounter can still meaningfully act in it; the level gap shows up in *options and resilience*, not in whether the dice can connect. *(Kills: any "cannot hit / cannot fail" scaling wall; any DC unreachable for the untrained.)*

2. **No mandatory seats.** Every required party function — damage, durability, healing, face, tech — is reachable by multiple classes, by skills, or by gear. An all-scoundrel table and an all-Jedi table are both fully viable. *(Kills: a class whose absence makes a pillar unplayable, e.g. "no Force-healer = no recovery.")*

3. **Every class has a verb.** Each class owns an *active* gameplay mechanic that changes how its turns — and ideally the party's turns — play out. A class is never defined by "+X to a roll." *(Kills: a class whose identity is bigger numbers; "auto-succeed at this pillar" abilities that ask nothing of the player.)*

4. **Choices that change play, not just math.** Every level grants at least one decision that alters *how* the character plays, so two same-class/same-species characters diverge by low levels. No dead levels. *(Kills: a level granting only a numerical bump; a "feat" that is strictly a stat increase with no new action or option.)*

5. **Engage the challenge, don't delete it.** Between an ability that lets a player *do something cool during* a challenge and one that lets the party *bypass* it, the system always prefers the former. *(Kills: passive "skip the lock / skip the negotiation / skip the trap" abilities, even when mechanically efficient.)*

---

## 2. Core Loop

The two first-class pillars **share one resolution engine and one action grammar**, so mastery transfers and players aren't learning two games.

- **Combat:** assess the board → spend three actions among genuinely different good options → resolve against a four-degree outcome → enemies and environment respond.
- **Social/intrigue (co-equal pillar):** read the situation and the people → spend actions/leverage to shift a tracked social state (disposition, suspicion, faction standing) → resolve against the same four-degree engine → NPCs and factions respond.

Starships, vehicles, and exploration are **supporting systems** that reuse this engine with thin bespoke rules — never their own full subsystem. (A starship chase should be learnable in ~2 minutes by anyone who knows combat.)

---

## 3. Complexity Budget — **High**, spent on the core loop first

- **Spend freely on:** the three-action combat engine, the social/intrigue engine, class verbs, and the trait web tying them together.
- **Keep deliberately cheap:** starships/vehicles, exploration, crafting, downtime — thin rules reusing the core engine.

Bounded accuracy is a budget *ally*: a small per-level math gap means we avoid per-tier retuning of every DC, stat block, and item. The crunch we keep is **tactical** (options on a turn), not **arithmetical** (recomputing the same check at every tier).

---

## 4. Audience Matrix

| Axis | Position | Reconciliation / rationale |
|---|---|---|
| Engagement | **Hardcore-leaning, high floor** | Mastery (build, action sequencing) raises the ceiling; bounded accuracy + horizontal balance mean a naive build is still functional. Mastery never gates the floor. *(This is the deliberately-built bridge for the hardcore/casual tension.)* |
| Orientation | **Tactical, with a real narrative pillar** | Combat is tactical-first; social/intrigue is co-equal and first-class, so this is not a pure wargame. |
| Format | **Long campaign** | The per-level "meaningful choice" pillar only pays off across a full progression arc. Progression matters. |
| Authority | **Rules-centered** | Four-degree DCs, explicit machine-readable traits as prerequisites, constrained bonus types — disputes resolve by procedure, not ruling. |

---

## 5. Scope Statement

> A high-crunch, tactically deep Star Wars system where character power comes from **renewable** options — action economy and cooldowns — rather than a daily resource clock, letting any party composition (all-Jedi to all-scoundrel) play at the same table with no mandatory roles.

**The novelty** is the *removal* of the daily resource clock and the dedicated healer. Most design effort goes into proving the game stands without them.

---

## Acknowledged Tensions & Recommended Leans

Recorded as guiding direction; precise mechanics are deferred to `ttrpg-core-mechanic`.

| # | Tension | Lean |
|---|---|---|
| **T1** | Bounded accuracy vs. PF2E proficiency-rank scaling. | **Bounded accuracy wins.** Proficiency ranks gate *quality* (access, riders, crit effects), not raw to-hit. Numeric component is small: the `1 + (level // 4, min 1)` term **plus +1 per proficiency rank** (untrained → legendary). *Note: +1/rank is provisional — revisit if specialists don't feel distinct enough from the untrained; the preferred fix is rank-gated effects, not bigger numbers.* |
| **T2** | Four degrees (crit on ±10) vs. flat bounded math. | **Preserve four degrees; don't let crits hinge on the ±10 band alone.** Use nat-20/nat-1 escalation and crit-enabling traits/conditions so crit frequency stays stable across the level band. (Deferred to core-mechanic.) |
| **T3** | No daily resources vs. high-crunch class depth. | **Cooldowns + action-economy are the resource.** Depth comes from *when/how* actions are spent and which cooldowns are live. Consumables (money-gated) are the only expendable, tying class balance to the equipment economy. |
| **T4** | No traditional spellcasters vs. iconic Force fantasy. | **Force users are classes with verbs, balanced horizontally.** Versatility from a broad, cooldown-gated power list + trait-gated access — not a slot-based list that outclasses martials. A Jedi is *different*, never strictly *more*. |
| **T5** | Horizontal balance vs. fantasy power gap (Jedi vs. moisture farmer). | **Niche over tier.** Balanced in *contribution*, differentiated in *arena and method*. Setting "power" is expressed through narrative authority and trait access, not win-more numbers. |

---

## Key Decisions Captured

- **Power band:** Full spectrum — system must support all-scoundrel through all-Jedi tables with horizontal class balance.
- **First-class pillars:** Ground combat + social/intrigue (sharing one engine). Starships/vehicles/exploration are lightweight supporting systems.
- **Recovery model:** Decoupled from class and mostly from combat. In-combat patching exists as a tactical *option* (consumables, Medicine skill, a few class abilities); the bulk of recovery happens in exploration/downtime via something any character can do. No mandatory in-combat healer. Not gritty/slow; not a daily clock.

---

## Next Steps (not part of this document's scope)

1. `ttrpg-core-mechanic` — resolution system: dice, exact proficiency formula, four-degree thresholds under bounded math (resolves T1 numbers + T2), action economy specifics, bonus-type rules.
2. `ttrpg-character-framework` — attributes-as-modifiers, skill/proficiency structure, character creation skeleton.
3. Then content tiers: classes (`ttrpg-class-design`), the Force-user framework, progression (`ttrpg-progression-design`), equipment/economy (`ttrpg-equipment-design`), creatures (`ttrpg-creature-design`).

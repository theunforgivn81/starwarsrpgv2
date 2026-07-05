# Phase 4 — Social / Intrigue Engine

**Status:** Approved
**Date:** 2026-06-13
**Roadmap phase:** 4 of 9 — see [build roadmap](../plans/2026-06-13-star-wars-rpg-build-roadmap.md)
**Upstream:** [Philosophy](2026-06-13-star-wars-rpg-design-philosophy.md), [Phase 1 — Core Mechanic & Traits](2026-06-13-phase1-core-mechanic-and-traits.md), [Phase 2 — Character Framework](2026-06-13-phase2-character-framework.md), [Phase 3 — Progression Chassis](2026-06-13-phase3-progression-chassis.md)
**Resolves:** the **co-equal second pillar** (core loop); Pillar 5 (engage the challenge, don't delete it) at the social layer; Pillar 2 (social is a whole-party activity, no mandatory "face").

> *(Gate A)* = provisional pending balance calibration. *(content: Phase N)* = a slot filled later. The engine deliberately **reuses the combat resolution engine** (four degrees, three-action economy, status/circumstance bonuses, traits) so mastery transfers and the two pillars don't feel like two games.

---

## 1. When the Engine Engages

Only for **social encounters with real stakes** — a negotiation, interrogation, standoff, debate before a council, or winning over a faction broker. Routine conversation stays light (roleplay + the occasional single check), per "only roll when failure is interesting." The full engine is reserved for set-piece social scenes, exactly as the combat engine is reserved for fights.

---

## 2. The Symmetric Two-Meter Model

Social play mirrors combat's structure — two opposed "HP bars," and **both sides actively attack**:

| Meter | Held by | Attacked by | At 0 |
|---|---|---|---|
| **Resolve** | the NPC / opposing side | the **party** (appeals) | they are won over — final degree sets how favorable the terms |
| **Composure** | the party (or an individual PC) | the **NPC** (its appeals) | the party caves, accepts bad terms, or is out-maneuvered |

The NPC is an **active opponent**, not a passive target: it spends its turns attacking Composure and defending its Resolve. First side to empty the other's meter wins the exchange.

### 2.1 Sizing the meters

- **NPC Resolve** and **Party Composure** are **scene-scoped**, sized by difficulty like an encounter budget *(Gate A: e.g., Resolve/Composure ≈ 4 trivial / 8 standard / 12+ "social boss")*. They are **not** permanent sheet stats.
- **Composure base derives from Will** (anchored on the lead spokesperson's Will, or the best Will among active participants), then the GM applies **situational starting modifiers** (home turf or holding leverage = bonus; desperate supplicant or caught in a lie = penalty). NPC Resolve is sized the same way (its Will + situational standing).
- **Shared by default; individual when it matters.** Most scenes use one shared Party Composure. Duel/temptation/interrogation scenes may instead give a single PC their own Composure (a Sith tempting one Jedi).
- **Social bosses** (a lone NPC vs the whole party) need elevated Resolve and likely extra actions/reactions, paralleling solo-creature action-economy — formalized in Phase 7.

---

## 3. Turn Structure

- Social encounters run in **exchanges** (rounds), each participant getting the standard **three actions**. **No grid** — "position" is *informational* (what you know about the other side), never spatial.
- Turn order is **fiction-arbitrated** (no initiative roll needed); a light round-robin in multi-party scenes (§7).
- **No appeal Multiple-Attack Penalty.** Because appeals are 2-action activities (§4), you cannot make two in a 3-action turn — the action cost is itself the anti-repetition limiter, so no special penalty is needed.

---

## 4. The Standard Action Suite

Available to anyone in a social encounter (the social equivalent of Strike/Stride/Step). Class-specific social *verbs* come in Phase 5 and benchmark against these.

**Appeals** roll a chosen **approach** — **Diplomacy** (reason/rapport), **Deception** (mislead), or **Intimidation** (threaten) — vs the opponent's **Will DC** (`10 + Will mods`; reuses existing math, bounded accuracy intact). A situational **Lever** grants a circumstance bonus; a situational **Guard**ed approach takes a penalty or is negated.

### Offensive actions (2-action activities)

**Make a Case** — `[appeal]` `[mental]` `[linguistic]`, **2 actions**, at-will
- Crit success: opponent Resolve/Composure **−3**
- Success: **−2**
- Failure: no effect (lost tempo, like a missed Strike)
- Crit failure: the opponent **reacts** — Stands Firm, gains a Guard, or makes a free Counter

**Press** — `[appeal]` `[mental]` `[linguistic]` `[press]`, **2 actions**, at-will
- Crit success: **−4**
- Success: **−3**, but you expose yourself (opponent gains a reaction *or* you take a Composure hit)
- Failure: no effect
- Crit failure: opponent gets a **free Counter**
- *Niche: closing fast when you can afford the exposure; worse than Make a Case when you're on the back foot.*

### Supporting actions (1-action)

| Action | Effect | Niche |
|---|---|---|
| **Read the Room** (Sense Motive) | Perception/relevant vs opponent's Deception or Will DC; reveal a situational Lever, a Guard, or rough meter state | recon — makes appeals land harder |
| **Find an Opening** (Feint) | Deception vs Perception DC; your next ally's appeal gains a circumstance bonus (or exploits a Lever) | the setup that lets non-faces drive wins |
| **Defuse** | skill check to **restore** your side's Composure | the "heal" when your nerve is breaking |
| **Aid** | standard Aid: +circumstance to an ally's next check | universal teamwork |
| **Leverage an Asset** — `[social]` | **1 action**; expend a concrete Asset (evidence, blackmail, gift, favor, bond) for a no-roll effect: Resolve **−2** and/or remove a Guard / open a Lever | priced like a consumable; rewards exploration prep. Limited by asset scarcity, not action cost |

---

## 5. Levers & Guards (situational, not assumed)

- **Most encounters have none** — a plain Resolve-vs-Composure contest.
- The GM adds a **Lever** (an exploitable value/desire/weakness — held blackmail, a loved one, greed) or a **Guard** (a defended approach — a fanatic guards against bribery) **only when the fiction supports it.** They apply to **either side** (a PC's secret is a Lever the NPC can exploit).
- **Recon** (Read the Room / the NPC's Probe) is how Levers and Guards are *discovered* when present. A known Lever → circumstance bonus / extra meter damage with the matching approach; a Guard → penalty or negation on that approach.
- PC-side Levers derive from **backgrounds/bonds/flaws** (light, narrative; content in later phases).

---

## 6. The NPC's Turn

The NPC acts from its **social stat block** (a "social role/difficulty," formalized in Phase 7). Its actions mirror the PC suite:

| NPC action | Effect |
|---|---|
| **Counter** (`[appeal]`, 2 actions) | reduce **Party Composure** |
| **Pressure** (`[appeal]` `[press]`, 2 actions) | reduce Composure harder, exposing itself |
| **Probe** (1 action) | discover a PC's Lever |
| **Stand Firm** (1 action) | recover its own Resolve / raise a Guard |
| **Demand / Reframe** (1 action) | change the terms or impose a Guard on the party |
| **Behavioral triggers** | **Disengage** (attempt to end the scene when cornered) · **Escalate** (flip to combat — e.g., on a crit-failed threat) |

---

## 7. Multi-Party Encounters

The engine generalizes from "one target" to **N participants + an optional Adjudicator**, using a single new tool kept deliberately light:

- **Favor track** — a sliding **tug-of-war meter** for any scene where you sway a *third party* rather than deplete an opponent directly. Each side's successful appeals (vs the Adjudicator's Will DC, modified by the Adjudicator's situational Levers/Guards — "this council values tradition") pull Favor their way; reaching your end wins. Sides may also **Rebut** (attack a rival's Composure to deny them tempo). The Adjudicator **reacts** rather than taking full turns (e.g., a pointed question = the targeted side makes a check or loses Favor).
- **Canonical use: Debate / Trial** before a council, judge, or crowd.
- **Mediation and Auction are handled ad hoc** as applications of the Favor track + the core duel (close the gap between two parties by swaying each; bid while swaying the seller's Favor and discrediting rivals) — **no bespoke subsystems.** GM guidance, not new rules surface.
- Turn order with many participants: light GM-arbitrated round-robin.

---

## 8. Outcomes, Escalation, Conditions

- **Win (opponent Resolve → 0):** goal achieved; the *final degree of success* sets how favorable the terms (crit = extra concessions). **Loss (Party Composure → 0):** the party caves, accepts worse terms, or the NPC ends it on their terms.
- **Escalation bridge:** if a scene turns violent it converts to a normal combat encounter — roll initiative, and **social state carries over as conditions** (a Rattled NPC enters Frightened; a winning party gains an opening). Shared engine = seamless transition.
- **Social conditions** (status effects, from the shared condition list finalized in Phase 5): e.g., **Off-Balance** (a landed Feint — vulnerable to the next appeal), **Guarded** (hardened), **Rattled** (Intimidation landed). They impose **Status** modifiers, slotting into the Phase 1 architecture.
- **Optional Suspicion overlay:** for infiltration/deception scenes, add a **Suspicion clock** (a danger clock filling on failures; maxing = cover blown) atop the core duel. Optional, so the base engine stays lean.

---

## 9. Faction Standing (light campaign layer)

A persistent reputation track per faction (**Hostile → Disliked → Neutral → Liked → Allied**). Social-encounter outcomes and notable deeds move it. It sets the **starting Disposition** (opening Resolve/Composure modifiers) for future encounters with that faction and gates `[faction]`-trait feats, gear, and contacts. Deliberately light — campaign-scale, not per-exchange crunch.

---

## 10. The Social Stat Block

A social encounter runs from a compact block (parallel to a creature stat block; format finalized in Phase 7 / rules-writing):

```
[NPC / Side name]            Disposition: [Hostile…Allied]
Resolve: [n]    Will DC: [n]    Composure attack: [approach/bonus]
Levers (if any): […]         Guards (if any): […]
Notable actions / triggers: [Stand Firm, Disengage at low Resolve, Escalate if threatened…]
```

---

## 11. Worked Example (exit-gate demonstration)

*The party needs a corrupt dock official (Resolve 8, Will DC 16, Composure attack via Intimidation +8; Guard: vs Intimidation — he has Imperial backers, so threats harden him) to release an impounded ship. Party Composure 8.*

- **Slicer**, *Read the Room* (1 action): success — reveals the Guard (Intimidation backfires) and a **Lever** (he's deep in gambling debt → greed). Then *Aid* (1 action) sets up the Face.
- **Face**, *Make a Case* with **Diplomacy**, exploiting the greed Lever (+circ from Lever, +circ from Aid): crit success → **Resolve −3** (now 5). Spends remaining action to *Find an Opening* for next round.
- **Official's turn:** *Counter* (Intimidation, 2 actions) vs Party Composure → success, **Composure −2** (now 6); *Probe* (1 action) → learns the Face is wanted by a rival syndicate (a PC Lever).

Two genuinely different good options are live every turn (appeal vs set-up vs defuse vs leverage), the whole party contributes (slicer's recon, face's appeal), and the official **pushes back** — satisfying the exit-gate test.

---

## 12. Exit-Gate Checklist (per roadmap)

- [x] A runnable social scene resolves entirely through the engine (§11).
- [x] At least two genuinely different good action choices per turn (§4, §11).
- [x] Shares the core resolution engine (four degrees, three actions, status/circumstance, traits) — no parallel math.
- [x] **Pillar 5:** appeals *engage* the scene; there is no single "win the negotiation" button (offensive actions are 2-action, contested, and reversible by the opponent).
- [x] **Pillar 2:** structurally a whole-party activity (recon, setup, leverage, aid) — no mandatory "face."
- [x] NPC is an active opponent, not a passive target (§6).
- [x] Multi-party handled (Favor track + presets) (§7).

## 13. Carried Forward (open items for later phases)

- **Class-specific social verbs & encounter pools** (e.g., a face's signature appeals) → Phase 5. *(First delivered 2026-07-05: the Consular Dominance Mandate's **Whispered Doubt** — see the [Consular Mandate rework](2026-07-05-consular-mandate-rework.md).)*
- **Shared condition list** (Off-Balance, Guarded, Rattled, etc.) → Phase 5.
- **PC Lever sources** (background/bond/flaw content) → background content phase.
- **Social stat-block format, social-boss action budgets, Adjudicator templates** → Phase 7.
- **Meter sizes, Composure base formula, appeal potency, Favor thresholds** → Gate A.

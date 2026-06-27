# Phase 5 — Class Design & the Force Subsystem (Vertical Slice)

**Status:** Approved
**Date:** 2026-06-13
**Roadmap phase:** 5 of 9 — see [build roadmap](../plans/2026-06-13-star-wars-rpg-build-roadmap.md)
**Upstream:** [Philosophy](2026-06-13-star-wars-rpg-design-philosophy.md), [Phase 1 (+§11 combat engagement)](2026-06-13-phase1-core-mechanic-and-traits.md), [Phase 2](2026-06-13-phase2-character-framework.md), [Phase 3](2026-06-13-phase3-progression-chassis.md), [Phase 4](2026-06-13-phase4-social-intrigue-engine.md)
**Resolves:** T4 (Force users as verb-having classes, not slot-casters), T5 (niche over tier), Pillar 3 (every class has a verb), Pillar 4 (no dead levels). Closes the deferred **condition list**.
**Scope:** a **vertical slice** — the class chassis, the Force subsystem, and **four classes to level 5** (one per archetype). Not a full roster; the full roster comes in Phase 8 after the slice is playtested.

> *(Gate A)* = provisional pending balance calibration. Numbers are deliberately light; the structures and identities are fixed.

---

## 1. The Class Chassis

Every class plugs into the Phase 3 per-level chassis (feats/boosts/skill increases) and additionally defines:

| Element | Convention |
|---|---|
| **Key attribute** | exactly one (drives class DC/attack); features key off it to avoid MAD |
| **HP value** | three tiers — **6 / 8 / 10** per level (+ CON + species base) |
| **Proficiency signature** | each class reaches **Legendary** in exactly one signature thing and caps lower elsewhere — *what you get Legendary in is identity* and a bounded-accuracy differentiator (shape, not sum) |
| **The verb** | the signature active mechanic, **online at level 1**, upgraded at tier boundaries |
| **Class resource** | optional texture (encounter pool / stance / building stacks / risk meter) |
| **Subclass** | chosen at **level 1**; subclass features land on the shared **3 / 7 / 11 / 15 / 19** cadence and *modulate* the verb (never replace it) |
| **Quick-build** | every class ships one (recommended species, boosts, skills, gear) to keep the floor high |

Proficiency ranks advance within the Phase 3 gates (Expert L3 / Master L7 / Legendary L15).

---

## 2. The Force Subsystem (resolves T4)

### 2.1 Architecture — known powers + an encounter pool, never slots

- **Force powers are abilities** with the `[Force]` trait, gated by **action cost + Attunement + cooldowns** — never prepared per day. A Force user has a toolkit of **known powers** (chosen at level-up), each **always available**. **Versatility = breadth known; depth = Attunement management.**
- **Numbers auto-scale with level** (bounded, automatic — a low-level power stays relevant without re-selection).
- **Disciplines** (the `[Force]` sub-traits; trait-gate access): **Telekinesis**, **Sense**, **Vitality** (the *optional* heal), **Influence** (`[mental]`), **Battle** (deflection/enhancement). A class grants access to *some*; subclass/feats expand — giving Force classes distinct discipline profiles. *(**Amended 2026-06-15:** superseded by the **six tradition-split schools** — Jedi: Control/Sense/Alter · Sith: Body/Mind/Offense — in the [Shared Force Toolkit](2026-06-15-shared-force-toolkit.md). Battle splits into Control (defensive) + Offense (destructive); the other four map 1:1.)*

### 2.2 Attunement (the resource texture)

- **Per-encounter pool = `2 + L`** (the Phase 1 level term) → 3 at L1, 4 at L5, 5 at L9, 6 at L13, 7 at L17. **Resets each encounter** (T3-compliant). *(Locked, resolving playtest F6; provisional pending next playtest.)*
- **0-cost powers are *non-combat utility only*** (at-will): retrieving/manipulating **unattended objects** at range, **enhanced Force senses** (precognition/perception), and similar minor effects. A 0-cost power **never** offensively targets a creature, forces movement, deals damage, debuffs, heals, or buffs. *(Revised per playtest F3 — see economy rule below.)*
- **Economy rule (F3):** **every Force effect with a combat impact costs Attunement (≥1)** — offense, forced movement, control, debuffs, healing, and buffs. A Force user's **free combat baseline is their weapon Strikes + Deflection** (defense), so they never gas out *defensively* (which would gut the §11 counter) or on baseline weapon offense; *powers* are the resourced spice/burst.
- **Power costs:** standard powers **1–2**, signature/big powers **3**. **Push** adds **+1** (extra target / knock prone) or **+2** (bigger upgrade) per added effect/mode — **never** raw numeric scaling (that's automatic by level).
- **Center** — `[Force]` `[concentrate]`, **1 action**: regain **2 Attunement** (cannot exceed pool max). The active refuel — the *cast-now-vs-meditate* tension. Center costs an action of *effect* (not an action of value), so there is **no action-positive loop**; sustaining ~one power per turn is the intended measured rhythm, with the pool allowing a frontloaded burst.
- **Force DC** = class DC (`10 + L+R + key attribute`); key attribute set per class (no MAD).

### 2.3 Deflection (universal; the §11 melee-risk counter)

**Every Force user** can adopt the **Deflecting Stance** (§4.3), the structural reason a Force user can close on gunners. **Guardians are the masters** (the reactive Deflect, redirects, stronger bonuses). This satisfies the user requirement that Deflection be universal but Guardian-superior.

### 2.4 Access & light/dark

- **Trait-gated:** Force powers require the `[Force]` trait — from a Force class or the **Force Adept archetype** (Phase 3 on-ramp for limited dabbling). No casual access.
- **Light/Dark** is a cross-cutting `[light]`/`[dark]` trait, not a discipline. Dark powers are "more potent at a cost," handled ad hoc for now; a **full Dark-Side corruption subsystem is deferred to Phase 8**.

---

## 3. SOLDIER — *"lock down a field of fire"*

**Identity:** a military professional who controls space with fire. **Typical turn:** ranged Strike, then **Suppress** a foe so it can't move or shoot freely. **Verb: Suppression.**
**Role** 3/2/3/1/1/0/1 · **Key** DEX · **HP** 10 · **Signature** Legendary weapons (best pure shooter); strong Fortitude.
**Subclasses (L1):** **Vanguard** (frontline, area suppression, heavy armor) · **Sharpshooter** (single-target, long range, called shots) · **Commando** (explosives, mobility).

**Signature — Suppressing Fire** `[attack]`, **2 actions.** Make a ranged Strike. Whether or not it hits, the target is **Suppressed** until the start of your next turn: it's Off-Guard and takes −2 circumstance to attacks; if it uses a move action or makes a ranged Strike, you may **Reactive Shot** it (extends the Reactive Shot to a ranged trigger). *Niche: pinning a shooter/approach; loses to a plain double-Strike for raw burst.*

**Levels 1–5 (class-specific, atop the chassis):**
| L | Soldier grants |
|---|---|
| 1 | Key DEX; trained weapons/armor & class DC; **Suppressing Fire**; **subclass** + its L1 feature; trained Fortitude→expert |
| 2 | Class feat (e.g., *Reactive Volley* — a 2nd reaction/round usable only for Reactive Shots) |
| 3 | **Subclass feature**; weapons → expert; (chassis: general feat, skill increase) |
| 4 | Class feat (e.g., *Suppressing Barrage* — Suppress a 10-ft burst) |
| 5 | Weapons → master gate prep (master at L7); *Pinning Shot* (Suppressed targets also can't Step); (chassis: boosts, species feat, skill increase) |

---

## 4. GUARDIAN (Force) — *"flow between blade and power"*

**Identity:** a Force warrior alternating lightsaber and power. **Typical turn:** saber Strike + spend Attunement on telekinetic control, or hold a deflecting posture to wade through fire. **Verb: Force Flow.**
**Role** 3/1/3/1/2/1/0 · **Key** WIS (Force DC) · **HP** 10 · **Signature** Legendary Force + lightsaber.
**Disciplines:** Battle + Telekinesis (core), limited Sense; subclass expands.
**Subclasses (L1):** **Sentinel** (deflection/defense master) · **Warrior** (aggressive saber, Telekinesis) · **Seer** (Sense, more powers).

### 4.1 Signature — the Force kit

**Lightsaber** uses `[finesse]` (DEX) for Strikes and `[deadly]` crits — high melee lethality (§11 "deadly").

**Telekinetic Nudge** `[Force]` `[telekinetic]` `[concentrate]`, **1 action, 1 Attunement.** *(Costed — it offensively targets a creature, per the F3 economy rule.)* A creature within range attempts a **Fortitude save** vs your Force DC; on a **failure** it's shoved **5 ft** (**crit failure**: 10 ft + prone), distance auto-scaling modestly by tier. **Forced movement stops at the edge of a precipice/hazard** — it cannot push a creature into a fall or hazard ([connective-tissue §G](2026-06-13-connective-tissue-and-review-remediation.md)). *Push:* **+1** add a target *or* knock prone on a normal failure; **+1** fling a grabbed unattended object as a ranged Strike; **+2 (Hurl)** the movement *may* carry the target off an edge / into a hazard — it attempts a **basic Reflex save** to stop at the brink. *(0-Attunement telekinesis is limited to unattended objects + senses, §2.2.)*

### 4.2 Center & Attunement
Guardians have an Attunement pool *(size: Gate A)* and the **Center** action (§2.2).

### 4.3 Deflecting Stance (universal Force baseline; Guardian-enhanced)

**Deflecting Stance** `[stance]` `[Force]` `[battle]`, **1 action.** While in this stance: (1) your melee Strikes **don't provoke Reactive Shots**; (2) +1 circumstance to AC vs ranged attacks. *(Available to **all** Force users.)*
**Guardian mastery (L1 class feature):** also gain **Deflect** `[reaction]` — Trigger: hit by a ranged Strike while in Deflecting Stance; Effect: reduce the damage (by your level + a value), and on your crit/their crit-fail margin, **redirect** the shot at another creature. Guardian's stance AC bonus scales (+1→+2→+3 at tier boundaries).

**Levels 1–5:**
| L | Guardian grants |
|---|---|
| 1 | Key WIS; trained saber/Force & class DC; **Deflecting Stance + Deflect (mastery)**; **Telekinetic Nudge** + 1 known power; **Attunement**; **subclass** + L1 feature |
| 2 | Class feat (a known power or saber technique) |
| 3 | **Subclass feature**; Force → expert; +known power; (chassis grants) |
| 4 | Class feat |
| 5 | saber/Force step; stance bonus → +2; +known power; (chassis: boosts, etc.) |

---

## 5. SCOUNDREL — *"turn angles into advantage"*

**Identity:** a fringe operator who weaponizes positioning and talk. **Typical turn:** set up or exploit a weakness for a precise Strike, then talk/slip clear. **Verb: Exploit.**
**Role** 2/0/1/1/1/3/3 · **Key** DEX · **HP** 8 · **Signature** Legendary skills (most in the game); great Reflex.
**Subclasses (L1):** **Gunslinger** (ranged trick-shots) · **Operator** (stealth/infiltration) · **Face** (con artist; bonus social verbs that plug into Phase 4).

**Signature — Exploit** (passive). When you Strike a creature **Off-Guard to you** or that you've **Studied**, deal **+1 precision damage die** (auto-scales).
**Study a Mark** `[concentrate]`, **1 action.** Choose a creature you can see; until the end of your next turn it's Exploited by you, and you learn one defense/weakness (an always-on Recall-Knowledge-lite benefit — never a dead action). *Niche: burst on a set-up/flanked target; rewards stealth, feints, teamwork; weak vs aware foes in the open — by design (feast mitigated by Study's info).*

**Face note (Phase 4 tie-in):** the Face subclass grants signature **social verbs** that benchmark against the Phase 4 standard suite (e.g., a 1-action Feint that also opens a Lever) — the Scoundrel's social spotlight.

**Levels 1–5:**
| L | Scoundrel grants |
|---|---|
| 1 | Key DEX; trained skills (extra) & class DC; **Exploit + Study a Mark**; **subclass** + L1 feature; skills → expert (one) |
| 2 | Class feat + skill feat |
| 3 | **Subclass feature**; an extra skill to expert; (chassis) |
| 4 | Class feat + skill feat |
| 5 | Exploit → +2 precision dice; a skill to master prep; (chassis) |

---

## 6. TECHNICIAN — *"deploy tech to multiply the party"*

**Identity:** a gadgeteer force-multiplier; the party's "no-cleric" support engine. **Typical turn:** command a drone, drop a device, patch/buff an ally. **Verb: Deploy.**
**Role** 1/2/1/3/2/1/1 (sum 11) · **Key** INT · **HP** 8 · **Signature** Legendary Computers/Repair + gadget DC.
**Subclasses (L1):** **Droid Tech** (combat drone) · **Field Medic** (stims/healing gadgets) · **Saboteur** (mines/slicing/zones).

**Signature — Command Drone** `[manipulate]`, **1 action.** Your **Drone** (a `[companion]` Commanded Actor — [connective-tissue §F](2026-06-13-connective-tissue-and-review-remediation.md); scales with you) takes **up to 2 actions**: Stride, ranged Strike, Aid, or activate a gadget. **Uncommanded it takes no actions** (it holds) — so it never grants free action economy (resolves playtest F4); it acts on your turn with no separate initiative or reaction (resolves F5).
**Deploy Device** `[manipulate]`, **2 actions, `[once per minute]`.** Place a gadget: **turret** (ranged Strikes), **shield emitter** (allies within 10 ft gain cover/temp HP), or **medbeacon** (allies within 10 ft regain HP **once on deploy** — a burst, not a per-round fountain; throttled by the `[once per minute]` cooldown). *The medbeacon is the optional party heal — never mandatory (Phase 2 floor covers a Technician-less party).* Vitality-power and medbeacon healing are **not** subject to stim tolerance (which is stim-only, [Phase 6 §3](2026-06-13-phase6-equipment-and-economy.md)); they're bounded instead by Attunement/action and deploy-cooldown costs.

**Levels 1–5:**
| L | Technician grants |
|---|---|
| 1 | Key INT; trained tech & class DC; **Command Drone** (the Drone); **Deploy Device** (one gadget type); **subclass** + L1 feature |
| 2 | Class feat (new gadget or drone upgrade) |
| 3 | **Subclass feature**; Computers/Repair → expert; (chassis) |
| 4 | Class feat |
| 5 | Drone upgrade (extra action when commanded / better stats); 2nd gadget type; (chassis) |

---

## 7. Condition List (closes the deferred item)

Standardized status effects (carry traits; impose mostly **Status** modifiers). Core slice set:

| Condition | Effect |
|---|---|
| **Off-Guard** | −2 circumstance penalty to AC |
| **Suppressed** | Off-Guard, −2 circumstance to attacks; provokes the suppressor's Reactive Shot on move/ranged Strike (until suppressor's next turn) |
| **Frightened X** | −X status penalty to checks & DCs; reduce X by 1 at end of each turn |
| **Prone** | Off-Guard; −2 to attacks; Stand costs 1 action |
| **Persistent (energy/kinetic/etc.) damage** | take the listed damage at end of turn until ended |
| **Off-Balance** *(social)* | the next appeal against you gains a circumstance bonus |
| **Guarded** *(social)* | appeals against you take a circumstance penalty |
| **Rattled** *(social)* | −1 status penalty to social checks/Composure (social Frightened-lite) |

The full condition catalogue expands in Phase 7 / rules-writing.

---

## 8. Validation Pass (class-design checklist)

- **Distinct verbs:** Suppress (deny) / Exploit (burst-on-setup) / Force Flow + Deflect (hybrid + active defense) / Deploy (field assets) — no two share a typical turn. ✔
- **Role budgets:** each class sums ~11; each has one 3 and ≥two ≤1s (§3–6). ✔
- **Identity online at L1; no dead levels** (chassis guarantees a feat/feature every level; each class's verb is L1). ✔
- **MAD check:** every class keys off one attribute (DEX/WIS/DEX/INT). ✔
- **Niche test (T5):** each signature beats the default in a named niche and loses outside it (§3–6). ✔
- **Same-class divergence (Pillar 4):** subclass at L1 + different feat/known-power picks make two same-class builds diverge by L3 (e.g., Sharpshooter vs Vanguard Soldier; Sentinel vs Warrior Guardian). ✔
- **Contribution parity (T5):** across a 1-fight scene, the four contribute via *different* axes (Soldier denies, Scoundrel bursts set-ups, Guardian controls+tanks fire, Technician multiplies) — balanced in contribution, differentiated in method. (Quantitative DPR/eHP validation → Gate A.)
- **No-mandatory-healer holds:** Vitality powers / medbeacon are *optional*; the Phase 2 recovery floor covers parties lacking them. ✔

---

## 9. Exit-Gate Checklist (per roadmap)

- [x] Four slice classes drafted to ~level 5 (§3–6).
- [x] Same-class divergence check (two builds of one class play differently by level 3) (§8).
- [x] Contribution-parity argument across the four (§8; quantitative pass deferred to Gate A).
- [x] T4 resolved: Force users are verb-having, cooldown/pool-gated classes — no slots (§2).
- [x] Force exemplars specced (Telekinetic Nudge, Center, Deflecting Stance/Deflect) (§2, §4).
- [x] Condition list closed (§7).

---

## 10. Carried Forward (open items)

- **Full level 6–20 tables, complete class-feat lists, full known-power lists per discipline, subclass features at 7/11/15/19, capstones** → completed before/at the slice playtest and expanded in Phase 8.
- **Quantitative balance** (DPR, eHP, Attunement sizing, Drone stats, precision dice, Deflect values, Suppression numbers) → **Gate A** (`ttrpg-balance-analysis`).
- **Full Dark-Side corruption subsystem; additional Force classes (Consular-type controller; area & control role gaps); additional martial/tech classes** → Phase 8.
- **Species & background content** (boosts, feats, PC Levers for Phase 4) → later content phase.
- **Weapon/gear specifics** (lightsaber `[finesse]`/`[deadly]` values, blaster ranges, stimpacks, armor Dex-caps) → Phase 6.
- **Commanded Actor rules now defined** ([connective-tissue §F](2026-06-13-connective-tissue-and-review-remediation.md)); remaining: deployable/gadget detail, social-verb content for the Face → refined alongside Phase 6–7.

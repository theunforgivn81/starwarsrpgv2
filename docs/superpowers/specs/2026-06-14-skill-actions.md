# Skill Actions

**Status:** Approved
**Date:** 2026-06-14
**Type:** Content spec — defines what each skill *does* (the substrate for rank-gated effects).
**Upstream:** [Phase 2 — Character Framework](2026-06-13-phase2-character-framework.md) (the 14 skills), [Phase 4](2026-06-13-phase4-social-intrigue-engine.md) (the social engine these CHA actions feed), [connective-tissue](2026-06-13-connective-tissue-and-review-remediation.md) (detection S1, dying S2, Commanded Actors §F).
**Source:** adapted from the **Starfinder 2E** skill-action set (Paizo **ORC**; Philosophy §0), paraphrased and bound to our rules. Magic skills (Arcana/Occultism/Religion) and their actions (Identify Magic, Learn a Spell, etc.) are **cut**; Performance is cut.

> Four-degree outcomes are given inline for the **tactical (encounter)** actions — these are the anchors rank-gated effects hook. Exploration/downtime actions are named with one-line effects; their full four-degree text follows the ORC standard and is finalized in rules-writing. **Downtime** actions (Craft, Earn Income, Subsist, Treat Disease, Create Forgery) are *named here, full procedures → Phase 8.*

---

## 1. How Skill Actions Work

- **Modes:** `[encounter]` (used in initiative; usually 1–3 actions), `[exploration]` (untimed, between scenes), `[downtime]` (long-form; Phase 8). A skill spans modes — e.g. Athletics does Climb in exploration and Shove in combat.
- **Gating:** **untrained** actions are usable by anyone; **(T) trained** actions require ≥ trained in that skill (Phase 1). Some uses demand higher ranks by *difficulty*, and **rank-gated effects** (the next spec) add capability at Expert/Master/Legendary.
- **Resolution:** every action uses the four-degree engine vs a DC (the [DC ladder](2026-06-13-gateA-balance-validation.md) for static tasks, or a defense DC for contested ones). **Recall Knowledge** uses the relevant knowledge skill per the [Phase 2 RK mapping](2026-06-13-phase2-character-framework.md).
- **Dual-mode CHA:** Diplomacy/Deception/Intimidation have the exploration actions below **and** power the Phase 4 social-encounter appeals (a social encounter is where these skills' "combat mode" lives).

**Basic actions (no skill; everyone):** Aid, Seek, Sense Motive, Point Out, Escape, Take Cover, Ready, Step, Stride, Crawl, Drop Prone, Stand, Interact, Release, Leap, Delay, Grab an Edge.

---

## 2. Physical Skills

### Athletics (STR)
| Action | Cost | Gate | Effect |
|---|---|---|---|
| Climb | 1a `[encounter]`/expl | — | move up/across a surface (vs DC). |
| Swim | 1a | — | move through liquid. |
| High Jump / Long Jump | 2a | — | leap vertically / horizontally. |
| **Grapple** | 1a `[attack]` | — | vs target Fort DC. **Crit success:** Restrained. **Success:** Grabbed. **Fail:** none. **Crit fail:** you fall prone / target escapes free. |
| **Shove** | 1a `[attack]` | — | vs Fort DC; push 5 ft (10 on crit) — forced movement (§G stop-at-edge). |
| **Trip** | 1a `[attack]` | — | vs Fort DC; **Success:** target Prone (Off-Guard). **Crit fail:** you fall Prone. |
| **Reposition** | 1a `[attack]` | — | vs Fort DC; move target within reach (§G). |
| Force Open | 1a | — | break a door/restraint. |
| **Disarm** | 1a `[attack]` | **T** | vs Fort DC; **Crit:** knock weapon away. **Success:** −2 circ. to target's attacks w/ it until its turn. |

### Acrobatics (DEX)
| Action | Cost | Gate | Effect |
|---|---|---|---|
| **Balance** | 1a | — | cross narrow/unstable ground; fail = stuck/Off-Guard, crit fail = fall/prone. |
| **Tumble Through** | 1a | — | move through an enemy's space (vs Reflex DC); success = treat as difficult terrain, no provoke. |
| Squeeze | `[exploration]` | **T** | move through a tight gap. |
| Maneuver in Flight | 1a | **T** | control flight (jetpack/repulsor) on hard maneuvers. |

### Stealth (DEX) — *detection states per [S1](2026-06-13-connective-tissue-and-review-remediation.md)*
| Action | Cost | Gate | Effect |
|---|---|---|---|
| **Hide** | 1a | — | with cover/concealment, become **Hidden** from foes (vs their Perception DC). |
| **Sneak** | 1a | — | move while staying **Undetected**. |
| Conceal an Object | 1a | — | hide an item on your person (vs Perception DC). |

*(An Undetected/Hidden attacker's target is Off-Guard; attacking from concealment doesn't provoke a Reactive Shot — S1/§11.)*

### Thievery (DEX) — *physical/mechanical*
| Action | Cost | Gate | Effect |
|---|---|---|---|
| **Palm an Object** | 1a | — | lift a small unattended/worn item unseen. |
| **Steal** | 1a | — | take an object from a creature (vs Perception DC). |
| Pick a Lock | 2a | **T** | open a **mechanical** lock (degrees = progress/jam). |
| Disable a Device | 2a | **T** | disarm a **mechanical** trap (degrees = disarm/trigger). |

### Piloting (DEX) — *vehicle system rules light; full → Phase 8*
| Action | Cost | Gate | Effect |
|---|---|---|---|
| Recall Knowledge (vehicles) | 1a | — | identify a vehicle/its systems. |
| Drive | 1–3a | **T** | move a vehicle. |
| Stunt | 1a | **T** | risky maneuver (evade, barrel-roll). |
| Stop / Take Control | 1a | **T** | halt / seize the controls. |
| Run Over | 3a | **T** | vehicle-impact attack. |
| Navigate / Plot Course | `[exploration]` | **T** | plan an overland route / a starship jump. |

---

## 3. Tech & Knowledge Skills (INT)

### Computers (INT) — *slicing/electronics*
| Action | Cost | Gate | Effect |
|---|---|---|---|
| Access HoloNet | `[exploration]` | — | look up data on a network (the digital "Gather Information"). |
| Operate Device | `[exploration]` | — | use standard tech/UI/controls. |
| Recall Knowledge (data/AI) | 1a | — | know systems, programs, droids' software. |
| **Slice** | `[exploration]`/`[encounter]` | **T** | breach a secured system (the digital "Pick a Lock"). |
| Disable a Device | 2a | **T** | neutralize an **electronic** system/trap/alarm. |
| Decipher Writing | `[exploration]` | **T** | decode encrypted data. |

### Repair (INT) — *fabrication & ordnance (SF2E "Crafting")*
| Action | Cost | Gate | Effect |
|---|---|---|---|
| Repair | `[exploration]` | — | restore HP to an item/droid/vehicle. |
| Recall Knowledge (machinery) | 1a | — | know machines, droids, vehicles. |
| Craft | `[downtime]` | **T** | fabricate/modify gear *(→ Phase 8)*. |
| **Demolitions** *(setting-native)* | varies | **T** | set or disarm explosives (disarm uses the Disable a Device frame). |
| Earn Income (technician work) | `[downtime]` | **T** | *(→ Phase 8)*. |

### Society (INT)
| Action | Cost | Gate | Effect |
|---|---|---|---|
| Recall Knowledge (people/orgs/history) | 1a | — | civilization, law, factions, planets. |
| Subsist (urban) | `[downtime]` | — | get by in a settlement *(→ Phase 8)*. |
| Create Forgery | `[downtime]` | **T** | forge documents/credentials *(→ Phase 8)*. |
| Decipher Writing | `[exploration]` | **T** | decode languages/historical scripts. |

### Lore (family, INT)
| Action | Cost | Gate | Effect |
|---|---|---|---|
| Recall Knowledge (narrow topic) | 1a | — | deep, easy answers within the specialization. |
| Earn Income (expertise) | `[downtime]` | **T** | *(→ Phase 8)*. |

---

## 4. Wisdom Skills

### Survival (WIS)
| Action | Cost | Gate | Effect |
|---|---|---|---|
| Sense Direction | `[exploration]` | — | orient / avoid getting lost. |
| Subsist (wild) | `[downtime]` | — | find food/shelter *(→ Phase 8)*. |
| Track | `[exploration]` | **T** | follow a trail. |
| Cover Tracks | `[exploration]` | **T** | hide your passage. |

### Nature (WIS)
| Action | Cost | Gate | Effect |
|---|---|---|---|
| Recall Knowledge (beasts/flora/ecology) | 1a | — | the living world. |
| **Command an Animal** | 1a | — | direct a beast (a `[companion]` beast is a **Commanded Actor**, §F). |
| Sense Environment | `[exploration]` | — | read terrain/weather hazards. |

### Medicine (WIS) — *recovery hub; dying per [S2](2026-06-13-connective-tissue-and-review-remediation.md)*
| Action | Cost | Gate | Effect |
|---|---|---|---|
| **Administer First Aid** | 2a | — | **stabilize** a dying creature (set Dying to 0) *or* stop persistent bleed (vs DC). |
| Recall Knowledge (medical) | 1a | — | diagnose injuries/afflictions. |
| **Treat Wounds** | `[exploration]` | **T** | heal HP out of combat (degrees: crit = more, **crit fail = minor damage**) — the class-agnostic recovery accelerant ([Phase 2 §5](2026-06-13-phase2-character-framework.md)). |
| Treat Poison | 1a | **T** | grant a save vs a poison. |
| Treat Disease | `[downtime]` | **T** | *(→ Phase 8)*. |

---

## 5. Charisma Skills (dual-mode: exploration actions **+** Phase 4 appeals)

### Deception (CHA)
| Action | Cost | Gate | Effect |
|---|---|---|---|
| **Create a Diversion** | 1a `[encounter]` | — | feint attention (vs Perception DC) → become **Hidden**. |
| Lie | `[exploration]` | — | deceive in conversation (vs Perception DC). |
| Impersonate | `[exploration]` | — | pose as someone (disguise). |
| **Feint** | 1a `[encounter]` `[attack]` | **T** | vs Perception DC; **Success:** target **Off-Guard** to your next melee Strike (Crit: until end of your turn). *(Enables the Scoundrel's Exploit; the social-engine "Find an Opening.")* |

### Diplomacy (CHA)
| Action | Cost | Gate | Effect |
|---|---|---|---|
| **Request** | 1a `[encounter]` | — | ask for a specific concession (vs Will DC). |
| Make an Impression | `[exploration]` | — | shift an NPC's initial attitude. |
| Gather Information | `[exploration]` | — | learn things by asking around. |
| *(encounter mode)* | — | — | drives the Phase 4 **appeals** (Make a Case / Press). |

### Intimidation (CHA)
| Action | Cost | Gate | Effect |
|---|---|---|---|
| **Demoralize** | 1a `[encounter]` `[emotion][fear]` | — | vs Will DC; **Success:** target **Frightened 1** (Crit: Frightened 2). *(Droids/mindless immune — `[emotion]`, S7.)* |
| Coerce | `[exploration]` | — | force compliance through threats. |
| *(encounter mode)* | — | — | drives the Phase 4 **appeals**. |

### Perception (WIS proficiency, not a skill)
Seek (find hidden/undetected), Sense Motive (read intentions — the social-engine **Read the Room**), Point Out, Initiative.

---

## 6. Integration Notes

- **Combat conditions:** Trip→Prone, Demoralize→Frightened, Feint/Create a Diversion→Off-Guard/Hidden, Grapple→Grabbed/Restrained — all from the [Phase 5 §7 condition list](2026-06-13-phase5-class-design-and-force.md).
- **Recovery:** Administer First Aid + Treat Wounds are the Medicine half of the no-mandatory-healer model ([Phase 2 §5](2026-06-13-phase2-character-framework.md)); stim tolerance does **not** apply to Treat Wounds (out-of-combat).
- **Detection:** Hide/Sneak/Seek run the S1 states; they gate the Reactive-Shot stealth counter (§11).
- **Companions:** Command an Animal directs a `[companion]` beast under the §F Commanded-Actor rule.
- **Social engine:** the CHA skills + Perception (Sense Motive) are the skills behind the Phase 4 appeals/Read-the-Room; this spec covers their *exploration*-mode uses.

---

## 7. Rank-Effect Anchors (sets up the next spec)

Rank-gated effects (the Gate A T1 directive) will hook these surfaces — *capability, not bigger numbers*:
- **New degree outcomes** an Expert+ unlocks (e.g., a Master slicer's *Slice* crit also plants a backdoor).
- **New action options / modes** (e.g., Legendary Stealth lets you Sneak at full Speed; Expert Medicine reduces Treat Wounds time).
- **Riders on success** (e.g., Master Intimidation's Demoralize also slows).
- **Removing a limit** (e.g., Expert removes the "can't retry" or range/cover requirement of an action).

Each of the four classes' **proficiency signatures** (Soldier=weapons, Scoundrel=skills, Guardian=Force, Technician=Computers/Repair) reaches Legendary and is the primary home for these effects.

---

## 8. Carried Forward

- **Full four-degree text** for exploration/downtime actions → rules-writing.
- **Downtime procedures** (Craft, Earn Income, Subsist, Treat Disease, Create Forgery, Repair-as-downtime) → Phase 8.
- **Full vehicle/Piloting system** (Drive/Stunt/Run Over in vehicle combat) → Phase 8.
- **Rank-gated effects** per action/signature → next spec.

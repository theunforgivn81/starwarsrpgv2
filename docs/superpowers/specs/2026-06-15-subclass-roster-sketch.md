# Subclass Roster (Phase 8 — sketch)

**Status:** Sketch — subclass identities + verb-forks; full features (on the 3/7/11/15/19 cadence) come with per-class detailing.
**Date:** 2026-06-15
**Type:** Content design. Informed by the prior-project **Subclass** table (read for patterns, not ported) and the design framing: Guardian = lightsaber Forms, Consular = Force applications (schools), Tech Specialist ~5, and Soldier/Officer/Scoundrel adapt SF2E ports. Each subclass **modulates the class verb, never replaces it** (Phase 5).
**Upstream:** [Class Roster](2026-06-15-class-roster-sketch.md), [Phase 5 chassis](2026-06-13-phase5-class-design-and-force.md), [Force subsystem](2026-06-13-phase5-class-design-and-force.md).

> Branch at **level 1**; subclass features on the **3 / 7 / 11 / 15 / 19** cadence. Counts vary by class: the Force classes and Tech Specialist carry more (their subclass *is* their core customization axis); the SF2E-derived classes run ~3.

---

## 1. Guardian — Lightsaber Forms *(STR · Blade-Flow + Intercede)*

> **Built in full** — [class-guardian §5](2026-06-18-class-guardian.md) (subclasses) + [lightsaber-forms](2026-06-18-lightsaber-forms.md) (the shared stance system). Verb refined: **Deflect** is a mastered shared-toolkit power; **Intercede** is the exclusive verb.

**Model:** Forms are a **feat-chain stance system** — *any* Guardian learns Forms via class feats and **switches between known Forms mid-combat** (a Form is a stance). A **subclass grants its signature Form's base stance for free + synergy abilities**, making you that Form's *specialist* while still able to flow into others. So subclasses = Form specializations.

**Concrete structure** (confirmed from the prior `ClassFeat` table; reference for the detailing pass): each Form is a **`[Form][Stance]` feat** — **1 action** to enter, **requires a lightsaber**, a while-in-stance effect **+ a "Guardian Mastery" clause** that upgrades it for Guardians. *Example —* **Soresu Stance** (Form III): *+2 circumstance AC vs ranged Strikes, Speed −10 ft; Guardian Mastery: the AC bonus also applies to melee.* Each base stance anchors a **chain of 3 prerequisite-gated follow-up feats**. All **seven** Forms exist (Shii-Cho/Makashi/Soresu/Ataru/Shien-Djem So/Niman/Juyo-Vaapad). **The "Guardian Mastery" clause makes Forms portable** — an archetype (e.g. Force Adept) can grant a base stance, while the Guardian gets the mastery upgrade — so Forms are the shared Force-melee vocabulary, mastered by Guardians.

> **The prior Form chains are *thematic* reference, not a port.** We keep each Form's *fiction and tactical role* (Soresu = defensive eye-of-the-storm, Ataru = acrobatic aggression, Makashi = the duelist, Djem So = counterattack, Niman = blade-and-power balance, etc.); the actual feats are (re)designed under our bounded system (our Deflect, Attunement, three-action economy). Not all prior chains will map — the value is the thematic scaffolding.

| Subclass (Form) | Forks the verb toward… |
|---|---|
| **Shii-Cho** (Way of the Sarlacc) | **multi-target / crowd control** — sweep a crowd, hold the line, area soft-taunt |
| **Makashi** (Way of the Ysalamiri) | **dueling/precision** — 1-v-1 saber mastery, disarms, single-target lock (Bind the Blade) |
| **Soresu** (Way of the Mynock) | **defense/deflection** — the Deflect master; weather fire, outlast |
| **Ataru** (Way of the Hawk-Bat) | **aggressive mobility** — Force-leaps, hit-and-spin, burst offense |
| **Djem So / Shien** (Way of the Krayt Dragon) | **counterattack** — deflect-and-riposte; punish attackers (synergizes with reactions) |
| **Niman** (Way of the Rancor) | **Force-blade balance** — best telekinesis↔saber interplay (Attunement + strikes) |
| **Juyo / Vaapad** (Way of the Vornskr) `[dark]` | **reckless aggression** — glass-cannon; max single-target threat, the corruption hook |

*(All **seven** Forms are Guardian subclasses — one each — designed in full in [class-guardian §5](2026-06-18-class-guardian.md). The base Form stances remain learnable by any Guardian via feats regardless of subclass.)*

## 2. Consular — Mandates *(CHA · Manifest)* — **6, built** *(one per Force school)*

> **Built in full** — [class-consular §5](2026-06-19-class-consular.md). One Mandate per [tradition-split school](2026-06-15-shared-force-toolkit.md).

| Mandate | School | Emphasis |
|---|---|---|
| **Telekinesis** | Alter | kinetic control — throw/crush/hold/zones |
| **Visions** | Sense | foresight — precognitive buffs, detection, init/defense |
| **Serenity** | Control | energy defense, barriers, Tutaminis, cloak |
| **Vitality** | Body | the Force healer (merges the prior Life + Ascendant) |
| **Dominance** | Mind | the mentalist — fear/influence/domination; the social engine |
| **Destruction** | Offense | raw Force violence — lightning, blasts (`[dark]`-adjacent) |

## 3. Sentinel — Reactive Sub-Identities *(WIS · Premonition)* — **fresh design**

The prior "Path of the…" subclasses are orphaned (old Sentinel was a Force-rogue). New ones steer the **reactive Premonition** chassis (the base verb is open by design — the subclass is the steering):

| Subclass | Reactive fork |
|---|---|
| **Warden** | **protector** — reactions intercept/redirect attacks meant for *allies*; shield, bodyguard |
| **Shadow** | **ambusher** — stealth + reactive counters; punish foes acting near you, then vanish |
| **Justicar** | **punisher** — precognitive riposte; when struck or when a foe acts, retaliate hard |
| **Investigator** | **detective/controller** — Recall Knowledge + Class-DC Trip/Disarm/Shove; subdue (adapted from prior *Watchman*) |
| **Corsair** | **ranged dirty-fighter** — blaster Counters, feints, ricochet trick-shots (adapted from prior *Corsair*; the reactive answer to the Scoundrel's proactive gunplay) |

*(Five designed in full — see [class-sentinel §5](2026-06-15-class-sentinel.md).)*

## 4. Tech Specialist — Tech Specialties *(INT · Deploy)* — ~5

> **Built in full** — [class-tech-specialist §5](2026-06-20-class-tech-specialist.md). Five disciplines adapt the prior Tech disciplines; each reshapes the **Overclock** risk its own way.

| Discipline | Role | Deploy fork |
|---|---|---|
| **Bio-Tech** | Support | medic — Mods as field medicine; Overclock a heal to save the dying |
| **Scrapper** | Utility | jury-rig versatilist — re-tune Mods; *ignore* an Overclock failure |
| **Armstech** | Offense | combat engineer — weapons/armor; Overclock a gun to Area/Auto-Fire |
| **Droidwright** | Companion | a droid partner (§F Commanded Actor); failed Overclock buffs the droid |
| **Slicer** | Control | electronic warfare — hack at range; Overclock → target off-guard |

## 5. Soldier — Fighting Styles *(CON · Suppress)* — **5, built** *(all ORC styles adapted)*

> **Built in full** — [class-soldier §5](2026-06-18-class-soldier.md). All five ORC Soldier fighting styles adapted.

| Subclass | Suppress fork |
|---|---|
| **Suppressor** (Action Hero) | auto-fire/area suppression; widest zone-denial |
| **Bulwark** (Armor Storm) | maneuver-control + soak; the immovable grappler-frontline |
| **Demolitionist** (Bombard) | explosives & grenades; ally-safe area burst |
| **Enforcer** (Erudite Warrior) | single-target menace; Oppressive Presence soft-taunt |
| **Vanguard** (Close Quarters) | two-handed melee whirlwind; self-centered melee suppression |

## 6. Officer — Leadership Styles *(CHA · Command)* — ~3 *(SF2E Envoy-adapted)*

| Subclass | Command fork |
|---|---|
| **Field Commander** (From the Front) | frontline leader — grant allies attacks/movement, lead the charge |
| **Spymaster** (From the Shadows) | intel/deception — debuff foes, coordinate ambushes, information |
| **Inspiring Hero** (In the Spotlight) | morale/rally — buffs, rally-from-the-brink, the social spotlight |

## 7. Scoundrel — Specializations *(DEX · Exploit)* — **5, built** *(four adapt the prior Operative specs)*

> **Built in full** — [class-scoundrel §5](2026-06-19-class-scoundrel.md).

| Subclass | Exploit fork |
|---|---|
| **Smuggler** *(new)* | fast-talking face — Feint→Exploit, the social engine |
| **Sniper** | long-range marksman — Mark at any range, the patient kill shot |
| **Gunslinger** (← Skirmisher) | close-quarters pistolero — point-blank deadly, trick shots, no-provoke-in-melee |
| **Infiltrator** (← Infiltrator + Ghost) | stealth/spy — Sabotage (slice tech), strike-and-vanish |
| **Striker** | melee brawler — finesse-melee Exploit, Overwhelming Strike (the only Legendary-melee fork) |

---

## 8. Carried Forward

- **Full subclass features** at L1 + 3/7/11/15/19 per subclass → per-class detailing.
- **Lightsaber Form feat-chains** (the stance system; all 7 Forms) → with Guardian/Force-feat content.
- **Consular Mandate of Conflict** (5th) decision.
- **Gate-A re-validation** of class+subclass combos once detailed.
- Subclass **flavor/description** → rules-writing.

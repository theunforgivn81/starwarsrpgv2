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
| **Soresu** (Way of the Mynock) | **defense/deflection** — the Deflect master; weather fire, outlast |
| **Ataru** (Way of the Hawk-Bat) | **aggressive mobility** — Force-leaps, hit-and-spin, burst offense |
| **Djem So / Shien** (Way of the Krayt Dragon) | **counterattack** — deflect-and-riposte; punish attackers (synergizes with reactions) |
| **Makashi** (Way of the Ysalamiri) | **dueling/precision** — 1-v-1 saber mastery, disarms, finesse |
| **Niman** (Way of the Rancor) | **Force-blade balance** — best telekinesis↔saber interplay (Attunement + strikes) |

*(Other Forms — Shii-Cho, Juyo/Vaapad — exist as feat-chain stances available to any Guardian; the five above are the showcased specializations. Juyo carries `[dark]` flavor.)*

## 2. Consular — Force Applications *(CHA · Manifest)*

**Model:** like schools of magic — each subclass emphasizes a **Force discipline** (*what* you Manifest), deepening that application's powers.

| Subclass (Mandate / application) | Discipline emphasis |
|---|---|
| **Mandate of Telekinesis** | kinetic control — throw/crush/hold/zones (battlefield control) |
| **Mandate of Visions** (Sense) | foresight — precognitive buffs, detection, initiative/defense |
| **Mandate of Life** (Vitality) | the Force healer — the optional party heal at its strongest |
| **Mandate of Dominance** (Influence) | the mentalist — mind influence/fear/command; drives the social engine |

*(A 5th, **Mandate of Conflict** (Battle), is possible — a powers-and-blade war-mystic — but overlaps the Guardian; held unless wanted.)*

## 3. Sentinel — Reactive Sub-Identities *(WIS · Premonition)* — **fresh design**

The prior "Path of the…" subclasses are orphaned (old Sentinel was a Force-rogue). New ones steer the **reactive Premonition** chassis (the base verb is open by design — the subclass is the steering):

| Subclass | Reactive fork |
|---|---|
| **Warden** | **protector** — reactions intercept/redirect attacks meant for *allies*; shield, bodyguard |
| **Shadow** | **ambusher** — stealth + reactive counters; punish foes acting near you, then vanish |
| **Justicar** | **punisher** — precognitive riposte; when struck or when a foe acts, retaliate hard |
| **Investigator** | **detective/controller** — Recall Knowledge + WIS-keyed Trip/Disarm/Shove; subdue (adapted from prior *Watchman*) |
| **Corsair** | **ranged dirty-fighter** — blaster Counters, feints, ricochet trick-shots (adapted from prior *Corsair*; the reactive answer to the Scoundrel's proactive gunplay) |

*(Five designed in full — see [class-sentinel §5](2026-06-15-class-sentinel.md).)*

## 4. Tech Specialist — Tech Specialties *(INT · Deploy)* — ~5

| Subclass | Deploy fork |
|---|---|
| **Bio-Tech** | medic — drone/gadgets as field medicine; the party's healer-by-tech |
| **Droidwright** | a strong **combat-droid** companion (the pet specialist) |
| **Slicer** | electronic warfare — hack/disable enemy tech, doors, droids |
| **Infosphere Director** | recon/comms — battlefield awareness, data-buffs, scouting drone |
| **Munitions Expert** | deployable weapons — turrets, mines, grenades (area/control) |

## 5. Soldier — Combat Styles *(CON · Suppress)* — ~3 *(SF2E-adapted)*

| Subclass | Suppress fork |
|---|---|
| **Bulwark** (Armor Storm) | heavy armor + heavy weapons; the immovable frontline |
| **Suppressor** (Action Hero) | auto-fire/area suppression; zone-denial gunner |
| **Demolitionist** (Bombard) | explosives & grenades; area burst |

## 6. Officer — Leadership Styles *(CHA · Command)* — ~3 *(SF2E Envoy-adapted)*

| Subclass | Command fork |
|---|---|
| **Field Commander** (From the Front) | frontline leader — grant allies attacks/movement, lead the charge |
| **Spymaster** (From the Shadows) | intel/deception — debuff foes, coordinate ambushes, information |
| **Inspiring Hero** (In the Spotlight) | morale/rally — buffs, rally-from-the-brink, the social spotlight |

## 7. Scoundrel — Operator Styles *(DEX · Exploit)* — ~3 *(SF2E Operative-adapted)*

| Subclass | Exploit fork |
|---|---|
| **Gunslinger** | ranged precision — the **Mark/Aim** engine (absorbs the prior Operative), trick shots |
| **Infiltrator** (Ghost) | stealth/infiltration — sneak-strike, escape, recon |
| **Face** | con artist — the social-engine specialist (signature appeals), disguise |

---

## 8. Carried Forward

- **Full subclass features** at L1 + 3/7/11/15/19 per subclass → per-class detailing.
- **Lightsaber Form feat-chains** (the stance system; all 7 Forms) → with Guardian/Force-feat content.
- **Consular Mandate of Conflict** (5th) decision.
- **Gate-A re-validation** of class+subclass combos once detailed.
- Subclass **flavor/description** → rules-writing.

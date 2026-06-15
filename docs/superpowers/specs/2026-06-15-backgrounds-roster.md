# Backgrounds Roster (Phase 8 content — mechanics)

**Status:** Approved (36 backgrounds; skill-feat *content* deferred; 4 Force-sensitive backgrounds deferred)
**Date:** 2026-06-15
**Type:** Content — the playable Background list. Adapts the prior-project **Background** table (`reference_data/swf20260426.sql`) into our model. A **direct 1:1** map: each background's Features JSON = `{skill feat, 1 trained Skill + 1 Lore, attribute boost {free 1, choice [X,Y]}}` — exactly the [Creation Slot Contributions](2026-06-15-creation-slot-contributions.md) Background contract (Trained skill + Lore + a Skill Feat + two boosts, one constrained to a choice of two, one free).
**Upstream:** [Creation Slot Contributions §1](2026-06-15-creation-slot-contributions.md), [Phase 2 skills](2026-06-13-phase2-character-framework.md), [Skill Actions](2026-06-14-skill-actions.md).

---

## 1. Adaptation Conventions

- **Map, don't copy-schema.** The source's Features JSON is a *reference for content*, not a data model we adopt. Every field is mapped into our own descriptive terms (the table below); we are not committing to the prior project's JSON shaping and stay free to define our own data representation later.
- **Direct transcription** of the constrained attribute pair, trained Skill, Lore, and Skill Feat.
- **Crafting → Repair** (our INT skill rename, [Phase 2](2026-06-13-phase2-character-framework.md)).
- **Performance → Diplomacy** (we folded Performance into the social skills; the performance-flavored feats become social skill-feats).
- **Skill Feats are deferred hooks** — named here, statted in a later feat batch (with Species Feats), from the source's feat tables.
- **Filtered Lore grants** ("any Settlement/Planet/Craft/Science/Org/Engineering/Creature/Species Lore") rely on **Lore category traits** — a Lore-taxonomy to be defined with Lore content; for now the label stands.
- **Four Force-sensitive backgrounds deferred** (§3): they trained a "The Force" skill we don't have.

## 2. The 36 Backgrounds

Each grants: **two boosts** (one to the listed **choice** pair, one free), **Trained** in the **Skill** + the **Lore**, and the **Skill Feat** (deferred).

| Background | Boost choice | Skill | Lore | Skill Feat (deferred) |
|---|---|---|---|---|
| Courier | DEX/WIS | Survival | any Settlement Lore | Urban Survivalist |
| Bartender | WIS/CHA | Diplomacy | Alcohol Lore | Seasoned |
| Gambler | DEX/CHA | Deception | Gambling Lore | Lie to Me |
| Laborer | STR/CON | Athletics | Labor Lore | Hefty Hauler |
| Bounty Hunter | STR/CON | Survival | Underworld Lore | Experienced Tracker |
| Recruit | STR/CON | Survival | Warfare Lore | Terrain Expertise |
| Spacer | DEX/CON | Piloting | Hyperspace Lore | Express Driver |
| Prisoner | STR/CON | Stealth | Underworld Lore | Experienced Smuggler |
| Droid Technician | DEX/INT | **Repair** | Droidtech Lore | Combat Repair |
| Fringer | DEX/INT | **Repair** | Salvage Lore | Quick Repair |
| Slicer | DEX/INT | Computers | Slicing Lore | Digital Diversion |
| HoloNet Technician | INT/WIS | Computers | HoloNet Lore | Hologram Skeptic |
| Pickpocket | DEX/INT | Thievery | Underworld Lore | Pickpocket |
| Clone Engineer | INT/WIS | Medicine | Genetic-Engineering Lore | Experienced Professional |
| Noble | INT/CHA | Diplomacy | any Planet Lore | Courtly Graces |
| Investigator | INT/WIS | Society | Underworld Lore | Streetwise |
| Smuggler | DEX/WIS | Stealth | Piracy Lore | Experienced Smuggler |
| Artisan | STR/INT | **Repair** | any Craft Lore | Specialty Crafting |
| Scientist | INT/WIS | **Repair** | any Science Lore | Assurance |
| Diplomat | INT/CHA | Diplomacy | any Planet Lore | Group Impression |
| Agent | INT/CHA | Deception | any Org Lore | Without a Trace |
| Space Pirate | STR/DEX | Intimidation | Piracy Lore | Group Coercion |
| Entertainer | DEX/CHA | **Diplomacy** | Media Lore | Virtuosic Performer |
| Podracer | DEX/INT | Piloting | Speeder-Engineering Lore | Incredible Initiative |
| Jizz Wailer | CON/CHA | **Diplomacy** | Jizz Lore | Impressive Performance |
| Salvager | STR/DEX | Athletics | Salvage Lore | Combat Climber |
| Artist | DEX/CHA | **Repair** | Art Lore | Specialty Crafting |
| Doctor | DEX/WIS | Medicine | Anatomy Lore | Battle Medicine |
| Engineer | DEX/INT | **Repair** | any Engineering Lore | Specialty Crafting |
| Farmer | CON/WIS | Nature | any Planet Lore | Train Animal |
| Hermit | INT/WIS | Nature | any Creature/Species Lore | Natural Medicine |
| Outlaw | DEX/CHA | Intimidation | Underworld Lore | Intimidating Shot |
| Saboteur | DEX/WIS | Thievery | any Engineering Lore | Concealing Legerdemain |
| Street Rat | DEX/WIS | Survival | any Settlement Lore | Urban Survivalist |
| Mandalorian | STR/CON | **Repair** | Mandalorian Lore | Quick Repair |
| Mercenary | STR/DEX | Intimidation | Mercenary Lore | Intimidating Glare |

`★ Insight ─────────────────────────────────────`
The background list is a quiet stress-test of the **skill list itself**, and ours passes: every background maps onto one of our 14 skills with none left homeless and none overloaded — the tech trio (Computers/Repair) absorbs the slicer/engineer/droid-tech fantasies, the social trio (Diplomacy/Deception/Intimidation) cleanly re-homed the cut Performance skill (Entertainer/Jizz Wailer → Diplomacy), and the dual-use CHA skills mean "face" backgrounds feed the Phase 4 engine. The only homeless entries were the four that pointed at a *Force skill we deliberately don't have* — which isn't a coverage gap, it's the system correctly refusing to let a background grant Force training. A skill list that cleanly absorbs 36 independently-authored backgrounds is good evidence the Phase 2 list was the right size and shape.
`─────────────────────────────────────────────────`

## 3. Deferred — Force-Sensitive Backgrounds

Four backgrounds trained a "The Force" skill (which our system doesn't have — Force is class/archetype-gated, T4) and granted a `Force Sensitive` feat. **Deferred to a later content pass**, to be designed alongside Force-sensitivity and the **Force Adept archetype** (Phase 3 on-ramp):
- **Dathomir Witch** (STR/WIS, Dathomir Lore), **Warden of the Sky** (DEX/CHA, Spacer Lore), **Temple Youngling** (WIS/CHA, Jedi-Order Lore), **Sith Initiate** (STR/CHA, Sith-Order Lore).

## 4. Carried Forward

- **Skill-Feat content** (Urban Survivalist, Battle Medicine, Specialty Crafting, etc.) → the feat batch (with Species Feats), from the source feat tables.
- **The 4 Force-sensitive backgrounds** → with Force-sensitivity / Force Adept archetype design.
- **Lore category traits** (Settlement, Planet, Craft, Science, Org, Engineering, Creature, Species) → Lore-taxonomy content (powers the "any X Lore" grants).
- **Flavor/description text** → rules-writing (the source has full background descriptions).

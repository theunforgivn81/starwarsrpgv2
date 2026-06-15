# Species Roster (Phase 8 content — mechanics)

**Status:** Approved (base mechanics for all 28; Species-Feat and most Heritage *content* deferred)
**Date:** 2026-06-15
**Type:** Content — the playable Species list. Adapts the prior-project **Ancestry** + **Heritage** tables (`reference_data/swf20260426.sql`, an unbounded ORC/2E build) into our Species model. The data was **net-+2 compatible out of the box** (the unbounded→bounded gap doesn't touch ancestries — boosts/HP/speed/size/senses are tier-agnostic).
**Upstream:** [Creation Slot Contributions](2026-06-15-creation-slot-contributions.md) (Species = net +2; Size/Speed/base HP; senses/movement/languages; rest via Species Feats), [Phase 2](2026-06-13-phase2-character-framework.md), detection states ([S1](2026-06-13-connective-tissue-and-review-remediation.md)).

---

## 1. Adaptation Conventions

- **Map, don't copy-schema.** The source's Features JSON is a *reference for content*, not a data model we adopt — every field is mapped into our own descriptive terms below; we stay free to shape our own data representation later.
- **Attributes:** transcribed directly — each species nets **+2** as fixed boosts + a flaw + one assignable (or two free boosts for Human). The species free/assignable boost can't target an attribute the species already boosts or flaws (so no attribute moves more than ±1 from species). *(Two source data-quirks fixed: Codru-Ji = DEX, CHA; Chubbit = DEX, WIS.)*
- **HP** = the species' flat **base HP** (added once; the "species base" term in the [Phase 2 HP formula](2026-06-13-phase2-character-framework.md)). Range 6–12.
- **Speed** = the listed value as **feet** (the source's "meters" label is a prior-project artifact; 25 = our standard).
- **Senses** use the **Precise / Imprecise / Vague** framework (our detection rules, S1). Baseline = Vision Precise, Hearing Imprecise, Scent Vague; deviations noted.
- **Languages** standardized to **Galactic Basic + native** (a few source rows omitted Basic — fixed).
- **Species-specific powers** (regeneration, precognition, scavenging, etc.) → **Species Feats** (recorded as hooks; statted in a later feat batch from the source's AncestryFeat table).

## 2. The Heritage Mechanic (ORC/2E)

At level 1, after choosing a Species, a character chooses a **Heritage** — a sub-lineage within that species. A Heritage grants a small ability/trait and may tweak senses/movement.
- **For most species:** the **base species** delivers the full **net +2** boosts; heritages are *flavor/ability* choices (their content is deferred with the Species Feats).
- **For the Droid (§4):** the base provides only **+1 free** boost; the chosen **Droid Class heritage** supplies the rest of the **net +2** plus the chassis's signature feature — so the heritage *is* the droid's stat profile.

*(Amends the [Creation Slot Contributions](2026-06-15-creation-slot-contributions.md) sequence: the Species step includes a Heritage sub-choice.)*

---

## 3. The Roster (27 organic species; Droid in §4)

Boosts list the fixed boosts then **(flaw)**; every species also gets **+1 free** (restrictions per §1). Senses are baseline unless noted. Languages = Galactic Basic + the listed native tongue(s).

| Species | Size | Speed | HP | Boosts (flaw) | Senses / Movement | Native language |
|---|---|---|---|---|---|---|
| **Human** | Med | 25 | 8 | **2 free** (no flaw) | baseline | — (+1 extra language) |
| **Twi'lek** | Med | 25 | 8 | DEX, CHA (WIS) | baseline | Ryl |
| **Rodian** | Med | 25 | 8 | DEX, WIS (CHA) | + Scent (vague) | Rodese |
| **Bothan** | Med | 25 | 8 | INT, CHA (CON) | baseline | Bothese |
| **Mon Calamari** | Med | 25 | 8 | INT, WIS (STR) | baseline *(aquatic → feat)* | Mon Calamarian |
| **Zabrak** | Med | 25 | 8 | CON, WIS (CHA) | baseline | Zabraki |
| **Kel Dor** | Med | 25 | 8 | DEX, WIS (CON) | baseline *(atmosphere → feat)* | Kel Dor |
| **Sullustan** | Med | 25 | 8 | DEX, INT (STR) | baseline *(astrogation → feat)* | Sullustese |
| **Duros** | Med | 25 | 8 | DEX, INT (CON) | **Darkvision** | Durese |
| **Cerean** | Med | 25 | 8 | INT, WIS (DEX) | baseline | Cerean |
| **Ithorian** | Med | 25 | 8 | CHA, WIS (DEX) | baseline | Ithorese |
| **Iktotchi** | Med | 25 | 8 | STR, WIS (CHA) | baseline *(precognition → feat)* | Iktotchese |
| **Codru-Ji** | Med | 25 | 8 | DEX, CHA (CON) | baseline | Codruese |
| **Shistavanen** | Med | **30** | 10 | DEX, WIS (CHA) | + keen **Scent (imprecise)** | Shistavanen |
| **Wookiee** | Med | 25 | 10 | CON, STR (CHA) | baseline *(rage/climb → feat)* | Shyriiwook |
| **Tusken Raider** | Med | 25 | 10 | CON, WIS (CHA) | baseline | Tusken |
| **Gamorrean** | Med | 25 | 12 | STR, CON (INT) | baseline | Gamorrean |
| **Mantellian Savrip** | **Large** | 25 | 12 | STR, INT (CHA) | baseline | Savrip |
| **Trandoshan** | Med | 25 | 8 | STR, WIS (DEX) | **Darkvision** *(regen → feat)* | Dosh |
| **Gungan** | Med | 25 | 8 | DEX, CON (CHA) | **Swim 30**, hold breath | Gunganese |
| **Jawa** | **Small** | 20 | 6 | DEX, INT (STR) | baseline *(scavenger feats)* | Jawaese, Jawa Trade |
| **Ortolan** | Small | 20 | 8 | CON, WIS (DEX) | + keen **Scent (imprecise)** | Ortolan |
| **Squib** | Small | 25 | 6 | DEX, CHA (STR) | + keen **Scent (imprecise)** | Squibbian |
| **Ewok** | Small | 20 | 8 | DEX, WIS (STR) | **Low-light/Night Vision** | Ewokese |
| **Ugnaught** | Small | 20 | 10 | CON, INT (CHA) | baseline | Ugnaught |
| **Chubbit** | Small | 25 | 8 | DEX, WIS (CON) | baseline | Chubbini |
| **Anzellan** | **Tiny** | 20 | 6 | DEX, INT (STR) | baseline; **reach 0** | Anzellan |

**Signature Species-Feat hooks (deferred):** Human → *Adaptive Will* (+1 circ Will vs control) + a bonus trained skill; Jawa → *Desert Survivor / Scavenger's Eye / Tinker's Knack*; Trandoshan → *Regeneration*; Cerean → *Assurance* (binary brain); Iktotchi → *Precognition*; Wookiee → *Wookiee Rage / Brachiation*; Mon Calamari & Gungan → aquatic feats; Kel Dor → atmosphere/antitox. *(Statted from the source AncestryFeat table in a later batch.)*

`★ Insight ─────────────────────────────────────`
Notice the roster already self-balances against the bounded math: the "tough" species (Wookiee/Tusken HP 10, Gamorrean/Savrip HP 12) pay with a social/mental flaw, and the small/frail ones (Jawa/Squib/Anzellan HP 6, Speed 20) get DEX/INT for it. Because HP here is a *flat base* (added once, not per level), even a +6 swing (Anzellan 6 → Savrip 12) is a meaningful-but-bounded level-1 difference that washes out as class HP accumulates — exactly the right shape under bounded accuracy: ancestry matters most early, never spirals. The unbounded source didn't have to be re-tuned because *flat* species values are inherently tier-agnostic.
`─────────────────────────────────────────────────`

---

## 4. Droid (Construct — Heritage-defined)

**Base Droid:** Size Medium, Speed 25, HP 8; **+1 free** attribute boost (no flaw); **Low-light Vision**; `[droid]` `[construct]` traits; language Galactic Basic + Binary. **Construct nature** (immunities to `[mental]`/poison/disease, no Constitution-based effects, healed by **Repair** not Medicine, replaces Catch Your Breath, etc.) → **deferred to a focused Construct-rules pass** (flagged; not fully designed here).

A Droid chooses a **Droid Class heritage** = its chassis, supplying the remaining net +1 (→ +2 total) and a signature feature:

| Droid Class | Heritage boosts (flaw) | Signature feature |
|---|---|---|
| **I — Analytical** | WIS | *Analytical Heuristics* (medical: Trained Medicine, use INT for Medicine) |
| **II — Utility** | DEX | *Integrated Utility Sockets* (*Machine Speak* — query simple machines) |
| **III — Protocol** | WIS, CHA (STR) | *Cybot-Galactica Interaction Matrix* (Trained Diplomacy/Society, +2 languages, +1 circ Make an Impression) |
| **IV — Ordnance** | STR, DEX (CHA) | *Integrated Ordnance Systems* (ignore Volley penalty; +damage with Area/Automatic/Kickback) |
| **V — Heavy** | STR | *Heavy-Grade Hydraulic Frame* (reinforced labor/combat chassis) |

Each Class's boosts + the base +1 free = **net +2** (Classes I/II/V = two boosts no flaw; III/IV = three boosts, one flaw).

---

## 5. Carried Forward

- **Species Feats** (per-species feat lists) → from the source **AncestryFeat** table, a later feat batch.
- **Full Heritage content** for the 27 organic species (each gets minor-ability heritages) → later batch.
- **Droid Construct rules** (immunities, Repair-heals-droids interaction with the Phase 2 recovery model, what replaces Catch Your Breath) → focused Construct pass.
- **Size mechanical effects** (reach, space, any size-based bonuses; Tiny reach 0 noted; Large Savrip) → a light Size rule (small framework gap to fill).
- **Flavor/description text** → rules-writing (the source has rich descriptions per species).

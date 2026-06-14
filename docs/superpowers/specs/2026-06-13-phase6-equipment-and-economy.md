# Phase 6 — Equipment & Economy

**Status:** Approved
**Date:** 2026-06-13
**Roadmap phase:** 6 of 9 — see [build roadmap](../plans/2026-06-13-star-wars-rpg-build-roadmap.md)
**Upstream:** [Philosophy](2026-06-13-star-wars-rpg-design-philosophy.md), [Phase 1 (+§5 potency, §11 engagement)](2026-06-13-phase1-core-mechanic-and-traits.md), [Phase 2](2026-06-13-phase2-character-framework.md), [Phase 3](2026-06-13-phase3-progression-chassis.md), [Phase 5](2026-06-13-phase5-class-design-and-force.md)
**Resolves:** the **last build layer before the vertical-slice playtest**; T3 (consumables = the money-gated expendable); Pillar 1 (gear doesn't break bounded math). Provides the lightsaber, blaster baseline, armor Dex-cap, and stimpacks the earlier phases deferred.

> *(Gate A)* = provisional pending balance calibration. Structures fixed; numbers light.

---

## 0. Design Stance — gear is *not* the progression treadmill

Item potency is **optional and not baked into creature math** (Phase 1 §5), so **gear-buying is not the progression system.** Consequences (these defeat the "big-six tax" and "unscheduled math items" traps by construction):

- No mandatory "+X" items; an un-upgraded party stays on-curve.
- **Credits buy *interesting* things** — options, access, customization, ships, contacts, information, and **social Leverage assets** (Phase 4) — not a power tax.
- **Every class has a "wealth identity"** (§7.2) so no class becomes idle party wealth.

---

## 1. Weapons

### 1.1 Baseline & the melee-deadlier rule

Baseline = a **ranged blaster** (§11); all weapons priced as deviations from it.

| Weapon | Damage | Hands | Key traits |
|---|---|---|---|
| **Blaster Pistol** *(baseline)* | 1d6 `[energy]` | 1 | range 60 ft |
| Blaster Rifle | 1d8 `[energy]` | 2 | range 120 ft |
| Heavy Repeater | 1d10 `[energy]` | 2 | `[reload 1]`, `[automatic]` |
| Hold-out Blaster | 1d4 `[energy]` | 1 | `[concealable]`, short range |
| Vibroblade | 1d6 `[kinetic]` | 1 | `[agile]` `[finesse]`, melee |
| Vibro-axe | 1d8 `[kinetic]` | 2 | `[deadly d8]`, melee |
| **Lightsaber** | 1d8 `[energy]` | 1 (`[versatile]` 2) | `[finesse]` `[deadly d8]`, melee, `[uncommon]`/`[rare]`, `[Force]`-gated |

**Melee-deadlier lever (confirmed):** **melee Strikes add the attribute modifier to damage; ranged Strikes do not.** Ranged classes keep pace via **weapon specialization** — a flat damage bonus that grows with weapon proficiency rank *(Gate A values)* — which also gives the "Legendary weapons" proficiency-signature real teeth. Melee's higher per-hit damage is paid for by the §11 Reactive-Shot risk.

### 1.2 Weapon trait glossary (registers into the Phase 1 taxonomy)

| Trait | Effect |
|---|---|
| `[agile]` | Multiple Attack Penalty −3/−6 (vs −4/−8) |
| `[finesse]` | use DEX instead of STR for attack (and for melee damage) |
| `[deadly dX]` | on a critical hit, add an extra `dX` (more dice at higher weapon proficiency) |
| `[reload N]` | requires N actions to reload after firing (a negative property that buys damage) |
| `[two-handed]` | requires two hands |
| `[versatile]` | usable one- or two-handed (damage die changes) |
| `[thrown R]` | can be thrown to range R; thrown melee weapons add the attribute to damage |
| `[concealable]` | circumstance bonus to conceal the weapon |
| `[automatic]` | can target a small area / multiple adjacent creatures (the ranged AoE option) |
| range increment | ranged weapons take a cumulative penalty per increment beyond the first |

### 1.3 Mods (the upgrade path)

Weapons improve via **transferable modifications** (scopes, barrels, power cells, **lightsaber crystals**) — keep your named weapon, upgrade the mods. Mods carry the **damage-dice scaling** and **optional potency**. Mod installation uses **Repair**. The mod schedule sits on the Phase 3 convergence map (optional, since not assumed power).

### 1.4 Matrix audit (anti-dominance — exit-gate check)

No weapon is strictly superior at its access tier; every wanted niche exists:
- **Default ranged:** Blaster Pistol (one-handed flexibility) vs Rifle (more damage, costs a hand) — a real trade.
- **Concealment build:** Hold-out (less damage for `[concealable]`).
- **DEX-melee build:** Vibroblade (`[agile]`/`[finesse]`).
- **Burst-melee build:** Vibro-axe (`[deadly]`, two-handed).
- **Force duelist:** Lightsaber — better than common melee, but `[rare]`/`[Force]`-gated, so it doesn't dominate the *common* market.
- **Suppression build:** Heavy Repeater (`[automatic]`, paid for with `[reload]`).

---

## 2. Armor

### 2.1 AC formula (amends Phase 2 §4 — adds the armor-base term)

> **AC = 10 + proficiency (L+R) + min(DEX, armor Dex-cap) + armor base + item potency + circumstance**

The **armor base** is a fixed, **non-scaling** category constant (like the `10`), so bounded accuracy holds — potency remains the only growing item bonus.

### 2.2 Categories

| Armor | Base | Dex-cap | Penalty |
|---|---|---|---|
| Unarmored | +0 | +5 | needs a class *unarmored-defense* feature to be on-curve |
| Light (flight suit) | +2 | +4 | none |
| Medium (combat armor) | +3 | +2 | minor speed / check penalty |
| Heavy (battle/powered armor) | +4 | +1 | −5 speed, Stealth/Acrobatics penalty, STR requirement |

- **Crossover ≈ DEX +3/+4:** low-DEX bruisers want heavy (consistent AC, DEX free to dump); high-DEX skirmishers want light (rewards investment, no penalties). Both sides populated.
- **Penalties bite real activities** (Stealth scenes, positioning) — not fake prices.
- **Unarmored on-curve:** robed Force users get an **unarmored-defense** class feature placing them on the light-armor curve (iconic Jedi-in-robes). Any unarmored class must have such a feature.

---

## 3. Consumables (the only money-gated expendable — T3)

Designed against hoarding (cheap, plentiful, renewable); **class/encounter balance assumes zero use** (consumables are a lifeline, not assumed DPR), consistent with the no-mandatory-healer floor.

| Consumable | Use |
|---|---|
| **Stimpack** | 1 action `[manipulate]`; heal a **clutch-relevant** amount on first use (enough to keep a downed-risk ally fighting). **Stim tolerance:** each additional stim on the same creature *within a scene* heals less — anti-chain, not anti-use. *(Potency must stay meaningful given the limit — Gate A directive.)* |
| **Medpac** | powers out-of-combat **Treat Wounds** (Medicine); **refillable in downtime** (renewable, not hoarded) |
| **Grenades** `[thrown]` | the **area expendable** covering the slice's AoE gap: frag `[kinetic]`, ion (vs droids/shields), stun, smoke (concealment) |
| **Adrenal / spike / demolition kits** | minor combat buffs, slicing aids, breaching |

**Design directive (clarification):** because in-combat stim use is *limited* by tolerance, the **first stim must be potent enough to be a real tactical lifeline** — stims keep you *in* the fight; full recovery remains Catch-Your-Breath's job between fights. Balance still assumes zero (the floor covers stim-less parties), but survivability math treats stims as an available clutch option.

---

## 4. Rarity & Access

`common → uncommon → rare → unique` (Phase 1 rarity traits). **Common = freely bought; uncommon+ = GM/faction/region-gated.** Because potency is the only numeric scaling (and optional), **rarity ladders *special properties and availability*, never a +X treadmill** — a rare item is *distinctive*, not merely *bigger*. Lightsabers are `[uncommon]`/`[rare]` and `[Force]`-gated. An **attunement-style cap** on simultaneously-active powerful items is available as the anti-stacking tool if needed *(Gate A)*.

---

## 5–7. Economy & Wealth

### 5. Wealth structure

- **Price bands:** *trivial* (consumables, mundane kit — bought without thought) · *decision* (a good mod, a gadget, a vehicle upgrade — save a few sessions) · *aspirational* (starship, base, custom lightsaber, holocron).
- **Sell at ~50%** for standard goods (restricted/illicit goods fence for less). Currency = **credits**.
- **Wealth-by-level** is a light published curve governing consumable budgets and aspirational goals — *not* a power treadmill *(numbers → Gate A)*.

### 6. The money sink (essential)

**Primary sink: ship & lifestyle upkeep and debt** — fuel, repairs, docking fees, loan payments. The iconic Star Wars drain; a bottomless sink *and* an adventure generator (keeping the freighter flying). Secondary sinks: bribes/access, consumable refills, mod/crafting costs.

### 7. What each class buys

**7.1 General:** credits buy options, access, customization, and **social Leverage assets** (bribe funds, gifts, blackmail — feeding the Phase 4 engine), plus shared aspirational goods (starship, base, speeder).

**7.2 Per-class wealth identity** (so no class is idle party wealth):

| Class | Wants to buy |
|---|---|
| **Soldier** | weapons & weapon mods (scopes, barrels, ammo types), heavy armor, grenades/munitions, a deployable arsenal |
| **Scoundrel** | gadgets, disguises & forged credentials, slicing kits, a personal speeder/ship share, **contacts & information**, social Leverage assets |
| **Guardian** *(Force)* | **lightsaber crystals & hilt mods**, **holocrons & Force artifacts** (teach new powers / unlock disciplines — *options & access, never +X*), meditation foci, modded robes |
| **Technician** | drone upgrades, gadget components, a fabrication workshop/tools, droid chassis & parts, crafting materials, deployable devices |

**Crafting/modding** (via Repair) beats shopping at *customization and access* (install mods, fabricate on remote worlds) — never as a primary power source (power isn't gear-gated).

---

## 8. Exit-Gate Checklist (per roadmap)

- [x] Baseline weapon defined (blaster pistol); all others priced as deviations (§1).
- [x] Matrix audit: no strict dominance; wanted niches covered (§1.4).
- [x] Armor crossover computed (~DEX +3/+4); both sides populated; unarmored on-curve via class feature (§2).
- [x] Penalties bite activities the game exercises (Stealth, positioning) (§2.2).
- [x] Rarity ladder with written delta (access/effects, not power); attunement-cap available (§4).
- [x] Big-six audit: mandatory math items **decoupled** (potency optional) — economy freed for interesting items (§0).
- [x] Consumables designed against hoarding; encounters assume zero; stim potency directive recorded (§3).
- [x] Upgrade (mods) schedule on the convergence map (§1.3).
- [x] Wealth-by-level + three price bands + a money sink (ship upkeep) (§5–6).
- [x] **A basic-gear set the four slice classes can use** (§1–3) — *slice is content-complete.*

---

## 9. Carried Forward (open items)

- **All numbers** (weapon specialization values, `[deadly]` dice, armor-base/Dex-cap tuning, stim potency & tolerance, grenade damage, wealth-by-level, mod prices) → **Gate A** (`ttrpg-balance-analysis`).
- **Full weapon/armor/mod/consumable catalogues, vehicle & starship stats, holocron/artifact content, attunement-cap decision** → Phase 8 expansion.
- **Crafting full rules, lifestyle/upkeep tables** → Phase 8.

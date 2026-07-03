# Class — Sentinel *(content-complete, pending Gate-A)*

**Status:** **Content-complete pending Gate-A.** Chassis locked; Premonition core abilities (§4), five subclasses (§5), and the class-feat menu (§6) all designed.
**Date:** 2026-06-15
**Type:** Class detail. First class detailed from the [Class Roster](2026-06-15-class-roster-sketch.md) / [Subclass sketch](2026-06-15-subclass-roster-sketch.md).
**Upstream:** [Phase 5 chassis](2026-06-13-phase5-class-design-and-force.md), [Phase 3 progression](2026-06-13-phase3-progression-chassis.md), [Creation Slot Contributions](2026-06-15-creation-slot-contributions.md), [Force subsystem](2026-06-13-phase5-class-design-and-force.md).

---

## 1. Identity

*A watchful Force-adept who sees the blow before it lands.* **Key attribute: Wisdom. HP 8.** The Sentinel's game is played **off its own turn** — its verb, **Premonition**, is a reactive/precognitive engine (dodge, counter, redirect, warn allies). It is the table's reaction specialist, distinct from the Guardian (proactive blade) and Consular (proactive powers). Defense comes from **anticipation** (saves + reactions), not toughness.

**Proficiency signature: Perception** — the Sentinel is the galaxy's keenest watcher and the only class to reach **Legendary Perception** (it also fuels Premonition's triggers).

---

## 2. Initial Proficiencies (Level 1)

| Category | Rank | Notes |
|---|---|---|
| **Perception** | **Expert** | the signature line |
| **Reflex** | **Expert** | precognitive dodge |
| **Will** | **Expert** | disciplined mind |
| **Fortitude** | Trained | the frail save |
| **Class DC** (Force) | Trained | Premonition effects |
| **Weapons** | Trained | simple weapons + **lightsabers** |
| **Defense** | Trained | **unarmored** + **light armor** |
| **Skills** | Trained in **4 + Int modifier** | a perceptive, moderately-skilled class |

Also at L1: gains **Attunement** (the Force resource; pool `2 + L`, [Phase 5 §2.2](2026-06-13-phase5-class-design-and-force.md)) — fuels Premonition (mechanics in §4).

---

## 3. Level Progression (chassis)

Chassis grants per [Phase 3](2026-06-13-phase3-progression-chassis.md) (incl. the new **level-1 class feat**). ✦ = Premonition class feature · ◆ = subclass feature (content → §4/§5).

| Lvl | Class features & chassis grants | Proficiency advances |
|---|---|---|
| 1 | **Premonition** ✦ · **subclass** ◆ · **class feat** · ancestry feat · Attunement | initial profs (§2) |
| 2 | class feat · skill feat | — |
| 3 | general feat · skill increase · ◆ | Class DC → **Expert** |
| 4 | class feat · skill feat | — |
| 5 | ancestry feat · skill increase · attribute boosts · ✦ | Fort → **Expert** · weapons → **Expert** |
| 6 | class feat · skill feat | — |
| 7 | general feat · skill increase · ◆ · **Weapon Specialization** | Perception → **Master** |
| 8 | class feat · skill feat | — |
| 9 | ancestry feat · skill increase · **Evasion** | Reflex → **Master** *(success→crit success)* |
| 10 | class feat · skill feat · attribute boosts | — |
| 11 | general feat · skill increase · ◆ · **Resolve** | Will → **Master** *(success→crit success)* |
| 12 | class feat · skill feat | — |
| 13 | ancestry feat · skill increase | Class DC → **Master** · armor → **Expert** · weapons → **Master** |
| 14 | class feat · skill feat | — |
| 15 | general feat · skill increase · ◆ · attribute boosts · **Greater Weapon Specialization** | Perception → **Legendary** ✦ |
| 16 | class feat · skill feat | — |
| 17 | ancestry feat · skill increase · ✦ | — |
| 18 | class feat · skill feat | — |
| 19 | general feat · skill increase · ◆ | — |
| 20 | class feat · skill feat · attribute boosts · **capstone** ✦ | — |

- **Skill increases:** 3/5/7/9/11/13/15/17/19 (raise one skill within the Expert-L3 / Master-L7 / Legendary-L15 gates).
- **Skill feats:** every even level (2–20).
- **No dead levels:** every level grants a feat or feature.
- **Weapon track:** Trained (L1) → **Expert (L5)** → **Master (L13)** — the hybrid-martial cadence (the Sentinel's Counter is a weapon Strike, so it is a gish, not a pure caster). Weapons cap at Master; **Legendary weapons are reserved for dedicated martials/Guardian.**
- **Weapon Specialization** (L7) / **Greater** (L15) are the universal grants ([Phase 3 §3.1](2026-06-13-phase3-progression-chassis.md)); keyed to weapon rank, they are **live from L7** (+2, Expert), rise to **+3** when weapons reach Master at L13, and **Greater** makes it **+6** (Master) at L15. They apply to weapon Strikes including **Counter** — but never to Force-power damage.
- **Save expertise** ([Phase 3 §3.2](2026-06-13-phase3-progression-chassis.md)): **Reflex (Evasion, L9)** and **Will (Resolve, L11)** → Master, each with *success→crit success* (the precognitive dodger's resilient pair). **Fortitude caps at Expert** — the frail save / deliberate vulnerability (fits HP 8, "defense by anticipation, not toughness"). No Legendary save; the Sentinel's one Legendary line is **Perception**.
- *(Exact advancement levels tunable at Gate A.)*

---

## 4. Premonition (the verb) — framework LOCKED; responses & ✦ features designed (2026-06-16)

**The Sentinel's *exclusive* identity is this reactive framework — not ownership of iconic Force powers** (see the Force-design principle, §4.1). The framework:

- **Premonition** `[reaction]` — one flexible reaction with a small menu of **responses** (fast to resolve — one decision, not a flowchart). **Trigger:** a creature you can perceive makes an attack or hostile action against you or an ally within range.
- **Two reactions baseline:** the Sentinel gains a **second reaction each round usable only for Premonition** (so 2 reactions/round — the core-mechanic table-speed budget).
- **Attunement overdrive:** spend **1 Attunement** for **one additional Premonition per round** (hard-capped at +1/round; pool-limited). This is the "out-react everyone" fantasy, *bounded* by the Force economy so it can never lock the table into endless interrupts. **Max 3 reactions/round, and only by spending resources.**
- **Foretell** `[1 action]` — the proactive *own-turn* play (so a reactor isn't bored on its initiative): read the immediate future to empower your next Premonition / mark a foreseen foe.
- **Fuel:** **Attunement** (Force resource, pool `2+L`, refuel via Center). The Sentinel spends Attunement on *reactions*, where the Consular spends it on *powers* — clean trinity differentiation.
- **Development (✦):** L5/L17/L20 deepen the engine (more responses available, overdrive/uses scaling, a capstone apex such as *never surprised / always act first*). **Breadth comes from subclasses (§5), not a pile of at-table reactions.**

### 4.0 Economy reconciliation (applies toolkit F3)

- **Range:** Premonition protects **you or an ally within 30 feet** that you can perceive.
- **The reaction is free; the *response* is what may cost Attunement.** Defensive responses (**Evade, Warn**) cost **0** — the never-gas-out-defensively baseline ([toolkit §5 / F3](2026-06-15-shared-force-toolkit.md)). Offense/debuff responses (**Counter, Foresee**) cost **1 Attunement** (the F3 rule that combat-impact offense/debuff is resourced). This is the snappy decision the framework wants: *defend for free, or spend to punish/disrupt.*
- **Overdrive** (the 3rd Premonition this round): **1 Attunement to unlock the extra reaction**, *plus* the chosen response's cost. (L17 makes the 3rd free.)
- **Foretell costs 0** — it is the reactor's free **proactive baseline** (its Strike-equivalent), not a resourced power.

### 4.2 Responses — the Premonition menu *(mechanism = position / timing / information, never energy/matter/minds; §4.1)*

One response per Premonition; pick on resolution (one decision, not a flowchart).

| Response | Type | Cost | Effect |
|---|---|---|---|
| **Evade** | position, defensive | 0 | **Step** (5 ft, doesn't trigger reactions) before the attack resolves. If the Step takes you out of the attacker's reach/range or into cover, apply that against the triggering attack (it may take the cover penalty or fail to reach you). *Foreknowledge footwork — not a flat AC dodge (that's the Sense toolkit's Precognitive Parry).* |
| **Counter** | timing, offensive | 1 | **`[once per round]`.** Make a single melee or ranged **Strike** against the triggering creature (must be a legal target). You strike into the opening as it commits. **Full accuracy — reaction Strikes are never subject to MAP** ([Phase 1 §4.2](2026-06-13-phase1-core-mechanic-and-traits.md)). |
| **Warn** | information, defensive (ally) | 0 | The ally targeted by the trigger may immediately **Step**, **or** gains a **+2 circumstance bonus** to AC (or the relevant defense) against the triggering effect. *A shouted warning — works against an area effect's edge via the Step.* |

**Niche/dead-zone check:** Evade is best when a square earns cover/breaks reach, dead when cornered; Counter is best when the foe is in range and you have Attunement, dead otherwise; Warn is best shielding a squishy ally from a big hit, dead when solo. None duplicates a toolkit power (deflection, parry, healing, telekinesis, mind influence).

### 4.3 Foretell `[1 action]` `[concentrate]` `[Force]`

Designate one creature you can perceive as **foreseen** until the start of your next turn (cost **0**; the proactive own-turn play). While a creature is foreseen:
- It **can't make you off-guard**, and you gain a **+1 circumstance bonus to AC and saves** against it (you see its moves coming).
- The **next Premonition you trigger off that creature is empowered:** *Evade* → you may **Stride** instead of Step · *Counter* → the Strike treats the target as **off-guard** · *Warn* → the ally gets the Step **and** the +2 (both).

*Foretell gives the reactor a satisfying initiative-turn button and converts foresight into a reactive payoff, without competing for the Attunement that fuels reactions.*

### 4.4 Premonition development (✦)

- **L5 — Widened Sight:** gain a fourth response, **Foresee** *(information, debuff, 1 Att)* — when the trigger creature acts, you call its move: it becomes **off-guard to the next attack made against it** before the start of your next turn. Foretell now affects up to **two** creatures, and a foreseen foe is also **off-guard to you**.
- **L17 — Unclouded Sight (Tier IV):** your **overdrive 3rd Premonition is free** (0 Att; still capped at 3 reactions/round — honors the locked table-speed cap, removing only the resource cost). At the **start of combat** you may Foretell every foe you can perceive for free (no action) — you read the whole battlefield's opening.
- **L20 — Prescience (capstone):** you **can't be surprised** and are **never off-guard** to any creature you can perceive; you and allies within 30 ft gain a **+4 status bonus to initiative**. Once per round, your Premonition may trigger off **any** hostile action a foe takes (not only attacks) — total foresight. *(The "never surprised / always act first" apex; keeps the 3-reaction cap intact — it broadens the* trigger*, not the count.)*

### 4.1 Force-design principle (cross-cutting) — *don't class-lock iconic powers*

A Force class's **exclusive** claim is its **verb-framework**, *not* ownership of iconic Force abilities. **Iconic powers** (deflection, telekinesis, mind influence, healing, precognitive foresight) are **shared Force toolkit** — discipline/feat-gated and **portable** across Force users (like Forms via their "Guardian Mastery" clause). So the Sentinel must **not** absorb e.g. the Guardian's **Deflect** as a Premonition response; if it deflects, it does so via the shared toolkit, as a specialist's *application*, not a class-exclusive grant. *(Recorded also in the [class roster](2026-06-15-class-roster-sketch.md) Force-trinity section.)*

## 5. Subclasses (Premonition forks) — five, designed (2026-06-16)

Branch at **L1**; features on the **1 / 3 / 7 / 11 / 15 / 19** cadence (the ◆ rows in §3). **Five forks:** Warden, Shadow, Justicar (§5.1–5.3) plus Investigator and Corsair (§5.4–5.5, adapted from the prior project's Watchman/Corsair). Each **shapes the Premonition reaction chassis** toward a different answer to *"how do you react?"* — none replaces the verb, none grants an iconic shared-toolkit power (§4.1). Built parallel for cross-balance: L1 signature · L3 deepen · **L7 a fork-flavored economy feature** · L11 Tier-III spike · L15 major · **L19 resource-/frequency-bounded capstone**. *(All numbers Gate-A tunable.)*

### 5.1 Warden — reactive protector *(role lean: Support)*

*You react to put yourself between the blow and the people behind you.*

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Interpose** | Gain **Athletics** (or +1). When a creature attacks an ally within range and you are within 5 ft of that ally, your **Warn** may instead **make you the target of the triggering attack** (you step into the path). *Heroic-sacrifice bodyguard — the HP-8 risk is real and intended.* |
| 3 | **Shielding Warning** | Your **Warn** grants the +2 circ AC **and** the Step (both, not either), plus a **+1 circ bonus to the triggering save** if it's a save effect. |
| 7 | **Vigilant Bulwark** | Once per round you may use **Warn/Interpose without spending a reaction** (out-protect by economy). |
| 11 | **Aegis Field** | Allies within 15 ft gain **+1 circ AC** (passive threat-reading aura). When you Interpose, **reduce the redirected attack's damage by your level** (foresight *bracing* — flat reduction, not a resistance power). |
| 15 | **Guardian's Premonition** | Once per round, when an ally within range would be **critically hit**, react to make it a **normal hit** instead. |
| 19 | **Unbreakable Watch** *(capstone)* | Allies within 15 ft **can't be critically hit** while you're conscious and not off-guard. Once per round, your protective reaction shields **every** ally within range from one area effect. |

### 5.2 Shadow — reactive ambusher *(role lean: single-target offense + Utility)*

*You react from concealment, strike the foreseen opening, and are gone.* **Vanish is mundane Stealth/Hide aided by foresight — not Force Cloak** (§4.1); a Shadow who wants true invisibility buys that power as a feat.

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **From the Shadows** | Gain **Stealth** (or +1). Your **Counter** against a creature **off-guard to you** (unaware of you, or foreseen via Foretell) deals **+1d6 precision damage**. |
| 3 | **Fade** | After any Premonition reaction, you may **Step** as part of the reaction. |
| 7 | **Vanish** | Once per round, after a Premonition you may **Hide** as a free action **even while observed**, if you end with cover/concealment from the triggering creature. |
| 11 | **Killing Foresight** | Precision die → **2d6**. Your **Counter** may now trigger when *any* creature you perceive within range attacks (not only when you're the target). Still once per round. |
| 15 | **Ghost Step** | When you **Evade** you may **Stride** (not just Step) and **Hide** as part of the reaction; a creature that loses track of you is **off-guard to your next Counter**. |
| 19 | **Inevitable Ambush** *(capstone)* | Precision die → **3d6**. Once per round, your **Counter** against a creature off-guard to you is **automatically a critical hit if it hits**. |

### 5.3 Justicar — reactive punisher *(role lean: Control)*

*You react to make attacking you — or yours — a mistake.*

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Retribution** | Gain **Intimidation** (or +1). When your **Counter** hits, the target is **off-guard to the next attack against it** before your next turn (knocked off-rhythm; sets up allies). |
| 3 | **Foreseen Riposte** | When an enemy's attack against you **hits** or **critically misses**, your **Counter** against it this round gains **+1 circ to hit**. |
| 7 | **Vengeful Premonition** | **Trigger-recharge:** when a creature **critically hits** you or an ally within range, immediately **regain your Counter this round** (may Counter a second time). |
| 11 | **Punishing Reach** | Your **Counter** may trigger when a creature attacks an **ally** within range. On a hit, the target also takes **−1 circ to its next attack** (deterrent; doesn't stack with itself). |
| 15 | **Inescapable Judgment** | When your **Counter** hits, the target is **frightened 1** (frightened 2 on a crit). |
| 19 | **No Refuge** *(capstone)* | You may **Counter beyond the once-per-round limit** by spending **2 Attunement** per extra Counter. A creature frightened by your Counter **can't reduce its frightened below 1** while within your Premonition range. |

### 5.4 Investigator — reactive detective / controller *(role lean: Control + Information)*

*You read the foe before it commits, then subdue it.* (Adapted from the prior **Path of the Watchman**.) **Mechanism = information + mundane maneuvers guided by foresight** — Recall Knowledge and Class-DC Trip/Disarm/Shove, not a Force power (§4.1).

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Deductive Angle** | Gain **Diplomacy or Society** (or +1). When you use a **Premonition** reaction, you may **Recall Knowledge** about the triggering creature as part of it (free); on a success, that reaction gains **+1 circ** to its roll/effect (you spotted the tell). |
| 3 | **Precognitive Maneuvers** | New response **Maneuver** *(control, 1 Att)* — react to **Trip, Disarm, or Shove** the triggering creature; the target saves against your **Class DC** (foresight leverage, not muscle — no separate maneuver roll, no MAD). |
| 7 | **Read the Room** | Once per round, **Recall Knowledge as a free action** (untethered from a Premonition) against any creature you perceive; share one fact to grant an ally **+1 circ** to their next attack vs that foe. |
| 11 | **Subduing Foresight** | A successful **Maneuver** also imposes **−1 circ to the foe's attacks** until your next turn; you take no penalty to deal nonlethal damage; you may fold a Maneuver into a **Counter** (Strike + maneuver, one reaction). |
| 15 | **Total Recall** | Against a creature you've Recalled this encounter, your Premonition responses gain **+1 circ** (reliable, no check) and your **Maneuver vs it also leaves it off-guard** until your next turn. |
| 19 | **Case Closed** *(capstone)* | Once per round, a successful **Maneuver** lets you apply a second, different maneuver to that foe for free. Creatures you've Recalled **can't be hidden/concealed from you**, and your **Counter** treats them as off-guard. |

### 5.5 Corsair — reactive ranged dirty-fighter *(role lean: ranged single-target offense + Utility)*

*A fringe-dweller who fights dirty — blasters, shoto-sabers, and foresight.* (Adapted from the prior **Path of the Corsair**.) The ranged fork the other four lack; distinct from the Scoundrel's *proactive* Mark by being *reactive*. **Mechanism = mundane gunplay/feints/ricochet** (not Force powers; §4.1).

| Lvl | Feature | Effect |
|---|---|---|
| 1 | **Gunslinger's Foresight** | Gain **blaster proficiency** (Trained) and **Deception** (or +1). Your **Counter** may be a **ranged blaster Strike** within range; ranged Premonition Strikes **don't provoke Reactive Shot** and **ignore the lesser-cover penalty for firing into melee** (ricochet angles). |
| 3 | **Underhanded Trick** | Gain the action: `[1 action]`, **Deception** to Feint a target in reach (or within 30 ft with a blaster) → **off-guard to your attacks** until end of your next turn (crit: off-guard to *all* attacks). Sets up your Counter — the own-turn play. |
| 7 | **Ricochet Shot** | Once per round, your blaster **Counter ignores cover and concealment** (full bank-shot) and can target a creature you can't precisely see. |
| 11 | **Dirty Fighting** | When your **Counter** (or any Strike) **crits** an off-guard creature, it is **blinded or deafened** (your choice) until your next turn. A successful **Underhanded Trick** now makes the target off-guard to *all* your attacks. |
| 15 | **Bank Shot** | When you **Counter** with a blaster, the bolt **ricochets to a second creature** within 15 ft, dealing **half** the Counter's damage (no second roll). |
| 19 | **Outer Rim Legend** *(capstone)* | Your blaster **Counter ricochets to up to two** extra creatures (half damage each); a foe you make off-guard via a trick this round is off-guard **to your whole party**; ranged Premonition Strikes ignore all cover/concealment. |

**Cross-balance & §4.1 notes (all five).** Same-level features are comparable in value with different *shapes*: Warden = ally defense, Shadow = burst + stealth, Justicar = debuff/deter, Investigator = info + control maneuvers, Corsair = ranged offense + tricks. The **L7 quintet** is the watch-item (Warden's free reaction is the most reliably-useful; Justicar's is conditional, Shadow's/Corsair's are utility, Investigator's is info/support) — judged balanced across axes, flagged for Gate-A. The Justicar **L7/L19** and Corsair **ricochet** interact with Counter's once-per-round clamp and the no-MAP-on-reactions rule; secondary ricochet targets take **half** damage to keep the off-turn full-accuracy multi-hit bounded — consistent with the [balance pass](2026-06-15-shared-force-toolkit.md). No feature grants Deflect, Force Cloak, Force Barrier, telekinesis, healing, or mind-influence — those remain feat-bought toolkit powers any Sentinel may add. Corsair's blaster proficiency is the one cross-subclass weapon grant (the enabler for its ranged identity).

---

## 6. Class Feats — designed (2026-06-18)

The Sentinel's own feat menu (picked into the L1,2,4,6,8,10,12,14,16,18,20 class-feat slots, [Phase 3 §3](2026-06-13-phase3-progression-chassis.md)). **Scope (per the §4.1 / toolkit boundary):** these feats **shape the Premonition framework** (responses, Foretell, reaction economy, the precognition/perception edge) — they do **not** re-grant shared-toolkit Force powers (Force sight, Mind Probe, Saber Throw, etc.), which any Force user buys generically. The clean bridge is the **conduit** feats, which let the Sentinel *apply* toolkit reaction-powers (Precognitive Parry, Energy Absorption, Force Reflection) **better/cheaper through its engine** — making it the deflection/parry *specialist* without owning those powers. **~50 feats total** (the ORC norm — ~36 general in §6.1 + ~15 subclass-gated in §6.2), giving real choice at every level slot (a character takes 11 across L1–20). *(Inspiration mined from the prior ClassFeat suite; tech/slicer feats routed to Tech Specialist, mind/sight/saber feats to the generic toolkit. Numbers Gate-A tunable.)*

### 6.1 General class feats (~36) — any Sentinel

| Lvl | Feat | Effect |
|---|---|---|
| 1 | **Watchful Initiative** | Roll **Perception for initiative** with **+2 circ**; you **can't be off-guard** during the first round. |
| 1 | **Foretelling Step** | When you **Foretell**, you may **Step**. |
| 1 | **Danger Sense** | You can't be off-guard to creatures you've detected; **+2 circ vs being ambushed/surprised**. |
| 1 | **Empathic Read** | Use **Perception** to read intentions/emotions; +1 circ to spot lies & hostility (the watcher's instinct). |
| 2 | **Premonitory Warning** | Your **Warn** can target **two allies** in range. |
| 2 | **Anticipatory Reflex** | `[once per minute]` With **no reaction left**, use a **defensive** Premonition response for **1 Att**. |
| 2 | **Evasive Foresight** | Your **Evade** Step is **10 ft** and ignores difficult terrain. |
| 2 | **Quick Draw** | Draw or switch a weapon as part of a Strike or **Counter** (gish flow). |
| 4 | **Quickened Foresight** | **Foretell** is a **free action** the first time each round you roll initiative or a foreseen foe falls. |
| 4 | **Reactive Conduit** | A Force power with the **`[Sense]`/`[Control]`** trait used **as a reaction** costs **1 less Att** (min 0). *(Specialist bridge; §4.1.)* |
| 4 | **Foreseen Pivot** | `[once per minute]` **Reroll a failed save** vs a creature you perceive; keep the higher. |
| 4 | **Disorienting Counter** | When your **Counter** hits, the target can't make you off-guard until your next turn. |
| 6 | **Mind Fortress** | **+1 circ to Will saves**; once per round reduce your frightened/fascinated by 1 (free action). |
| 6 | **Anticipatory Strike** | Your first Strike against a creature you **Foretold** this turn treats it as **off-guard**. |
| 6 | **Opportune Counter** | Your **Counter** may also trigger when a creature in reach **Strides** or makes a ranged attack (still once/round). |
| 6 | **Guardian's Reflex** | Your free defensive response (Evade/Warn) may also grant an **adjacent ally cover** vs the triggering attack. |
| 6 | **Precognitive Dodge** | `[once per round]` Spend **1 Att** when you'd be **critically hit** to make it a normal hit. |
| 8 | **Wide-Angle Sight** | Premonition **range → 60 ft**; perceive triggers through sense-blunting conditions. |
| 8 | **Deflecting Conduit** | Gain **Energy Absorption** as a known power; using it **counts as a Premonition** (fired through the engine). |
| 8 | **Blindsense** | Gain **imprecise sense 15 ft** (foresight); ignore concealment from creatures within it. |
| 8 | **Shared Premonition** | When you **Foretell** a foe, one **ally** treats it as **off-guard** on their next attack vs it. |
| 10 | **Storm of Premonition** | `[once per minute]` This round your **overdrive** Premonition costs **0 Att**. |
| 10 | **Force Reflection Conduit** | Gain **Force Reflection** as a known power, fired as a Premonition (ranged redirect). |
| 10 | **Unshakable** *(req. Danger Sense)* | You can't be made off-guard by flanking, surprise, or being hidden-from. |
| 12 | **Precognitive Battlefield** | Start of combat: allies within 30 ft gain **+1 status initiative** and can't be off-guard round 1. |
| 12 | **Deep Conduit** *(req. Reactive Conduit)* | Discount also covers **`[Battle]`** reactions; once per round one such reaction is **free**. |
| 12 | **Pinning Foresight** | When you **Foretell** then **Counter** a foe, it's **off-guard** and **can't Step** until your next turn. |
| 14 | **Untouchable Foresight** | While you have **≥1 Att** and aren't off-guard: **+1 circ AC**. |
| 14 | **Greater Conduit** *(req. Deep Conduit)* | Your Premonition reaction-powers gain **+1 circ** to their roll/DC. |
| 14 | **Foreseen Demise** | When your **Counter** drops a foe to 0 HP, **regain 1 Att** and refresh **Counter** this round. |
| 16 | **Master's Reaction** | `[once per round]` Use a **Premonition response and a Force-power reaction** on the same trigger (+1 Att). |
| 16 | **Shared Prescience** | Allies within 30 ft **can't be critically hit** during the first round of combat. |
| 18 | **Foretell the Field** | **Foretell** affects **all foes within 30 ft**. |
| 18 | **Ceaseless Watch** | Use **Foretell** as a **free action** once per round. |
| 20 | **Perfect Premonition** *(capstone)* | `[once per round]` A Premonition response **costs no reaction** (extra interrupt; still pays its Att). |
| 20 | **Inevitability** *(capstone)* | When you **Foretell** a foe, the first time it would **hit** you/a foreseen ally before your next turn, make it a **miss** (once/round). |

### 6.2 Subclass feats (~15) — gated to your §5 subclass

A few feats per fork, deepening its signature (the ORC norm). Each requires the named subclass.

| Lvl | Feat | Subclass | Effect |
|---|---|---|---|
| 4 | **Bodyguard's Burst** | Warden | When you Interpose, the ally also gains **+2 circ AC** vs other attacks until your next turn. |
| 10 | **Extended Guard** | Warden | Interpose range **15 ft**; you may **Step to the ally** as part of it. |
| 16 | **Retributive Guard** | Warden | When you Interpose, you may immediately **Counter** the attacker (1 Att). |
| 4 | **Ambush Reflex** | Shadow | When you Counter from concealment, you may **Step before** the Strike. |
| 8 | **Deadly Foresight** | Shadow | Your Shadow precision die increases by **+1d6**. |
| 14 | **Phantom Strike** | Shadow | `[once per minute]` After a successful Counter while hidden, immediately **Hide** again. |
| 4 | **Punishing Resolve** | Justicar | After a foe damages you, your next **Counter** vs it deals **+2 status damage**. |
| 10 | **Deterring Presence** | Justicar | Foes you've Countered this encounter take **−1 circ to attack you**. |
| 16 | **Relentless Riposte** | Justicar | `[once per minute]` Vengeful Premonition also triggers on a **normal hit**. |
| 4 | **Tactical Analysis** | Investigator | Share a Recalled fact: allies gain **+1 circ** vs that foe. |
| 8 | **Pressure Point** | Investigator | Your **Maneuver** can **Grapple**; a foe you've grabbed is **off-guard to your Counter**. |
| 12 | **Case Cracked** | Investigator | Vs a Recalled foe, your Maneuvers **can't be critically failed**; Trip/Shove distance **+5 ft**. |
| 4 | **Flashy Feint** | Corsair | **Underhanded Trick** works at 30 ft even **unarmed**; a feinted foe is **off-guard to your allies** too. |
| 8 | **Ricochet Stratagem** | Corsair | Your **ranged Strikes ignore Concealed and standard cover** (not greater). |
| 14 | **Quickdraw Corsair** | Corsair | Draw/holster **+ a ranged Counter** as one reaction; **+1 circ** to ranged Counters. |

**§4.1 / balance notes.** No feat grants an iconic Force power as an exclusive: the **Conduit** line (4/12/14) only discounts/sharpens powers the Sentinel *already bought*, and the access feats (Deflecting/Force Reflection Conduit) route those powers **through the Premonition engine** (the specialist bridge) rather than owning them. **Storm of Premonition** (10) and **Perfect Premonition** (20) remove *cost*, not the count — honoring the locked 3-reaction table-speed cap. Reroll/AC values stay bounded (reroll-keep-higher, +1 circ). Subclass feats deepen each fork's signature without exceeding its capstone. All flagged for Gate-A alongside the chassis.

---

## 7. Carried Forward

- ~~**§4 Premonition** mechanics + ✦ development~~ — **DONE (2026-06-16).**
- ~~**§5 subclass** features — Warden/Shadow/Justicar (+Investigator/Corsair)~~ — **DONE (2026-06-16).**
- ~~**§6 Class feats** list~~ — **DONE (2026-06-18):** ~50-feat menu (≈36 general + 15 subclass-gated), the ORC norm; §4.1-clean (no exclusive toolkit re-grants).
- **Gate-A validation** (eHP via saves+reactions, reaction-economy/table-speed check, DPR-equivalent of counters, the L7 subclass quintet, Conduit cost-stacking).
- Flavor/description → rules-writing. **Sentinel is now content-complete pending Gate-A.**

---

## 8. Revision — Premonition trait restructure (2026-07-03)

The single **Premonition [reaction] + response menu** proved mechanically clunky and was restructured in player-core: each former response (**Evade, Warn, Counter, Foresee**, Investigator's **Maneuver**) is now a **standalone reaction with the [Premonition] trait**, each with its own rules-precise trigger. The class's extra reaction (and the Overdrive third) is now "usable only for reactions with the Premonition trait." Consequences: Counter's trigger is explicitly self-only at baseline (Killing Foresight / Punishing Reach broaden it, resolving the old shared-trigger contradiction); **Premonition range** (30 ft) is a defined term on the chassis; the Conduit feats grant powers the Premonition trait instead of "counts as a Premonition"; **Precognitive Dodge** now costs a reaction (Premonition trait) rather than no action. Reactive Conduit deliberately does NOT grant the trait (kept a pure discount) pending the Gate-A reaction-stacking review.

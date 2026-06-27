# Rank-Gated Effects

**Status:** Approved (pattern + slice domains; full enumeration → content expansion)
**Date:** 2026-06-14
**Type:** Content spec — resolves the **Gate A T1 directive** (make expertise *felt* through capability, not bigger numbers).
**Upstream:** [Phase 1 T1](2026-06-13-phase1-core-mechanic-and-traits.md) (+1/rank kept), [Phase 3 rank gates](2026-06-13-phase3-progression-chassis.md) (Expert L3 / Master L7 / Legendary L15), [Skill Actions](2026-06-14-skill-actions.md) (the substrate), [Gate A §6](2026-06-13-gateA-balance-validation.md).

> The +1/rank *number* stays tiny by design; **these effects** carry the "expertise feels real" load. Every effect below is **purely additive** and honors the gating philosophy (§1).

---

## 1. Gating Philosophy (binding)

1. **Effect-gating is the default; permission is open.** Anyone may attempt nearly any action; proficiency raises the **outcome and reliability**, not the **right to try**. The **untrained = +0** math (Phase 2 cliff) is the disincentive — a novice can try a Hard task, will usually fail, and will crit-fail more.
2. **Hard access-locks are rare**, flagged **`[trained-required]`** — reserved for actions that are fictionally incoherent untrained *or* have a designated untrained fallback. This *re-frames* the SF2E "(T)" tag: for most actions, **trained = reliable/safe/full version; an untrained attempt is still allowed** (the GM may raise the DC and worsen the crit-fail). The `[trained-required]` set (slice): **Craft, Create Forgery, Treat Wounds** (fallback: anyone can Administer First Aid), **Treat Disease**. Everything else is attemptable untrained.
3. **Rank-gated effects are purely additive.** Expert/Master/Legendary grant new outcomes, options, and riders. They **never** remove a lower-rank character's ability to attempt anything.
4. **"Remove a limit" effects lift only a *proficiency* limit** (e.g., "a Master can Hide without cover"), never another character's baseline attemptability.

**Rank effects attach to the skill/proficiency, not the class.** Whoever reaches a rank gains its effects; a class's **proficiency signature** merely guarantees it reaches **Legendary** in that domain (Soldier→weapons, Scoundrel→skills, Guardian→Force, Technician→Computers/Repair). Ranks arrive per the Phase 3 gates.

**The four anchor types** (from [Skill Actions §7](2026-06-14-skill-actions.md)): new **degree outcomes** · new **action modes/options** · success **riders** · **removed proficiency-limits**.

---

## 2. Weapon Proficiency *(Soldier signature; any weapon user)*

- **Expert — Critical Specialization.** Your critical hits with a weapon group apply that group's **crit specialization effect** (e.g., **blaster/energy:** target is **Off-Guard** until your next turn; **vibro/melee:** **persistent bleed**; **automatic:** the crit also strikes one adjacent creature for half). *(New degree outcome.)*
- **Master — Combat Flow.** Once per turn, when you critically hit or drop a foe to 0 HP, take a **free Interact or Step**. Your crit specialization effects are intensified (e.g., bleed scales). *(New option.)*
- **Legendary — Unerring Fire.** Ignore the first range increment's penalty and the bonus from **lesser/standard cover** your target benefits from. *(Removed limit — you, the Legend, shoot around cover; nobody else loses any ability.)*

## 3. Force Proficiency & Class DC *(Guardian signature; any Force user)*

- **Expert — Focused Casting.** Your **Deflecting Stance** AC bonus rises (+1→+2) and your basic powers gain a minor rider (a Telekinetic Nudge that fails still nudges 5 ft on a normal failure). *(Rider.)*
- **Master — Efficient Attunement.** Your **Pushes cost 1 less Attunement** (minimum 1), and you may **Center as a free action once per turn**. *(New option / resource flexibility — not a flat to-hit bump.)*
- **Legendary — Perfect Deflection.** Your **Deflect** *negates* a ranged Strike (rather than reducing it) and may **redirect** it at any creature you can see; your stance bonus rises to +3. *(Intensified outcome; the duelist apex.)*

## 4. Skill Exemplars *(any character reaching the rank)*

### Stealth *(Scoundrel signature)*
- **Expert — Quiet Step.** When you **Sneak**, you may move up to your full Speed (instead of half) once per turn. *(Removed proficiency-limit.)*
- **Master — Foil Senses.** You can **Hide** and **Sneak** even against creatures relying on precise non-visual senses; remaining Hidden after a Strike no longer ends automatically until the end of your turn. *(New mode.)*
- **Legendary — Vanish.** You can **Hide even while observed and without cover** (briefly); creatures you are Hidden from are **Off-Guard** to your first Strike each turn. *(Categorical capability.)*

### Computers *(Technician signature — slicing)*
- **Expert — Multitask.** A successful **Slice** also lets you **Access HoloNet** (pull data) as part of the same action; you may attempt Slice in **1 action** once per encounter. *(Rider + mode.)*
- **Master — Backdoor.** A **critical** Slice plants a **backdoor** (re-enter later without a check); you can Slice a system **remotely** via the HoloNet (lift the "be at the console" limit). *(New degree + removed limit.)*
- **Legendary — Ghost.** Your Slices **never trigger alarms on a failure** (only crit-fail), and you can Slice **multiple linked systems** with one action. *(Crit-fail protection + scale.)*

### Medicine *(Technician — Field Medic)*
- **Expert — Field Surgeon.** **Treat Wounds** also ends one minor condition on a success; **Administer First Aid** is **1 action**. *(Rider + reduced cost.)*
- **Master — Battlefield Medic.** Your First Aid also restores HP; you can **Treat Wounds** in a fraction of the time. *(New outcome.)*
- **Legendary — Pull From the Brink.** You can Treat Wounds on a creature even at 0 HP, waking and healing it; you may stabilize a dying ally at range. *(Removed limit.)*

### Athletics *(Soldier/Guardian — maneuvers)*
- **Expert — Powerful Maneuvers.** Your Shove/Trip/Grapple crits gain improved riders (Shove crit pushes 15 ft; Trip crit also damages). *(Degree.)*
- **Master — Hurl.** Your **Shove/Reposition may Hurl** a target off an edge / into a hazard by default (target gets the §G basic Reflex save). *(New option — gated to Masters, but never restricts a novice's normal Shove.)*
- **Legendary — Overpower.** Your forced-movement and maneuvers gain **reach**, or affect a second adjacent target once per turn. *(Scale.)*

### Social skills *(Scoundrel — Face; any)*
- **Expert (Diplomacy/Deception/Intimidation):** your encounter **appeals** gain a small rider (a successful Make a Case also reveals a Lever; a successful Demoralize also makes the target Off-Guard to your next appeal). *(Rider — boosts the Phase 4 engine.)*
- **Master:** once per encounter, **Demoralize** or an appeal affects **all valid targets in a burst**. *(Mode.)*
- **Legendary:** your crit successes on social appeals impose a **Guard-removing** or **double-Resolve** effect. *(Intensified outcome.)*

---

## 5. Validation Against the Gating Rule

- Spot-check: none of the above says "you must be rank X to *attempt* Y." Each grants a *new* capability to the higher-rank character. ✔
- "Removed-limit" effects (Quiet Step, Backdoor-remote, Hurl, Pull From the Brink, Unerring Fire) all lift a **proficiency** constraint on the *holder* — a novice's normal Sneak/Slice/Shove/Treat Wounds/Strike is untouched. ✔
- Numbers stay bounded: the only flat bumps are the small Deflection-stance steps (+1→+3 over the campaign, already in budget); everything else is capability. ✔ T1 satisfied without re-opening the spread.

---

## 6. Carried Forward

- **Full enumeration** (every skill + Perception + armor/save proficiencies × Expert/Master/Legendary) → rules-writing / content expansion; §2–4 establish the pattern and the slice's key domains.
- **Crit specialization effects** per weapon group → finalize with the full weapon catalogue (Phase 8 equipment).
- **Exact numbers** (bleed amounts, time reductions, burst sizes) → Gate A spot-checks when enumerated.
- **Apply the §1 re-tag** to the [Skill Actions spec](2026-06-14-skill-actions.md)'s "(T)" tags during rules-writing (mark the few `[trained-required]`; note the rest allow untrained attempts).

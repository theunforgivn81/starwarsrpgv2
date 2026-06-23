# Gate A — Balance Pass (all seven classes + shared layers)

**Status:** Part 1 done 2026-06-19 (Guardian/Sentinel/Soldier/Consular); **Part 2 done 2026-06-20** (Scoundrel/Tech Specialist/Officer — see §A). Fixes applied; watches recorded.
**Type:** Balance validation (`ttrpg-balance-analysis`) across the content-complete roster: **Guardian, Sentinel, Soldier, Consular** + the [Force toolkit](2026-06-15-shared-force-toolkit.md) and [Lightsaber Forms](2026-06-18-lightsaber-forms.md).
**Method:** relative comparison on the bounded spine (on-level attack +5/+12/+19; Level term cancels; MAP −4/−8; weapon dice 1→4; Weapon Spec +2/3/4→+4/6/8; Force damage 1→4 dice, no attribute). Absolute creature numbers are still Phase-7/Gate-A placeholders, so this is a **relative** pass (class-vs-class + vs the spine) + a stacking/nova audit.

---

## 1. What holds ✅

- **Bounded accuracy intact.** No flat to-hit/AC creep anywhere; every **Legendary** line is the universal +4 rank *cap*, not a spine break. Save-DCs track saves (no high-level blowout, Phase 3 §9 holds).
- **Role shapes are correct (relative).** eHP: **Soldier > Guardian > Sentinel ≈ Consular**; single-target DPR: **Guardian > Soldier(area) > Consular(burst) > Sentinel(control)** — both orderings match the role-profile budgets. No DPR/eHP outlier breaks the bracket *at base*.
- **No action-positive loops** (pending the Officer's action-granting, audited later). No infinite combos.
- **Save-or-lose gated:** hard control keeps `[incapacitation]` + `[once per minute]` (toolkit pass); class control is mostly *soft* (off-guard, Suppressed-debuff, frightened).
- **No-daily model intact:** Attunement is per-encounter; the few `[once per day]` feats (Unyielding, Deny Death) are sparing.
- **Anti-MAD holds:** every class runs on one attribute (Walking Armory/Fearsome Bulwark for the Soldier; Class-DC/level-based riders elsewhere).

---

## 2. Fix 🔴 (applied)

### F-A1 — Reaction stacking exceeds the table-speed budget
The core mechanic budgets **~2–3 commonly-triggering reactions/character** for table speed; the Sentinel is deliberately hard-capped at 3. But:
- **Guardian:** Vigilant Guard (2nd reaction, L7) + Combat Reflexes (+1, L10) + Greater Combat Reflexes (+1, L14) → **up to 4/round**.
- **Soldier:** Withering Fire (2nd Suppressing Reaction, L13) + Combat Reflexes (+1) + Greater (+1) → **up to 4/round**.

4 interrupts/round from one player taxes the table past the budget.
**Fix (applied):** a **system-wide hard cap of 3 reactions per round** (recorded in [Phase 1 §4.3](2026-06-13-phase1-core-mechanic-and-traits.md)); the Combat-Reflexes-style feats raise *toward* 3, never past it. Noted in the Guardian/Soldier specs.

### F-A2 — Bulwark flat-resistance stacking trends to damage-negation
The Soldier/**Bulwark** can layer flat resistance: **Dig In** (resist = CON, when stationary) + **Armored Reaction** (resist = level, **doubled = 2×level vs Suppressed**) + **Unshakable Juggernaut** (half damage on a *failed* Fort save). Armored Reaction's `2×level` = **34 at L17** — larger than most on-level hits (~25–40), so vs a Suppressed attacker a hit is near-negated, *then* halved again on a failed Fort save.
**Fix (applied):** Armored Reaction resist = **half your level** (→ **level** vs Suppressed, not 2×); Dig In and Armored Reaction may stack but to a modest total (~½-of-a-hit reduction, not negation). Bulwark stays the toughest fork without becoming unkillable.

---

## 3. Tune 🟠 (applied where clear; one flagged)

### F-A3 — Consular pool inflation *(applied)*
**Deep Reservoir** (pool `3+L`) + the **Deep Reserve** feat (+2) → pool **11 at L20**, on top of Center +3 and the metamagic line. The single-round nova is already bounded by the `[once per minute]` gates on Empower/Twin/Overchannel/Quickened, but the standing pool was over-deep.
**Fix (applied):** **Deep Reserve** feat reduced to **+1** (pool tops at `3+L`, +1 feat ≈ 10 at L20). Metamagic gates unchanged (they hold).

### F-A4 — Soldier multi-Legendary load *(RESOLVED 2026-06-19)*
The Soldier reached Legendary in **Fort, armor, weapons, AND Class DC** (4 lines vs 1–2 for the others) — compounding into high-level eHP and an over-strong suppression DC.
**Fix (applied):** cap **weapons** and **Class DC** at **Master**, leaving **Fort + armor** Legendary (2 lines, both *defensive* — the durability-tank spotlight). Rationale (per the user): the **Scoundrel** is the dedicated ranged striker, so the Soldier sits one weapon rank lower; and Class DC → Master is a soft nerf because the Soldier's Class-DC abilities are mostly **multi-target** debuff/area. *(Chosen over the original armor+Class-DC recommendation — keeps the tank's armor at cap, which is more on-identity than capped weapons.)*

### F-A5 — Intercede double-scaling *(noted, left as-is)*
**Improved Intercede** = `4 + level + STR` (= 30 at L20) vs on-level hits ~30–40 → negates ~one hit/use, which is the intended "save an ally from a blow." It *slightly* exceeds one hit vs weaker attackers. Acceptable; if Gate-A tuning wants it tighter, drop to one scaling term (`4 + level` *or* `+ STR`).

---

## 4. Note 🟡 (by design; validate in playtest)

- **Sentinel & Consular low sustained DPR** — intended (Control/Support roles; offense ≤1). Their value is control/protection/burst, not damage — confirm it *feels* impactful (Mode A/B playtest), not like dead weight.
- **Tank-aggro dependency** — the whole design leans on *soft* aggro (Demand Attention, Oppressive Presence, Bind the Blade, suppression, Intercede's threat) actually pulling fire onto the tanks so the HP-8 casters survive. This is the #1 thing to validate at the table; if enemies can profitably ignore the tanks, the casters are too fragile.
- **Two HP-8 casters share frail physical saves** (Sentinel weak Fort, Consular weak Reflex) — a Sentinel+Consular-heavy party is doubly exposed to the targeted save. Party-comp texture, not a fix.
- **Guardian is the current single-target DPR ceiling** — re-bracket against the **Scoundrel** (DEX precision striker) when built; that's the proper comparable.
- **Suppressed −2 on a large cone** = high aggregate party-mitigation (many foes, −2 each). It's the control-tank's spotlight and costs the Soldier its damage; watch the aggregate in multi-enemy fights.

---

## 5. Carried into the remaining build

- Apply the **3-reaction cap** to any future reaction feats (Scoundrel, etc.).
- **Officer** will need the dedicated **action-granting audit** (the one not-yet-tested red-flag category — grant-an-ally-an-action is action-positive by definition).
- Re-run a focused pass once the **Scoundrel** sets the striker bracket and the **Tech Specialist** companion adds an extra actor.
- Absolute tuning (HP-per-level, creature DPR, exact dice) still belongs to **Phase 7 creatures + a numeric Gate-A** once a bestiary exists; this pass validated *structure and stacking*, which is what's actionable now.

---

## A. Part 2 — Scoundrel / Tech Specialist / Officer (2026-06-20)

The three newest classes. Bounded accuracy and role shapes hold again; the issues are the same *stacking/action-economy* category, plus the deferred **action-granting audit**.

### A.1 Officer — action-granting audit (the priority): PASSES, one fix

The test per ability: **(Officer actions spent) vs (party action-value gained)**.
- ✅ **Bonus-directives grant 0 actions** (pure buff) — the default; trivially safe and *why* the Officer force-multiplies without going action-positive. **Get Moving! / Fall Back! / One Unit** grant **movement** (Step/Stride — not a full action's combat value). **Ready Arms!** = 2 actions → 1 own Strike + 1 *contingent* ally Strike = **1:1**. **Double Time / Perfect Coordination** issue extra **Directives** (bonuses, not actions) and are gated (once/min; L20). The bonus-first design (§4.1) holds — the deferred red-flag is resolved by rule.
- 🔴 **O-1 (applied) — Overwhelming Volley** (Guns Blazing L8) let Ready Arms!'s contingent Strike come from **two** allies → 2 actions yielding 1 + 2 = **3 Strikes (1.5:1)**, reliably via Area-Fire. **The one action-positive edge.** Fixed: **one** contingent Strike (choose which of two allies takes it).

### A.2 Scoundrel — ranged-striker bracket: on-curve

- Mid single-target ≈ **+19%** over the Guardian — inside the 20% flag and **intended** (the dedicated DPR striker), paid for by **HP 8**, the **Aim setup action** (turn-one = Aim + one Strike), and precision that **precision-resistant / no-flanking foes negate**. Guardian trades the gap for active defense. Both bracket. ✅ *(Resolves Part-1's "Guardian is the DPR ceiling, re-bracket vs Scoundrel.")*
- 🟡 **S-1 (watch):** each-Strike Exploit × extra-attack feats (Double Tap, Twin Guns, Run and Gun) multiply precision instances — mirrors the PF2E Rogue (balanced by needing off-guard + MAP). Not fixing now; the spike to watch in playtest. If it over-delivers, gate Exploit to once/turn.

### A.3 Tech Specialist — engine sound; two stacking items

- ✅ **No-daily holds:** Overclock is a per-action **flat-check + lockout**, not a clock — can't nova. **Droidwright** is bounded by **§F Commanded Actors** (Tech spends an action to Command the droid ≈ 1:1; not action-positive). Skill-every-level = utility breadth.
- 🟠 **T-1 (applied) — install ceiling:** chassis 3→7 + Expanded Rig + Master Engineer + Perfect Machine = up to **10 installs** (10 always-on Standby passives). Fixed: **bonus installs capped at +2 over chassis (max 9)**; Standby passives stay minor/utility.
- 🟠 **T-2 (watch) — Overclock-safety stacking:** by L20 the safety feats (Surge Protector / Recharge / Hardened Systems / Failsafe / Overcharged Core / Perfect Machine) largely remove the Overclock risk → reliable boosts. Acceptable as a **multi-feat-investment payoff** *if* they aren't all cheap/early and the boosted Mod values stay on-curve (enforced in the per-Mod value rewrite).

### A.4 Holds (all three)

Bounded accuracy intact; no infinite loops / repeatable action-positive engines (after O-1); reaction features under the **3-cap**; no-daily model intact (per-round Directive / per-action Overclock); role shapes match the profiles (Scoundrel single-target 3, Tech utility/support 3, Officer support 3). **Gate-A now covers all seven classes** — remaining tuning is the absolute-numbers/creature pass (Phase 7) and a table playtest (esp. the soft-aggro dependency, Part-1 §4).

---

## B. Written-class watches — player-core publication pass (2026-06-21)

As each class is written to publication finish in [`docs/player-core/`](../../player-core/), a quick relative re-pass checks for drift introduced by the prose/rules-writing. **Both classes below re-confirmed all prior Gate-A fixes hold as written** (3-reaction cap honored; Soldier weapons/Class DC capped Master; Scoundrel save-expertise + Legendary-guns-only). New items are **watches**, left in by user decision (2026-06-21) — recorded here, not yet applied.

### B.1 Soldier *(content-complete in player-core: [chassis](../../player-core/classes/soldier.md) · [styles](../../player-core/classes/soldier-fighting-styles.md) · [feats](../../player-core/classes/soldier-feats.md))*

- 🟡 **B1 (watch) — Withering Onslaught hotter than spec intent.** The publication rewrite made a *success* vs Suppressing Fire take **full** damage (only a crit-success halves). Vs on-level (need-11 save) that lifts expected area damage from ≈ **0.78× → 1.03× full per target** (**+32%**), multiplied across every target in the cone — a large aggregate for one L18 feat. *Lever if it over-delivers:* dial to "a **critical** success still takes half" (distinct from the Suppressor's *Withering Hail*, which also adds a die). → ability-design.
- 🟡 **B2 (watch) — Bulwark flat-resist stack vs a suppressed attacker.** F-A2 fixed *Armored Reaction* (half-level / level-vs-suppressed), but the other layers compound at cap: Dig In (CON ≈6) + Armor Storm resist **doubled by Living Wall** (≈12) + Immovable Object (+2) = **≈20 standing** on every hit from a suppressed attacker (stationary), **plus** Armored Reaction (≈20) on the one reacted hit → **≈40**, near-negating a ~30–45 on-level Strike. Heavily conditional (stationary + suppressed + a reaction), and the Bulwark *should* be toughest — but the lever F-A2 missed is **Living Wall doubling the always-on Armor Storm resist**. *Lever if it over-delivers:* have Living Wall double only *Armored Reaction*, not the standing Armor Storm resist. → balance-analysis / class-design.
- Notes (no action): Repulsor Blast cone prone-on-fail (strong but Reflex-gated); Bullet Typhoon two area attacks/round (capstone-gated); Carpet Bomb is the only nova, `[once per minute]`, bounded.

### B.2 Scoundrel *(content-complete in player-core: [chassis](../../player-core/classes/scoundrel.md) · [specializations](../../player-core/classes/scoundrel-specializations.md) · [feats](../../player-core/classes/scoundrel-feats.md))*

- 🟡 **Sc-1 (watch) — per-Strike Exploit × MAP-frozen multi-Strike Flourishes.** Confirms Part-2 **S-1**. Exploit is per-Strike (user ruling), and several Flourishes make multiple Strikes at a **frozen MAP**: **Fan the Hammer** (3 Strikes, one adjacent target) is the ceiling — opened first, that's **three Strikes at MAP 0, each carrying the full Exploit die** (~3×4d6 ≈ **42 precision** in one action at L20, freeing two actions). Bounded by Flourish (one/round), the Mark/off-guard setup, adjacency, and precision-resistant foes, so it's a *spike*, not an engine — but the likeliest to exceed the +20% striker bracket in its best case. *Levers if it over-delivers:* **Exploit once per turn**, or **multi-Strike Flourishes apply Exploit to one Strike only**. Also clarify whether *Greater Trick Shot* (+1 die) applies to multi-Strike Flourishes (if yes, it compounds). → balance-analysis / ability-design / rules-writing (the Greater Trick Shot clarity).
- Notes (no action): capstone novas (Assassinate / Untraceable+Assassin's Mark / Perfect Shot) all `[once per minute]`, single-target, bounded; *Perfect Opening* and *One in a Million* both grant a 19–20 crit range vs the Mark — they don't stack further.

### B.3 Officer *(content-complete in player-core: [chassis](../../player-core/classes/officer.md) · [styles](../../player-core/classes/officer-leadership-styles.md) · [feats](../../player-core/classes/officer-feats.md))*

The **action-granting audit** (the priority Gate-A deferred to this class) **passes as written**: every `[Directive]` is bonus-first (status bonuses, 0 actions); bounded grants stay ≤1:1 (movement, or Ready Arms!'s one contingent Strike — **O-1 held**); mass-grants (All Guns Blazing, One Unit) are `[once per minute]` capstones, not repeatable; two-Directive feats (Double Time, Perfect Coordination) grant *bonuses, not actions*, and same-type status bonuses don't stack, so two directives = two separate buffs, never a stacked mega-buff.

- 🟡 **Of-1 (watch → rules-writing) — Tactical Reaction vs the one-Directive throttle.** Issuing a `[Directive]` as a reaction (L14) needs an explicit clause that it can't add a *third* tagged Directive in a round alongside Double Time, or the one-per-round throttle has a seam.
- 🟡 **Of-2 (watch → balance-analysis) — Suppressing Command (Guns Blazing L11) is a no-save lockdown** (off-guard + can't Step, 2 actions). Reliable single-target control with no roll; consider gating it (save vs Class DC, or "a foe an ally has Struck this round").
- Notes (no action): **Will → Legendary on a frail CHA body** is on-role (HP 8 / Fort-Expert / light armor leave Fort + Reflex as the vectors); the **L20 buff-stack** (Perfect Coordination + Greater Directives + Grand Strategy + Unify) is wide-not-deep (same-type-no-stack bounds it); once/min capstone novas (All Guns Blazing, Alpha Strike) are the gated action-value ceiling.

### B.4 Consular *(content-complete in player-core: [chassis](../../player-core/classes/consular.md) · [Mandates](../../player-core/classes/consular-mandates.md) · [feats](../../player-core/classes/consular-feats.md))*

Holds on-profile (Control-caster). The **deferred metamagic/deep-pool nova** is the watch, as expected — bounded the right way.

- 🟡 **C-1 (watch → balance-analysis) — deep pool + metamagic is the nova ceiling.** Pool 3 + Level Bonus, Center +3, plus **Greater Empower** (once-per-*round* maximize, L16), **Avatar of the Force** (once/encounter full refill), and **One with the Force** (−1 Attunement to all powers). Bounded by: no to-hit/DC inflation (maximize only kills variance), the 3-action economy, the ~4-die damage arc, and per-spike Frequencies. Watch the aggregate of Greater Empower on the highest-dice powers; confirm the dice-arc cap holds on everything empowerable.
- Notes (no action): **Legendary Class DC (L17)** is the sanctioned offensive spotlight (mirrors the Guardian's Legendary saber); the save-or-suck it powers stays honest via Incapacitation + once-per-minute + crit-fail-escalation. **At-will Telekinetic Impact** is on-curve (≈ one Strike's worth per 2 actions, below a striker's turn, no attribute on the damage). **Mandate parity** holds (temp-HP-on-heal doesn't stack). **Squishy by design** (HP 8, weak Reflex is the vector).

*(Guardian / Sentinel / Tech Specialist get the same written-class re-pass as they're brought to publication finish.)*

---

## C. The Force powers chapter — written-numbers pass (2026-06-22)

A relative re-pass on the 55 authored power entries ([the-force.md](../../player-core/the-force.md)) — checking the prose numbers against the bounded spine. **The chapter holds.**

- ✅ **Damage tracks the weapon curve.** Save powers d6 / attack & healing d8, +1 die at L5/11/17 on a {1,2,2,3,4}-base arc (≈4 dice at cap), **no attribute on Force damage** → Force damage lands at or below a weapon Strike's, buying range/area/a save instead of raw DPR.
- ✅ **Flat values stay sub-curve** — Force Barrier resist (2 + Level Bonus), Force Valor temp HP (10/15/20), Energy Absorption (2×(2 + Level Bonus)) — soak, never negate.
- ✅ **Push is always an effect, not a number** (off-guard, extra target, redirect, condition).
- ✅ **Hard control gated** — the six save-or-suck powers (Hold, Stasis, Choke, Dominate Mind, Mass Mind Trick, Mind Fracture) carry Incapacitation + once-per-minute, with crit-fail escalation that never deletes or kills.
- 🟡 **F-1 (watch → balance-analysis) — Force Destruction's 8 dice (4d6 + 4d6)** is the chapter's largest single hit, sharpened by Greater Empower. Consider whether two full dice-arcs is intended or should be one 4-die pool split across force/fire.
- 🟡 **F-2 (note) — Mind Fracture crit-fail stunned 3** is heavy action-denial; gated (L17 / 3-Att / once-per-minute / Will / crit-fail-only), acceptable at capstone tier.

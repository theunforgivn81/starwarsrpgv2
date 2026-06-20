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

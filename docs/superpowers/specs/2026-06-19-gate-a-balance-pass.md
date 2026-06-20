# Gate A — Balance Pass (four classes + shared layers)

**Status:** Done (2026-06-19). Findings + fixes below; clear fixes applied, judgment calls flagged for ratification.
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

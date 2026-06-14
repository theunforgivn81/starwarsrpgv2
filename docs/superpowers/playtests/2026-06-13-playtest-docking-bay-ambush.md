# Playtest Simulation — "Docking Bay Ambush" (Mode B smoke test)

**Date:** 2026-06-13
**Mode:** B (single-context adversarial role-play) — **smoke test, not a gate.** Escalate to Mode A before sign-off.
**Target:** the vertical slice (Phases 0–7 + remediation + Gate A numbers).
**Personas run:** Optimizer, Rules-Lawyer, Chaos, New Player (full panel).
**Method:** two-pass adjudication; every Pass-1 silence logged. *Find, don't fix.*

---

## 1. Scenario & Exact Builds

**Scene:** A cramped docking bay. The **Inquisitor** (L5 boss, saber) and **2 Stormtroopers** (L4 standard, ranged, *Squad Tactics*) corner the party near a freighter ramp; a **maintenance pit** runs along one edge of the bay. The **Scoundrel begins Hidden** (rolled Stealth for initiative, Undetected).

**PCs (L5, Gate A numbers):**
- **Vexa — Soldier** (Sharpshooter): DEX +4, CON +2. HP 68, AC 20, Perception +6. Blaster Rifle **2d8+2**, attack **+9**. *Suppressing Fire, Reactive Volley (2 reactions).*
- **Dax — Scoundrel** (Operator): DEX +4, CON +1. HP 53, AC 21, Stealth +8. Blaster pistol **1d6**, attack **+9**; **Exploit +2 precision dice** (Off-Guard/Studied target). *Vibroblade option (1d6 agile/finesse).*
- **Kira — Guardian** (Sentinel): WIS +4, DEX +3, CON +1. HP 63, AC 20. Lightsaber **2d8+3** `[finesse][deadly d8]`, attack **+8**. **Force DC 18.** Attunement pool ~4. *Deflecting Stance + Deflect mastery; Telekinetic Nudge (0 Attunement).*
- **Bex — Technician** (Field Medic): INT +4, CON +1. HP 53, AC 18. Blaster pistol attack **+6**. **Gadget DC 18.** *Drone (pre-deployed); Command Drone; Deploy Device (medbeacon/turret).*

**Adversaries:**
- **Inquisitor** L5 boss: AC 18, HP 140, saber +11 (2d8+4, deadly), **Force DC 19**. *Deflect Blaster Bolts; Boss Actions ×2/round; Phase 2 ≤70 HP (saber-throw/ranged, 2nd deflection); condition resilience; Force Shove.*
- **Stormtrooper** ×2, L4: AC 16, attack +10, blaster 1d8+? , HP ~30. *Squad Tactics (allies firing the same target gain +1 circumstance).*

---

## 2. Turn-by-Turn Log (condensed; findings flagged inline)

**Initiative:** Dax (Stealth, Undetected) 22 · Vexa 18 · Inquisitor 17 · Troopers 12 · Kira 11 · Bex 9.

### Round 1
- **Dax (Optimizer line):** Undetected → target is **Off-Guard** to him → opens with **Exploit**. Studies a Trooper (1 act), Strikes (1d6 +2 precision dice, Off-Guard): hits, ~14 dmg. Stays Hidden? He attacked from concealment → **does attacking break Hidden?** *(Pass-1: detection adopted from ORC says attacking makes you observed unless a feat says otherwise — GM rules Dax is now Observed. **F-DET log:** the slice references ORC stealth but never states the "attack ends Hidden" line in our own text — adjudicated by importing ORC. Note.)*
- **Vexa:** **Suppressing Fire** on Trooper B → hits (~14), Trooper B **Suppressed** (Off-Guard, −2 attacks; provokes Vexa's Reactive Shot on move/ranged). Spends 3rd action to reload? *(Pass-1: does the Blaster Rifle need reloading? **F-AMMO log** — ammo abstraction undefined (C2). GM rules no reload. )*
- **Inquisitor:** sees blasters incoming → **the Optimizer immediately reasons:** "the boss deflects ranged, so we should all melee it — and it's a *saber* user, so meleeing it draws **no Reactive Shot**. Free, safe, higher-damage melee." → **F1 flagged.** Inquisitor spends turn: saber Strike on Dax (nearest), **Boss Action** ×2 (on PCs' turns, below). Hits Dax ~16.
- **Troopers:** Trooper A fires at Dax (now Observed); Trooper B is Suppressed — it tries to reposition for a shot → **provokes Vexa's Reactive Shot** (Reactive Volley, 2nd reaction available): Vexa shoots it. *(Works. But Rules-Lawyer asks: "If three troopers were here and I melee one, do the **other two** Reactive Shot me? The trigger says 'a melee Strike against **you**' — only the target.")* → **F2 flagged** (firing-line intent vs target-only trigger).
- **Kira (Guardian):** wants to close on the Inquisitor and saber it. Enters **Deflecting Stance** (1 act), Strides (1 act), Strikes (1 act). Meleeing the Inquisitor (saber user, no ranged) → no Reactive Shot anyway. Hits, 2d8+3 ~12. **Then the Rules-Lawyer pivots:** "Next turn I'll just **Telekinetic Nudge** (0 Attunement, at-will) to shove the Inquisitor into the **maintenance pit** every round for free." → **F3 flagged** (at-will forced movement × undefined hazard/fall rules).
- **Bex (Technician):** Drone (pre-deployed) takes its **uncommanded basic action** (a Strike on Trooper A) — *free, no Technician action spent.* Bex then **Commands Drone** (1 act → Drone Strides + Strikes again) and **Deploys medbeacon** (2 acts). *(Optimizer notes: Bex effectively acted ~4 times this round.* → **F4 flagged** (drone is a persistent action-positive engine). *New Player asks: "does my Drone roll its own initiative / get its own turn?"* → **F5 flagged**, drone turn/initiative undefined.)*

### Round 2
- **Kira:** executes the F3 plan — **Telekinetic Nudge** on the Inquisitor toward the pit. *(Pass-1: how far does it push? "auto-scales with level" — unstated value. How does a creature at a pit edge resist? **F3/F-NUDGE:** no rule. GM improvises: Fort save vs Force DC 18 or pushed 5 ft; at the edge, a second save or fall.)* Also: **the Guardian wants to Push the Nudge** for extra distance — **Attunement cost of Push unstated.** → **F6 flagged** (Attunement/Push numbers too soft to run).
- **Vexa (Optimizer nova attempt):** 3 Strikes at the boss: +9 / +5 / +1. Computes it's better to take 2 Strikes + Suppress. *(Confirms MAP −4/−8 working — 3rd Strike not worth it. **Positive note.**)*
- **Inquisitor Phase check:** party has dropped it ~50 → not yet ≤70. **Boss Actions** used on Kira's and Vexa's turns (Force Shove Kira away from the pit — *the GM uses this as the ad-hoc answer to F1/F3, but it's improvised, not in the stat block as written*).
- **Chaos Player (Dax):** ignores the boss; **shoots the freighter's fuel line** above the troopers. *(Pass-1: no environmental/hazard rules. **F-ENV log**, expected gap. GM improvises a Reflex save / fire burst.)*
- **Bex:** an ally (Dax) is at 9 HP; Bex uses a **stimpack** on him. *(Pass-1: heal amount + the "tolerance" curve unstated. **F7 flagged** — stim potency/tolerance not runnable as written.)*

### Round 3 (abridged)
- Inquisitor hits Phase 2, throws saber (ranged) — *now a melee-PC adjacent to it could Reactive Shot it? It used a **ranged** Strike, which doesn't provoke. Fine.* Party finishes it with melee + Suppression-enabled Exploits. **Dax drops to 0** from a Boss Action saber Strike → gains **Dying 1**, recovery check DC 11 next turn (ORC dying works cleanly — **positive note**).

**Outcome:** party wins in ~3–4 rounds; no slog; tension real (one PC downed). The *engine* ran. The *gaps* below are what a real table would trip on.

---

## 3. Findings (prioritized)

| id | sev | turn | spec | class | finding & repro | routed-to |
|---|---|---|---|---|---|---|
| **F1** | **Major** | R1 Inquisitor | [Phase 7 §9](../specs/2026-06-13-phase7-creatures-and-challenge.md) | creature behaviour | **Boss anti-ranged signature backfires.** The Inquisitor *deflects blasters*, funneling PCs into melee — but he's a **saber (melee) user, so meleeing him provokes no Reactive Shot**, and melee is *deadlier*. The signature meant to pressure the party instead **removes their risk and raises their damage.** Repro: party drops ranged, safely melees the boss. Fix direction: pair deflection with a melee deterrent (AoE Force Shove as a *printed* Boss Action, lair hazard, or clustered-melee punish). | ttrpg-creature-design |
| **F2** | **Major** ✅ **RESOLVED** | R1 Troopers | [Phase 1 §11](../specs/2026-06-13-phase1-core-mechanic-and-traits.md), [remediation S5](../specs/2026-06-13-connective-tissue-and-review-remediation.md) | cross-subsystem hole | **Reactive Shot was target-only, but "don't charge a firing line" implies many shooters.** **Resolution (2026-06-13):** Reactive Shot now triggers for any perceiving gunner **within 10 ft** of a melee attacker, not just the target — delivers the firing-line fantasy; bounded by 1 reaction/round, loop-free (ranged Strikes don't provoke). Watch melee-vs-group risk in the next playtest. | ttrpg-system-review (done) |
| **F3** | **Major** ✅ **RESOLVED** | R1–R2 Kira | [Phase 5 §4.1](../specs/2026-06-13-phase5-class-design-and-force.md), [connective-tissue §G](../specs/2026-06-13-connective-tissue-and-review-remediation.md) | exploit / hole | **At-will forced movement × undefined hazard rules = free shove-off-ledge.** **Resolution (2026-06-13), three layers:** (1) **economy rule** — offensive Force costs Attunement, so Nudge is now 1 Attunement (no free spam); (2) **stop-at-edge** system-wide forced-movement rule — displacement never pushes into a fall/hazard by default; (3) the **Hurl** Push (+2) is the only off-ledge option, and it grants a basic Reflex save. | ttrpg-system-review + ttrpg-ability-design (done) |
| **F6** | **Major** ✅ **RESOLVED** | R2 Kira | [Phase 5 §2.2](../specs/2026-06-13-phase5-class-design-and-force.md) | number (blocks play) | **Attunement loop was unrunnable.** **Resolution (2026-06-13):** locked — pool `2+L`; Center (1 act) regains 2 (cap pool); powers 0/1–2/3; Push +1/+2; **Deflection & basics free of Attunement** (no defensive gas-out); no action-positive loop. Now runnable; provisional pending next playtest. | ttrpg-balance-analysis + ttrpg-ability-design (done) |
| **F7** | **Major** ✅ **RESOLVED** | R2 Bex | [Phase 6 §3](../specs/2026-06-13-phase6-equipment-and-economy.md) | number | **Stim heal + tolerance unstated.** **Resolution (2026-06-13):** grades **2d8/4d8/6d8/8d8** by tier; tolerance halves per stim on a creature per **encounter** (`÷2^(N−1)`); **stims-only** scope (per your call) — medbeacon now a deploy-burst, Vitality Attunement-costed, so heal-stacking stays bounded (**watch in next playtest**). | ttrpg-balance-analysis + ttrpg-rules-writing (done) |
| **F4** | **Minor/Note** | R1 Bex | [Phase 5 §6](../specs/2026-06-13-phase5-class-design-and-force.md) | action economy | **Drone is a persistent action-positive engine.** Uncommanded, it takes a free basic action/Aid **every round** — the Technician effectively acts ~4×. Bounded (one modest drone) and *intended* class identity, but it's the red-flag "nets positive actions repeatably"; confirm it's priced and that the uncommanded free action isn't too strong. | ttrpg-balance-analysis |
| **F5** | **Minor** | R1 Bex | [Phase 5 §6](../specs/2026-06-13-phase5-class-design-and-force.md) | ambiguous text | **Drone turn/initiative/reaction undefined.** Does it act only on the Technician's turn, roll its own initiative, have its own reaction? New Player stalled. Fix: state the companion's action/initiative rules. | ttrpg-rules-writing + ttrpg-ability-design |
| **F-DET** | **Minor** | R1 Dax | [remediation S1](../specs/2026-06-13-connective-tissue-and-review-remediation.md) | ambiguous text | "Attack ends Hidden/Undetected" is **imported from ORC but not stated in our own text.** Players relying on our docs won't know strikes reveal them. Fix: state the reveal-on-attack line explicitly. | ttrpg-rules-writing |
| **F8** | **Minor** | R1 | [remediation S5](../specs/2026-06-13-connective-tissue-and-review-remediation.md) | edge case | If a **Reactive Shot drops the attacker** (to 0/Dying), is the triggering melee Strike lost? Implied "disrupt," not stated. Fix: one line. | ttrpg-rules-writing |
| **F-AMMO** | **Minor** | R1 Vexa | [Phase 6](../specs/2026-06-13-phase6-equipment-and-economy.md) | hole (C2) | Blaster **ammo/reload** abstraction undefined (already parked as C2; confirmed it surfaces in play turn 1). | ttrpg-equipment-design |
| **F-ENV** | **Note** | R2 Dax | — | expected gap | **Environmental interactions** (shoot the fuel line, hazards) undefined — known deferral (Phase 8); GM improvises. | ttrpg-system-review |

**Positive confirmations (no defect):** MAP −4/−8 correctly deters the 3rd Strike; Suppressed→Off-Guard→Exploit synergy lands as intended; ORC dying/recovery runs cleanly; the pre-deployed Drone gives round-1 value as designed; bounded-accuracy hit/crit feel correct in sequence.

---

## 4. Headline

No **Critical** (no infinite loop / unbounded nova / blocked play). But **four Majors** a real table would hit immediately:
- **F1** the boss's signature *helps* the party — a creature-design own-goal that static review and math both missed because it only emerges when the Optimizer reasons about it in sequence.
- **F3** an at-will forced-movement exploit against undefined hazard rules.
- **F6 / F7** two of the "soft numbers" (Attunement, stims) are not just imprecise — they're **unrunnable**, which blocks play, not just balance.
- **F2** the melee-risk fantasy doesn't fully deliver vs grouped gunners.

**Recommendation:** route F1–F7 to their skills and resolve **F6/F7 (unrunnable numbers) and F3 (exploit)** before any Mode A gate or live table. This is a smoke test — a Mode A run (blind player agents) should follow once these are addressed.

# Playtest Simulation — "Docking Bay Ambush" (Mode A gate run)

**Date:** 2026-06-14
**Mode:** A (subagent table — information asymmetry). GM subagent had the full specs; four player subagents got **only** their character sheet + a player-facing primer + their hunter persona, **blind** to designer intent and to each other. Conductor relayed turns.
**Target:** the post-fix vertical slice (Phases 0–7 + remediation + Gate A + skill-actions + rank-effects), validating that the Mode-B fixes (F1–F7) hold under blind adversarial play.
**Scope run:** 2 full rounds (concluded before Phase 2 / endgame — see §Untested).
**Method:** two-pass GM adjudication; every rules-as-written gap logged. *Find, don't fix.*

---

## 1. Scenario & Builds

**Scene:** "Docking Bay Ambush" — a ~40-ft bay; boarding ramp at the party edge; a deep **maintenance pit** along the far-left edge; cargo crates mid-room for cover. Party vs **Inquisitor** (revised L5 boss) + **2 Stormtroopers** (L4). Dax began **Hidden** (Stealth-for-initiative).

**PCs (L5):** Vexa (Soldier/Sharpshooter — **Optimizer**), Dax (Scoundrel/Operator — **Rules-Lawyer**), Kira (Guardian/Sentinel — **Chaos**), Bex (Technician/Field-Medic — **New Player**). Stats per the Mode A spawn briefs (reproducible in the orchestration log).

**Initiative:** Dax 26 · Inquisitor 23 · Kira 21 · Trooper A 17 · Vexa 16 · Trooper B 14 · Bex 11.

---

## 2. Condensed Session Log

**Round 1.** Dax (Undetected) Studied + crit the Inquisitor from stealth (24 dmg → **Deflect reduced to 14**); ruled **Observed** after attacking. Inquisitor armed **Force Repulse** (telegraph) and Strided into ~13 ft of the ramp cluster. Kira tried to **Hurl the boss into the pit** — geometry denied it (boss center-room) and she burned 3 Attunement for nothing (declaration-timing dead turn). Vexa Suppressed Trooper A + hit B; troopers fired on Kira (Squad Tactics). End R1: Inq 126, troopers wounded, Repulse armed.

**Round 2 (climax).** Dax dumped 3 pistol Strikes into the boss to "race the wind-up" — **Deflect (−10) reduced two hits to a total of 4 damage** (anti-ranged signature working *too* hard). **Force Repulse detonated** on the semi-cluster (Kira/Vexa/Bex/Dax all caught): 26 total damage, party pushed away — **but the burst scattered the boss's own melee targets**, re-opening saber range. Kira put up **Deflecting Stance**, then **Hurled** the now-adjacent boss toward the pit — boss **failed Fort but made the Reflex save → stopped at the brink** (the §G anti-instakill working). Trooper A, **Suppressed**, took a ranged Strike → **Vexa's held Reactive Shot killed it before its shot resolved**; Vexa then killed Trooper B. End R2: **both adds dead**, Inquisitor 107/140 (Phase 1), Repulse on cooldown, pinned at the pit brink next to a 26-HP Kira — **now a lone boss vs 4 PCs.**

---

## 3. Findings

`id · severity · where · class · finding / repro · routed-to`

### Major
- **MA1 — Deflect Blaster Bolts: magnitude undefined AND the working value breaks low-die ranged.** The boss signature has no stated reduction (Gate A). The GM's "reduce 10" made the boss **functionally immune** to pistols/drone (1d6±precision → 0–3 dmg; the drone's 1d6 was a *guaranteed* 0) while a 2d8 rifle still leaks ~3/hit. Flat reduction is too swingy across weapon die sizes. Repro: Dax's full 3-Strike turn dealt **4 total**. Fix: stat the value as **non-flat** (halve damage, or small flat + cap) so it pressures ranged without deleting the pistol/drone archetype. → **ttrpg-balance-analysis + ttrpg-creature-design**
- **MA2 — R-SELFSCATTER: the Inquisitor's anti-cluster AoE undoes its own melee approach.** The F1 redesign paired Deflect (funnel to melee) + Force Repulse (punish the cluster) — but the Inquisitor is *itself* a melee attacker, so after it Strides in, its own Repulse **pushes its prey out of saber range**, costing it tempo. Sig A and Sig B fight each other on the same body. Repro: R2 — boss closed R1, Repulsed R2, then had to re-Stride to reach anyone. Fix: make Repulse a **pull**, or a *ranged-stance* tool, or have the boss hold range and let the party come (telegraph while staying back); reconcile the two signatures' positioning logic. → **ttrpg-creature-design**
- **MA3 — Solo-boss action economy (the §9 warning made real).** Both adds died by end of R2 (Squad Tactics never triggered meaningfully; Suppression + Reactive Volley + focus fire dismantled them), leaving the boss alone vs 4 PCs at full action parity with Repulse on a once/min cooldown. The Inquisitor's 2 Boss Actions may be insufficient once adds collapse. Repro: 2 standard L4 adds vs an optimized L5 party lasted <2 rounds. Fix: tougher/more numerous adds, **wave reinforcements**, or more boss durability/Boss-Actions; honor §9 "don't run it truly solo" with encounter-budget guidance. → **ttrpg-creature-design + ttrpg-balance-analysis**

### Minor
- **MN1 — Undetected→Observed transition not in our text** (confirms Mode-B F-DET; the Rules-Lawyer exploited it). State "attacking reveals you" in our own rules. → ttrpg-rules-writing / system-review
- **MN2 — Telegraphed-AoE-if-caster-dies (R-DEADBOSS) undefined.** Ruled no-caster-no-burst. State it. → ttrpg-rules-writing
- **MN3 — "Disrupt the wind-up" (R-DISRUPT) has no mechanic.** Spec names it as counterplay but defines no interrupt; ruled only incapacitation cancels. Define or reword. → ttrpg-rules-writing / creature-design
- **MN4 — Forced-movement direction default unstated (G-DIRECTION).** §G says "distance and direction" but not who chooses. Ruled per-power. Add a default. → ttrpg-rules-writing
- **MN5 — Nudge+Hurl is a hidden double-gate** (fail Fort *then* fail Reflex). Likely intended anti-instakill, but undocumented. Note it. → ttrpg-ability-design / rules-writing
- **MN6 — Reactive Shot triggers on melee STRIKE, not movement** — Optimizer misread it as triggering on a Stride. Clarify in player-facing text. → ttrpg-rules-writing
- **MN7 — "Struck" (Squad Tactics) = attacked vs hit?** Ambiguous wording. → ttrpg-rules-writing
- **MN8 — PC and boss SAVE numbers absent** (sheets list only attacks/DC; the Inquisitor's "saves high" is unstatted). Saves drove every Repulse outcome via GM estimates. Stat them; the Phase 7 §9 showcase needs full save lines. → ttrpg-creature-design / character-sheet
- **MN9 — Speed & weapon ranges missing from player-facing sheets; blaster pistol range inconsistent** (Phase 6 implied 60, GM ruled 30). Pin pistol/drone increments; put Speed+ranges on the sheet. → ttrpg-equipment-design / rules-writing
- **MN10 — Telegraph timing phrasing confuses new players** (B-TELEGRAPH). Reword to "immediately when its turn begins, before it acts." → ttrpg-rules-writing
- **MN11 — Deploy Device: temp-HP duration & placement range undefined** (B-TEMPHP, B-DEPLOY). Stat them (ruled persist-to-encounter-end / adjacent-or-short-throw). → ttrpg-ability-design / Gate A
- **MN12 — Push/Hurl Attunement cost findability** (K-NUDGE-COST): it *is* in Phase 5 §4.1 (+2), but the GM couldn't find it from §G. Consolidate cross-refs. → ttrpg-rules-writing
- **MN13 — Attunement max = pool (4) should be on the sheet** (K-CENTER-CAP). Clarity; resolved by spec. → rules-writing

### Notes — positive confirmations & method caveats
- **F2 held:** the within-10-ft Reactive Shot functioned (killed Trooper A on its own turn); the Optimizer *learned* the trigger after a R1 misread. ✓
- **F3 held (tested 3 ways):** the pit-cheese failed appropriately every angle — geometry, the 3-Attunement Hurl cost, the fail-Fort-and-make-Reflex gate, and stop-at-edge. The Chaos player *tried hard* and the boss stopped at the brink. ✓
- **F4 held:** drone economy confirmed correct (1 action → 2 drone actions, none free); the New Player's "is this cheating?" worry was unfounded — but signals the sheet should *say* so. ✓
- **Suppression lock** is strong but bounded/non-looping (a Suppressed mook is damned either way) — working as designed.
- **Method caveat:** Kira's R1 dead turn and Vexa's pre-roll retarget are partly artifacts of **parallel full-round declaration** (the conductor's efficiency choice); a stricter sequential conduct would reduce these. Not game defects.

---

## 4. Untested (recommend a focused follow-up)
- **Phase-2 mode flip** — the centerpiece of the F1 redesign (boss wields the saber as a *ranged* weapon ≤70 HP, so meleeing it then provokes its Reactive Shot). The boss never dropped below 107, so the flip was **not exercised.** Recommend a scenario starting the boss near the threshold.
- **Solo-boss endgame swarm (R3+)** — directly tied to MA3; run the lone-boss phase to see if it survives action parity.

---

## 5. Verdict

**No Critical issues; the F1–F7 fixes hold under blind adversarial play.** The gate's real yield is three **Major** findings prior passes missed — **MA1** (the deflect value is both undefined *and* breaks low-die ranged), **MA2** (the boss's two signatures are tactically self-interfering), and **MA3** (the adds collapse, exposing the solo-boss economy) — plus a tidy stack of undefined-number and rules-writing/presentation **Minors** that are mostly the *expected* Gate-A/rules-writing backlog. The information asymmetry worked exactly as intended: the blind Optimizer misread a trigger, the blind Rules-Lawyer pried two genuine ambiguities, and the blind Chaos player confirmed the F3 fix from three angles.

---

## 6. Scope Resolution (post-run decision, 2026-06-15)

Project scope is the **rules system**, not a polished bestiary or an AI gamemaster. Findings re-triaged accordingly:

- **MA1–MA3 → content / test-fixture (DEFERRED).** These are about the *Inquisitor stat block* and how an AI ran it (deflect value, the two-signatures-self-interfere tactics, weak adds) — encounter tuning a human GM handles, not rules-engine defects. The Inquisitor was scaffolding. Revisit in a future bestiary/encounter-budget pass; not tracked as system bugs.
- **Bucket "inherited" (e.g., Undetected→Observed on attack, Take Cover, dying specifics) → NON-ISSUES.** Covered by the ORC stealth/dying/initiative we adopted; the AI only flagged them because they weren't restated locally. We document deviations and novelties, not the whole ORC corpus.
- **Bucket-3 (our novel rules) → RESOLVED / SKIPPED:**
  - **Forced-movement direction** — RESOLVED: the **source** chooses direction unless an ability specifies (per-ability balance lever). (§G updated.)
  - **Reactive Shot** — RESOLVED: explicitly triggers on a melee **Strike**, not movement; the **"disrupt" concept is removed** (normal reaction timing + incapacitation suffice). (§11 and S5 updated; Force Repulse counterplay reworded.)
  - **Push/Hurl cost findability** — SKIPPED: that Force power is slated for rework; not worth consolidating now.
  - The number/stat Minors (boss & PC saves, temp-HP, deploy range, weapon ranges, sheet presentation) → **Gate-A / content / character-sheet** backlog, not system-rules defects.

**Net:** the gate validated the engine and the F1–F7 fixes; two genuine novel-rule clarifications were folded in; the remainder is content/Gate-A backlog. The **Phase-2 mode flip remains unexercised** — worth a targeted future run, but not blocking.

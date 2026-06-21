# Playtest (Mode A) — "Open-Field Strike": L8 four-class party vs mixed squad

**Date:** 2026-06-21 · **Mode:** A (subagent table, information-asymmetric) · **Type:** milestone gate (high-fidelity).
**Method:** 1 GM subagent with full specs + intent; 4 player subagents each given **only** their own sheet + persona + a fun-test, blind to designer intent and to each other. Players declared Round 1 blind; the GM resolved the full fight adversarially (playing both sides) to conclusion.
**This is the first run of the revised skill's [Fun Audit](../specs/2026-06-13-playtest-simulation-skill-design.md) — it earned its place (see §4).**
**Find, don't fix** — no specs edited; every finding routed to a fix skill.

---

## 1. Scenario & builds (reproducible)

**Party (L8)** — tank + leader + caster + striker; three of four at HP 72 to stress protect-the-squishy:
- **Kira — Guardian / Shien-Djem So** (STR). AC 27, HP 96, reach **5 ft**. Saber +18, 2d8+6. Stance (+2 dmg, Riposte), **Intercede** (−10 + 4 reflected + self +2), **Deflect**, **Guardian's Reach**, **Vigilant Guard** (2 reactions), Force Push. Fort/Will Master.
- **Tev — Officer / Guns Blazing** (CHA). AC 24, HP 72. Blaster +14. One Directive/round; First Blood. Class DC 19. Will Master.
- **Soren — Consular / Mandate of Dominance** (CHA). AC 22, HP 72. Telekinetic Impact (at-will), pool 6 + Center, Force Push/Hold/Mind Trick/Fear. Will Master, Reflex weak.
- **Jax — Scoundrel / Gunslinger** (DEX). AC 25, HP 72. Gun +18 agile, 1d10+5. Aim/Mark, **Exploit +2d6 per-Strike**, Trick Shot. Reflex Master.

**Encounter (moderate–severe, run to win, focus the squishy):** **Brute** L10 (AC 28, HP 180, axe +22/2d12+10) · **2× Trooper** L7 (AC 25, HP 60, blaster +16, focus-fire Soren from cover) · **Skirmisher** L8 (AC 27, HP 70, Speed 40, blade +18, Acro +18 — *bypass the tank to reach Soren*).
**Terrain:** open field; only cover is contested crates at midfield (~25 ft). Initiative interleaved so the Skirmisher acts before the Guardian.

**Designer rulings applied mid-run:** Exploit is **per-Strike**; Trick Shot **split into three 1-action options** (Disarm / Ricochet / Off-Guard Shot); Tumble Through uses **Class DC**; stub rules → GM rules ad-hoc and logs.

---

## 2. Condensed session log

**R1.** Tev opens **Get-the-Job-Done + Lead by Example** on the Brute (party +1 hit/+1 dmg vs it; whiffs his own Strikes). **Skirmisher (Speed 40) simply paths *around* Kira's 5-ft bubble** — never enters reach, so **Guardian's Reach never triggers** — and reaches Soren, hits for 14; **Kira Intercedes** (→4). Jax Aims+Strikes the Brute (one hit, 23, Exploit). Brute charges **Kira**, lands 28+23 (Kira 96→45), whiffs the 3rd → **Kira Riposte** (19). Kira enters Stance, burns the Brute (Brute →96). Troopers tunnel Soren from cover; **Kira out of reactions** for the 2nd trooper. End R1: Kira 45, **Soren 40**, Brute 96, Skirmisher 66.

**R2.** Tev pivots **Get-the-Job-Done** onto the Skirmisher. Skirmisher full-attacks Soren; **Kira Intercedes twice** (Soren clings, 40→31). **Jax Aims the Skirmisher → 2× Exploit → kills it.** Brute hammers Kira (45→13) but **whiffs twice into two Ripostes (~42 free dmg)** — Brute →54, then Kira →31. Troopers keep on Soren; he reaches a midfield crate for **greater cover** but ends R2 at **1 HP**.

**R3.** Tev + Jax delete the Brute (Jax Exploit crit-burst). Kira (13) advances on the troopers to pull heat — **which moves her >15 ft from Soren, out of Intercede range.** Trooper drops **Soren (dying)**. Trooper-B then drops **Kira (dying)**. End R3: both front and caster down; Tev & Jax untouched.

**R4–R5.** Tev + Jax (full HP, full actions) mop up both troopers. **Party wins — but lost its tank and its caster.**

---

## 3. Findings

`id · severity · round · failure class · routed-to` — full repro in §2 / the GM transcript.

### Major

- **MA1 · Major · R1 · the tank structurally fails to tank · ttrpg-class-design (+ creature/encounter).** A 5-ft-reach Guardian **cannot zone open terrain.** **Guardian's Reach triggers only when a foe *leaves* a square in reach** — so a faster foe paths *around* the 5-ft bubble, never enters it, and the reaction never fires. **This reopens Mode-B [F2](2026-06-20-playtest-modeB-mixed-party.md), which "resolved" melee zoning with Guardian's Reach** under charitable Mode-B play that assumed the foe moved *through* the threatened square. **Mode A (adversarial) shows the fix is necessary-but-insufficient: it works in chokes/corridors, not open field.** The Guardian needs a real zoning tool (extended threatened area, a soft-taunt/"demand attention" pull, or reach) — *or* the design must commit to "a lone tank can't cover open ground; that's what the Soldier / terrain / positioning are for" and say so loudly. **Headline finding.**
- **MA2 · Major · R1–R2 · Intercede is the only thing making the tank work, and it's a net-positive reaction · ttrpg-balance-analysis.** One reaction = ~−10 damage **+** 4 to the attacker **+** Kira +2 to-hit, with a **15-ft range** and **no per-round/per-target cap** (usable twice/round via Vigilant Guard). It "tanks" the backline that the Guardian physically can't reach. Strong, and load-bearing — propped Soren up across two rounds. (Cf. Gate-A F-A5, noted-left-as-is; Mode A says revisit.)
- **MA3 · Major · R2 · Riposte self-fuels vs multi-attackers · ttrpg-balance-analysis.** Every enemy *miss* yields a free **full-accuracy** Strike. The Brute fed Kira ~42 damage in one turn by attacking her. The more a foe swings, the more free Strikes it grants — action-economy positive and self-amplifying.
- **MA4 · Major · all · forced-movement-into-objects/creatures + shovable/destructible terrain have no rules teeth · ttrpg-system-review.** Every "push into a crate," "collide two enemies," "knock cover into an obstacle," and the Mandate +5 ft stacking required ad-hoc GM rulings. Terrain is decorative. (This is the **Chaos persona's** core fun failure — see §4.)
- **MA5 · Major · R1/R3 · no range / range-increment handling for Force powers · ttrpg-system-review.** Soren's declared Push was simply out of range with no graceful penalty path; the GM had to redirect his whole turn.
- **MA6 · Major · R3+ · no death/dying/stabilize and no coup-de-grâce rules in the specs · ttrpg-system-review.** Downing PCs and enemies "confirming kills" both required improvisation and **directly affected the outcome** (whether Soren/Kira could be finished).
- **MA7 · Major · R1 · Tumble-Through DC contradiction · ttrpg-rules-writing.** Skill table = Reflex DC; Guardian spec = Class DC. (Also: **Kira's Class DC is never printed** — MA15.)
- **MA8 · Major · all · Officer directive dominance · ttrpg-ability-design.** *Get-the-Job-Done + Lead by Example* was the near-auto-correct pick every round (own Strike + party to-hit + party dmg + buffs reactions). Other directives rarely competed.

### Minor / Note

- **MA9 · Minor · DPR · Exploit-per-Strike ≈ +18 dmg/turn from one Aim · ttrpg-balance-analysis (watch).** Confirmed designer intent (per-Strike); flag the number, not a bug. Also flattens Jax's decisions (the Aim→2×Exploit loop is always optimal). Cf. Gate-A **S-1**.
- **MA10 · Minor · R1 · "when hit by melee → +2 next attack" doesn't bank if the hit lands before Stance is entered · ttrpg-rules-writing.** Turn-order feels-bad.
- **MA11 · Minor · R1 · Vigilant Guard (2 reactions) vs system cap (3) — which governs? · ttrpg-rules-writing.** (They're compatible — grant vs ceiling — but the text should say so.)
- **MA12 · Minor · R1 · Consular Force Push has no success/damage line · ttrpg-rules-writing.** "Basic save" implies a damage-on-success path that isn't written.
- **MA13 · Minor · R3 · Force Push (DC 19) vs on-level Fort (+14) fails only on ≤4 · ttrpg-balance-analysis.** Single-target soft control is unreliable for a 2-action spend vs on-level foes.
- **MA14 · Note · R1 · no cover at the party's default start · ttrpg-creature-design.** Only contested midfield crates; defensive positioning forces movement toward the enemy.
- **MA15 · Note · — · Kira's Class DC not printed · ttrpg-rules-writing.** Needed for Tumble Through and other DC interactions; GM inferred 27.

---

## 4. Fun Audit (per persona — the new pass)

Judged against each persona's observable fun-test, as a separate pass from the failure-hunt.

| Persona | Fun read | Verdict |
|---|---|---|
| **Optimizer** (Kira/Jax) | ≥2 viable lines most turns (kill-skirmisher vs burn-Brute; DPS vs hold reactions) and mastery moved outcomes — **but** Jax's Aim→2×Exploit is the same solved loop every turn. | **PASS** (one flat spot, MA9) |
| **Rules-Lawyer** (Tev) | The R1 directive win was a genuine *legal* payoff — but the slice's other cool combos (shove-into-crate, collide, Intercede-reach-tanking, Tumble timing) all needed GM rulings, two of them contradictory/undefined. | **FAIL** (MA4/5/7/12) |
| **Chaos** (Soren) | The signature move — weaponize the crates/environment/forced movement — hit "no rules teeth" and got hand-waved, not a supported "yes, and." Terrain is decorative. | **FAIL** (MA4) |
| **New Player** (Jax/Soren) | Martial turns resolved in ≤3 decisions and felt impactful; **but** Soren's caster turn was a dead, confusing whiff (out-of-range push, riders that don't exist, resisted save → "I felt useless"). | **MIXED** (MA5/13) |

**Fun severity:** the Rules-Lawyer and Chaos failures **recur across turns** (terrain/forced-movement undefined everywhere) → **Major** fun findings, folded into MA4/MA5. Soren's no-payoff turn is **Minor** (watch caster reliability vs on-level saves).

**Meta — the Fun Audit validated itself:** it surfaced two Major problems a pure exploit-hunt would have shrugged off — *"the system won't let me be creative with terrain"* (Chaos) and *"the caster's turn had no payoff"* (New Player). Those aren't exploits; they're fun failures, invisible without the new pass. The observable per-persona tests (vs vibes) made the FAIL verdicts defensible, not charitable.

---

## 5. Triage summary

- **Critical:** none (play completed; no infinite/degenerate engine — though MA2/MA3 are net-positive reactions to quantify).
- **Major — class identity:** **MA1** (tank can't zone open field; Guardian's Reach insufficient — *reopens Mode-B F2*) → **ttrpg-class-design**. **MA8** (directive dominance) → **ttrpg-ability-design**.
- **Major — balance/action-economy:** **MA2** (Intercede), **MA3** (Riposte) → **ttrpg-balance-analysis** (quantify the net-positive reactions).
- **Major — missing subsystems (the big hole):** **MA4** (forced movement + destructible/shovable terrain), **MA5** (power range), **MA6** (death/dying + coup) → **ttrpg-system-review** then **ttrpg-rules-writing**. These touched the outcome and broke fun for two personas.
- **Major — text:** **MA7** (Tumble DC contradiction) → **ttrpg-rules-writing**.
- **Minor/Note:** MA9–MA15 → balance-watch + rules-writing clarifications.

**Bottom line.** Offense is in a great place — focus-fire + Exploit-per-Strike + Riposte melted a 180-HP Brute in ~2.5 rounds. The **defensive and control sides are where the system bleeds:** the defender archetype structurally failed to defend (MA1), staying afloat only on net-positive reaction rulings (MA2/MA3); and the **missing forced-movement/terrain, range, and death subsystems** (MA4/5/6) repeatedly forced improvisation and killed Chaos/Rules-Lawyer fun. Mode A's adversarial, information-asymmetric play found the open-field bypass that Mode B's charitable play papered over — exactly the gate's purpose.

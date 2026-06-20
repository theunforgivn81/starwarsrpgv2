# Playtest (Mode B) — Mixed L8 party vs ranged-heavy strike team

**Date:** 2026-06-20 · **Mode:** B (single-context, adversarial roster) · **Type:** smoke test (not a gate — escalate to Mode A for a milestone).
**Goal:** smoke out glaring issues in the seven-class system. Priorities: the **soft-aggro/tank dependency**, **action-economy at the table** (Officer Directives, reaction-heavy turns), and **turn variety** (no "Strike ×3").
**Find, don't fix** — every finding is routed to a fix skill; no design edited here.

---

## 1. Scenario & builds (reproducible)

**Party (L8), built per the specs** — deliberately tank + striker + caster + support, **three of them HP 8** (to stress the protect-the-squishy question):
- **Guardian / Soresu** (STR) — bodyguard tank. Medium armor + Soresu (+2 AC vs ranged); HP ~96. **Intercede** (reduce ally damage 2+L = 10), **Deflect** (mastered), **Vigilant Guard** (2 reactions for Deflect/Intercede). Saber Expert.
- **Scoundrel / Sniper** (DEX) — ranged striker. HP ~72. Guns Master; **Aim** (Mark at any range), **Exploit 2d6**.
- **Consular / Mandate of Telekinesis** (CHA) — controller-caster. HP ~72; light armor (lowest AC). Attunement pool **6** (3+L), Center +3; Telekinetic Impact (at-will), Force Push/Hold; Class DC ~19.
- **Officer / From the Front** (CHA) — leader. HP ~72. **Get-the-Job-Done**, **Into Position!**, **Form Up!**; the L1 bonus Directive feat → **Take Cover!**.

**Encounter (moderate–severe):** **1 Brute** (Lvl 10 elite, melee, ~21/hit, big HP) + **3 Blaster Troopers** (Lvl 7, ranged ~8/hit). The troopers are the soft-aggro stress: *ranged* enemies can ignore a melee tank and shoot the casters.

---

## 2. Condensed session log

**R1.** Scoundrel (high init) **Aims** the Brute, snipes (Exploit) — 1 action setup + 1 Strike + Step to cover (not "Strike ×3" ✔). Officer issues **Get-the-Job-Done** on the Brute (party +1 status attacks) + Strides up (Lead by Example). Consular **Force Push**es a Trooper back + Telekinetic Impact. Guardian enters **Soresu**, Strikes the Brute, **holds 2 reactions**.
- **Enemy turn:** Brute charges — *walks past the Guardian* toward the Consular (no opportunity attack exists to stop it — F2), Strikes Consular for 21; Guardian **Intercedes** (−10 → 11 taken). **3 Troopers ignore the Guardian entirely** and shoot the Consular/Scoundrel (F1); Guardian **Intercedes** a 2nd shot (its last reaction); the other 2 shots land (~16 total on the squishies). End R1: Consular ~45/72, taking fire from turn one.

**R2.** Officer **Take Cover!** (allies to cover, +circ AC vs ranged) — *finally blunts the troopers*. Consular **Force Hold**s the Brute (Class DC vs Fort) — Brute slowed. Scoundrel snipes the held Brute. Guardian Strikes + holds reactions.
- **Enemy turn:** Troopers (now in cover-fight) miss more; Brute (slowed) still swings at Consular; Guardian Intercedes. Casters holding.

**R3.** Focus-fire: Officer Get-the-Job-Done + Scoundrel Mark on the Brute (bonuses stack — different types, F5); Consular Kinetic burst. Brute drops. Troopers waver.

**Outcome:** party wins ~R4; the **Consular dipped to ~⅓ HP** because it ate focused fire **R1 before Take Cover!/positioning came online**. Survivable, but the squishy was the clear target and the *single melee tank could not prevent it* — only mitigate.

---

## 3. Findings

`id · severity · turn · failure class · routed-to`

- **F1 · Major → CONFIRMED INTENDED (2026-06-20) · R1 · anti-ranged tank gap.** Vs **ranged** enemies, the Guardian's **Lever-A (be a melee threat) does nothing** — troopers shoot past it at the HP-8 casters; protection collapses to reaction-limited Intercede. **Ruling: working as designed.** The Guardian actively prevents ally damage only at **close range** and draws fire by *being a melee threat* — the worst-case scenario here *deliberately bypassed* that by going ranged-heavy with no Soldier. **Guardian = melee tank; Soldier (Suppression) = ranged tank — not interchangeable.** *Remaining carried-forward (not a fix):* make **cover rules prominent** and add **encounter/GM guidance** on the two-tank coverage so the table understands it. → creature-design (encounter guidance) + rules-writing (cover).
- **F2 · Major → RESOLVED (2026-06-20) · R1 · melee zoning.** The Brute walked past the Guardian with no consequence (no universal AoO — the Reactive-Shot genre-flip). **Fix applied:** added **Guardian's Reach** ([class-guardian §4.2](../specs/2026-06-18-class-guardian.md)) — a class-specific `[reaction]` melee Strike when a foe **leaves the Guardian's reach** (soft zoning: the move still happens, but it pays; Tumble Through is the counterplay). Recorded in [Phase 1 §4.3](../specs/2026-06-13-phase1-core-mechanic-and-traits.md) as the deliberate exception to "no universal opportunity attack," and **subclass-enhanceable** (Djem So damage, Makashi Disarm, Soresu push, Ataru reposition) — the design hook the user wanted.
- **F3 · Minor · R1 · Intercede timing wording · rules-writing.** Pass-1 gaps: does Intercede's flat reduction apply **per damage instance**? **before or after** a crit's doubling? can it reduce an **area** effect's damage to one ally? Text says "reduce the damage the ally takes by 2+level" — needs an explicit timing/scope line.
- **F4 · Minor · R2 · Directive edge cases · rules-writing.** "allies who can sense you" + duration/refresh: what if the Officer is blinded/silenced mid-round? do two Officers' identical status bonuses stack (no — same type, but state it)? does re-issuing the same Directive refresh or waste? Clarify.
- **F5 · Minor · R3 · focus-fire bonus stacking · balance-analysis (watch).** Officer *Get-the-Job-Done* (+1 status attack) + Scoundrel *Mark* (precision) + Consular control on one foe = strong, **legal** stacking (different bonus types). Intended teamwork, but watch the aggregate vs single-target bosses (it's how the party melts the Brute by R3).
- **F6 · Minor · R1 · Deflect scope · rules-writing.** "ranged energy attack" — does **Deflect** cover slug-throwers/kinetic ranged, thrown weapons, or only energy (blasters)? Affects how much the Guardian can self-protect vs different ranged types.
- **N1 · Note · reaction-economy table load.** Guardian (2) + Officer *Heads Up!*/*Take Cover!* = several interrupts on each enemy turn. Within the 3-cap per character, but a 4-PC table with held reactions slows enemy turns — watch pacing in larger fights.
- **N2 · Note · turn variety holds ✔.** No dead turns. Each class had a distinct, non-"Strike ×3" turn: Guardian (stance → Strike → hold reactions), Scoundrel (Aim → snipe → reposition), Consular (Manifest control + at-will), Officer (Directive + Lead-by-Example). The core design promise survives contact.
- **N3 · Note · the dependency is real but functional.** HP-8 casters **survived with teamwork** (Intercede + Take Cover! + positioning + control). The system works *as a unit*; it punishes a party that can't answer ranged focus-fire (no Soldier, slow to take cover) — which is the intended cost of party composition.

---

## 4. Triage summary

- **Critical:** none. (No broken/blocking play; no degenerate engine — Gate-A already closed the O-1 action-positive edge.)
- **Major (ruled 2026-06-20):** F1 → **confirmed intended** (Guardian = melee tank, Soldier = ranged tank; worst-case deliberately bypassed the threat-draw). Carried forward: cover rules + encounter guidance. F2 → **resolved** by adding **Guardian's Reach** (class-specific reactive melee Strike on movement-out; subclass-enhanceable).
- **Minor (text):** F3/F4/F6 → **rules-writing** (Intercede timing, Directive sensing/stacking, Deflect scope). F5 → **balance-analysis** watch.
- **Headline:** the **soft-aggro dependency the Gate-A pass flagged is confirmed and *threat-type-dependent*** — melee tanks (Guardian) don't pull or stop *ranged* attackers, so protecting HP-8 casters vs a ranged strike team leans on the **Soldier (suppression)**, the **Officer (cover/warnings)**, **positioning/cover**, and **control** — not on the Guardian alone. Functional, but the table must understand it (an encounter/GM-guidance + party-comp note), and it argues for **cover rules being prominent and a clear "two tanks cover two threat types" framing.** Turn variety and the action-economy guardrails both held.

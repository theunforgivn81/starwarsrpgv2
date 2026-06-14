# Gate A — Balance Validation & Benchmark Numbers

**Status:** Approved (slice passes Gate A)
**Date:** 2026-06-13
**Type:** Milestone validation gate (`ttrpg-balance-analysis`) — pins the deferred `(Gate A)` numbers and validates the dials.
**Upstream:** all Phase 0–7 specs + the [connective-tissue remediation](2026-06-13-connective-tissue-and-review-remediation.md).
**Verdict:** **the vertical slice passes Gate A.** All dials land inside bracket; one content directive (rank-gated effects, §6) is required before/with playtest.

> These numbers **supersede** the provisional `(Gate A)` values scattered through Phases 1–7. Hard-validated numbers are marked ✔; soft numbers (effect-dependent) are marked ~ and tuned in playtest.

---

## 1. Pinned Parameters

| Parameter | Value |
|---|---|
| **Attribute schedule** | key +3 at creation; +1 at L5/10/15/20 (4-attribute boost events); cap +6 → key = +3 (L1–4), +4 (L5–9), +5 (L10–14), +6 (L15+) |
| **Rank value (R)** | +1 per rank (untrained 0 → legendary 4) — **kept** (§6) ✔ |
| **DC ladder** | Trivial 8 · Easy 11 · **Moderate 14** · Hard 18 · Severe 22 · Extreme 26 ✔ |
| **MAP** | **−4 / −8** (agile −3 / −6) ✔ |
| **Weapon specialization** (flat dmg by weapon rank) | trained +0 · expert +2 · master +4 · legendary +6 ✔ |
| **Weapon damage dice** (via mods) | +1 die at Tier II (~L5), +1 per tier after |
| **Item potency** | +1 at ~L4, +2 ~L10, +3 ~L16 (optional, not baked) |
| **Armor (light/med/heavy)** | base +2/+3/+4; Dex-cap +4/+2/+1 ✔ (crossover ~DEX +3/+4) |
| **Lethality** | standard **15%** / boss **30%** of PC HP per round ✔ |
| **Stim** | first use ~25–30% max HP; tolerance halves subsequent ~ |
| **Precision dice** (Scoundrel Exploit) | +1 die (L1), +2 (L5), +3 (L11), +4 (L17) ~ |
| **Attunement** (Guardian) | pool ≈ 2 + (level ÷ 2); Center regains ~1; powers cost 1–3; Push +1–2 ~ (softest; playtest) |

---

## 2. Benchmark Table (PC side, L1–5) ✔

Representative on-level PC (medium class, light armor, DEX key, CON +1; HP shows medium/tank):

| Lvl | Attack | AC | HP (med / tank) | Save DC | Good save |
|---|---|---|---|---|---|
| 1 | +5 | 17 | 17 / 20 | 14–16 | +6 |
| 3 | +6 | 18 | 35 / 44 | 16–17 | +8 |
| 5 | +8 (+9 geared) | 20 | 53 / 68 | 18–19 | +10 |

## 3. Creature Numbers (built to the benchmark) ✔

Standard on-level creature = **AC ≈ PC AC − 3** (PCs hit ~60%) and **attack ≈ PC attack + 3** (hits PCs ~60%):

| Lvl | Std AC | Std attack | Std HP | Std dmg/round | Role HP ×: minion 0.3 · elite 2 · boss 4 |
|---|---|---|---|---|---|
| 1 | 14 | +8 | ~16 | ~3 | minion ~5 · boss ~64 |
| 3 | 16 | +9 | ~28 | ~5 | elite ~56 · boss ~112 |
| 5 | 17 | +11 | ~35 | ~8 | minion ~12 · elite ~70 · **boss ~140** |

---

## 4. Validations (all inside bracket)

### 4.1 Bounded-accuracy / crit stability (T2) ✔
On-level hit = **60%** and crit = **10%** at *both* L1 and L5 — the Level term cancels, so rates depend only on build edge, never level. Crit climbs with optimization (e.g., +15% vs an Off-Guard target) but stays level-stable.

### 4.2 MAP −4/−8 ✔
L5 Soldier (ranged, ~11/hit vs AC 17): 2-Strike turn ≈ **12.6 DPR**, 3-Strike ≈ **15.4**. The 3rd Strike adds only **~18%** — discouraged but live; the 3rd action competes fairly with Suppress/move/Aid. Not spam-dominant.

### 4.3 Class DPR & contribution parity (T5) ✔ (qualitative)
| Class | L5 single-target DPR | Contribution shape |
|---|---|---|
| Soldier | ~13 | DPR + **Suppression control** (denies enemy actions/space) |
| Scoundrel | ~12–14 *when Exploiting* (Off-Guard), lower otherwise | conditional burst + **utility/social 3** |
| Guardian | ~14–16 melee (higher per-hit, Reactive-Shot risk; deflection tanks ranged) | single-target + **durability/control** |
| Technician | ~8 direct **+ drone Strike + turret + buffs/heals** | **support 3** force-multiplier (drone is *pre-deployed*, so round-1 relevant) |

Balanced in **contribution across different axes**, not identical DPR — niche over tier. (Support-value exact math → playtest.)

### 4.4 Encounter (rounds-to-kill, both directions) ✔
- Standard (~30 HP): **~1–2 rounds** of focused fire. Boss (140 HP): party ~40 DPR → **~4 rounds** with phases. No HP-slog.
- Boss → party: ~30% PC HP/round spread + Boss Actions → tense over 4 rounds, PCs may need stims / go down, but not a TPK.

### 4.5 Boss model ✔
- **Action ratio** 12 PC : (3 + 2 Boss Actions) = **~2.4 : 1** (vs naked 4:1). Boss Actions meaningfully restore parity.
- **Nova:** best party round ≈ 43–57% of boss HP < 60%, and the 50% phase fires first. ✔

### 4.6 DC ladder ✔
Trained L1 specialist (+5) vs Moderate 14 = 60%, rising with level; untrained L5 (~+2) vs Moderate 14 = 45% — a deliberate ~30-point trained/untrained gap. Spread holds across Hard/Severe/Extreme.

### 4.7 Degenerate scan ✔
- **No loops** (reactions can't chain — ranged Reactive Shot never provokes; Center is not action-positive).
- **No nova break** (§4.5).
- **No action compression** beyond intended bounded grants (Boss Actions ×2; the pre-deployed Drone commanded by an action).
- **No same-type stacking** past caps (circumstance/status/item each take best; MAP untyped by design).

---

## 5. Soft Numbers (validate in playtest)

Deflection damage-reduction values, precision-dice curve, support-value of the Technician's drone/turret/buffs. Structures are sound; the magnitudes need table data.

**Now locked** (playtest F6/F7, no longer "soft"): **Attunement** (pool `2+L`, Center +2, costs 0/1–2/3, Push +1/+2, Deflection free) → [Phase 5 §2.2](2026-06-13-phase5-class-design-and-force.md); **stimpack** grades 2d8/4d8/6d8/8d8 + tolerance `÷2^(N−1)` per encounter → [Phase 6 §3](2026-06-13-phase6-equipment-and-economy.md).

---

## 6. Required Content Directive — Rank-Gated Effects (resolves T1 watch-item)

**Decision:** keep **+1/rank** (bounded); make expertise *felt* through **rank-gated effects**, not bigger numbers.

- Every proficiency **signature** must unlock a capability at each rank step: **Expert** = a new option or crit-effect; **Master** = another; **Legendary** = the capstone.
- Without these, becoming Expert is just +5% to hit and feels flat. **This is a content task to complete before/with the playtest** (author rank-effects per class signature: Soldier weapons, Scoundrel skills, Guardian Force, Technician tech).
- *(Numbers stay; the effects are what differentiate — consistent with the Phase 1 "rank gates quality, not raw to-hit" lean.)*

---

## 7. Verdict & Carried Forward

- **Slice passes Gate A** — bounded-accuracy math validated, dials in bracket, no degenerate engines, contribution parity holds.
- **Before/with playtest:** author rank-gated effects (§6).
- **Tune in playtest:** the §5 soft numbers.
- **Re-run Gate-A-style analysis** after content expansion (Phase 8) and on any new class/creature/item — this doc is the benchmark to compare against.
- **Cosmetic C1–C6** (review doc) still parked.

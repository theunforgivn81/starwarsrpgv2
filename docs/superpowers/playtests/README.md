# Playtest Reports

Dynamic playtest reports produced by the `ttrpg-playtest-simulation` skill.

Each run writes a dated file here, kept separate from design specs so playtest
output and design intent don't intermix.

**Naming:** `YYYY-MM-DD-playtest-<scenario>.md`

**Each report contains:**
- The scenario and exact character builds used (so the run is reproducible)
- A condensed turn-by-turn session log
- A prioritized findings list: `id · severity · turn ref · spec link · failure class · repro · routed-to skill`

The skill **finds; it does not fix.** Each finding is routed to the relevant
design skill (balance-analysis, ability-design, rules-writing, creature-design,
system-review) for remediation.

# starwarsrpgv2

A Star Wars tabletop RPG rulebook (d20, ORC/2E substrate). Player-facing chapters live in `docs/player-core/`; design specs in `docs/superpowers/specs/`.

## Design wiki — primary source of truth

`wiki/` is the LLM-maintained design knowledge base (gitignored; OneDrive-backed) and the **first place to look for design knowledge** — what a mechanic is, why it exists, what was decided or rejected, what's still open. Start any design question here: read `wiki/index.md`, drill into the relevant pages, then follow their links out to canon in `docs/player-core/` or the underlying specs. The spec and plan files in `docs/superpowers/` are **raw sources beneath the wiki**, not the first stop — reach for them when a wiki page sends you there, not by default.

Its conventions and the ingest/query/lint workflows live in `wiki/SCHEMA.md` — read that before touching or querying wiki pages. When a design doc is added or meaningfully changed, ingest it into the wiki (per the Ingest workflow).

## Directives

- **Class and species traits are named exactly after their parent.** The Tech Specialist's class trait is `Tech Specialist`, never `Tech`; a species trait is the species' full name. `Technological` (not a class trait) marks technological creatures, objects, and effects.
- **Appendices are closed indexes.** Whenever new content references a trait or condition that has no entry in `docs/player-core/appendix-traits.md` or `docs/player-core/appendix-conditions.md`, add the entry in the same change. If the trait or condition exists in the ORC-licensed 2E core rules, adapt that text; otherwise write an original entry.

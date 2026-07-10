# LLM Wiki — Design Knowledge Base

**Date:** 2026-07-09
**Status:** Approved
**Pattern source:** the "LLM Wiki" idea file (persistent, LLM-maintained knowledge base sitting between raw sources and queries; Memex-style compounding artifact).

## Purpose

A persistent, interlinked markdown wiki at `/wiki/` that captures the **design knowledge** of the starwarsrpgv2 project: mechanics concepts, design decisions and their rationale, class design intent, open issues, and per-source summaries. The rulebook chapters in `docs/player-core/` remain the canonical rules text; the wiki holds the *why*, the cross-references, and the evolution — it never restates rules text at length, it links to it.

The wiki is written and maintained entirely by the LLM. The user browses it (Obsidian or VS Code), directs analysis, and asks questions; good answers are filed back into the wiki as pages.

## Three layers

1. **Raw sources (immutable):** `docs/player-core/` (canonical rules), `docs/superpowers/specs|plans|playtests/` (design history), `reference_data/swf20260426.sql` (ORC dump). The wiki reads these, never modifies or copies them.
2. **The wiki:** `/wiki/` — LLM-generated markdown, structure below.
3. **The schema:** `wiki/SCHEMA.md` — conventions and workflows (ingest/query/lint). A short pointer section in the project `CLAUDE.md` tells future sessions the wiki exists and that `SCHEMA.md` governs it.

## Directory structure

```
wiki/
  SCHEMA.md      — conventions + ingest/query/lint workflows (the wiki's CLAUDE.md)
  index.md       — catalog of every page by category; updated on every ingest
  log.md         — append-only chronology; entries: ## [YYYY-MM-DD] ingest|query|lint | Title
  overview.md    — synthesis hub: what the game is, state of the design, where things stand
  concepts/      — cross-cutting mechanics & design ideas (bounded accuracy, no-daily-clock
                   recovery, trait system, four-degree resolution, social engine, …)
  decisions/     — one page per significant design decision: what was decided, why,
                   alternatives rejected, what would reopen it
  classes/       — one page per class: design intent, core verb, subclass logic,
                   balance history — never restating rules text
  sources/       — one summary page per ingested document
  issues/        — open problems & deferred work (reaction stacking, social chapter gap, …)
```

## Page conventions

- **Wikilinks** `[[page-name]]` everywhere (Obsidian graph view is a first-class consumer).
- **YAML frontmatter** on every page: `type` (concept | decision | class | source | issue | hub), `tags`, `sources` (repo paths), `updated` (date). Dataview-compatible.
- **Source pages** carry the repo-relative path of the underlying document so canon is one click away, plus: key takeaways, what it decided, what superseded it or what it superseded.
- **Supersession is flagged, not deleted:** `> ⚠️ Superseded by [[x]]` — the history is the point.
- **No design-rules duplication:** where the rulebook already says it, link `docs/player-core/...` instead of restating.

## Storage & versioning

- `wiki/` is **added to `.gitignore`** — it is backed up by OneDrive, not git (user decision 2026-07-09).
- `.obsidian/` is also gitignored so the user can open the project root (or `wiki/`) as an Obsidian vault without polluting the repo. The old empty vault at `Documents\Obsidian\StarWarsRpg` is abandoned.

## Workflows (detailed in SCHEMA.md)

- **Ingest:** read source → write/update `sources/` page → update every touched concept/decision/class/issue page → update `index.md` → append to `log.md`.
- **Query:** read `index.md` first, drill into pages, answer with citations; file durable answers back as pages (and log them).
- **Lint:** periodic health check — contradictions, stale claims, orphan pages, missing cross-references, concepts mentioned but pageless; log the pass.

## Initial ingestion (phased, full build now)

Dependency order mirroring the build roadmap:

1. **Foundation:** design philosophy + build roadmap.
2. **Engine:** Phase 1–3 specs (core mechanic + traits, character framework, progression chassis) + rank-gated effects + skill actions.
3. **Pillars:** Phase 4–7 specs (social engine, class design + Force, equipment, creatures) + shared Force toolkit.
4. **Classes:** class roster/subclass sketches, seven class specs, lightsaber forms, creation-slot contributions, species/backgrounds rosters + chapter design; player-core writeups read for the *delta* between spec and shipped text.
5. **Validation:** playtests + Gate-A balance passes + connective-tissue remediation.
6. **Recent reworks:** Manifest universal action, Consular mandate rework, appendices design, feat entry + activated-ability formats.

Each ingest touches: one source page, the relevant concept/decision/class/issue pages, `index.md`, `log.md`.

## Success criteria

- Every document in `docs/superpowers/` has a `sources/` page; `index.md` catalogs all pages; `log.md` records every ingest.
- Concept pages answer "what is the current state of X and how did it get there" with links, without re-reading the specs.
- Obsidian graph shows a connected web (no orphan pages after the lint pass).
- A future session can maintain the wiki from `SCHEMA.md` alone.

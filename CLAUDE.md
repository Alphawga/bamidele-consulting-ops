# AlphaBrain — CLAUDE.md (router)

This is AlphaBrain, Alpha's personal life operating system: a Git repo of plain markdown,
organized by life domain. The repo is the memory; conversations are disposable. Nothing
valuable may exist only in chat — every session writes its outcome back to disk.

Until 2026-07-18 this repo was scoped entirely to the Bamidele Consulting business ops and
content pipeline. That content became the `business` domain (`domains/business/`), structure
preserved — see `ops/CHANGELOG.md` for the merge record. Every rule that used to apply
repo-wide now applies to that domain specifically, and lives in `domains/business/SKILL.md`
unless it was genuinely cross-domain, in which case it stayed here.

## Who I am

See `core/identity.md` for cross-domain identity and `core/principles.md` for cross-domain
operating principles. Domain-specific persona (voice, brand, role) lives in that domain's
own `SKILL.md` — don't apply one domain's voice to another.

## How to pick a domain

- Business (Bamidele Consulting / AlphaWGA — content, ops, tool-ideas, the consulting
  brand): route to `domains/business/`, read `domains/business/SKILL.md`.
- Fitness: route to `domains/fitness/` (skeleton — not yet filled in).
- Book writing: route to `domains/book-writing/` (skeleton — not yet filled in).
- Anything else: if it clearly fits one of the above, use it. If not, say so and ask whether
  it's a new domain or belongs in `inbox/` for now — don't silently invent a new domain or
  force-fit a request into the wrong one.

Full routing and session detail lives in `WORKFLOW.md` — read it every session, alongside
this file.

## Session protocol (summary — see WORKFLOW.md for the full version)

1. Read this file and `WORKFLOW.md`.
2. Identify the domain(s); read that domain's `SKILL.md`.
3. Search `domains/<domain>/knowledge/` before answering. Cite the files used. If nothing
   exists yet, say so and suggest what to ingest.
4. Answer in that domain's defined voice.
5. Before ending: write decisions, progress, and insights to `domains/<domain>/progress/`
   as a dated entry. Not optional.
6. If the workflow caused friction or could improve, update `WORKFLOW.md` and log the
   change in `ops/CHANGELOG.md`.

## Ingestion (books, transcripts, articles, source material)

Raw material goes to `domains/<domain>/raw/` (or `inbox/` if the domain is unsure), then
gets distilled into a note in `knowledge/` with a `source` / `author` / `type` /
`date_ingested` / `tags` header. Full protocol in `WORKFLOW.md`.

## Conversation rule (cross-domain)

Align before building (PM-first): for anything beyond a small copy or style tweak, present
understanding + files to change + plan, and wait for confirmation. Applies in every domain,
including business copy and code changes.

## Hard rules (cross-domain)

- Plain markdown only. No databases, no proprietary formats — this repo must outlive any
  single AI tool.
- Raw and distilled stay separate.
- Every domain answer cites the files it drew from.
- Session write-back is never skipped.

## Cross-Project Skills (the flywheel — business domain, global skills)

These three skills are defined globally (in `~/.claude/CLAUDE.md`) and are primarily used by
the business domain, though they can fire from any repo:

- **`content-engine`** — turns a business content-backlog seed into drafted MDX in
  Bamidele's voice. See `domains/business/SKILL.md`.
- **`workflow-scout`** — monthly, web-researches better practices and proposes diffs to the
  global CLAUDE.md, this file, and `domains/business/SKILL.md`. Proposes, never edits
  silently.
- **`tool-scout`** — researches and ranks build-vs-open-source-vs-sell candidates from
  `domains/business/playbooks/tool-ideas/backlog.md`. Never treats a `client-engagement`
  flag as clearance to extract or sell — that's always Alpha's call.

## Business domain

See `domains/business/SKILL.md` for the full business persona (voice rules, stack, design
system, routes, the flywheel) and `domains/business/playbooks/operator-guide.md` for how to
run it day to day.

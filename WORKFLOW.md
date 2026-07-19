# Workflow

How AlphaBrain operates day to day. This file evolves — if the workflow causes friction or
could work better, update it and log the change (date + reason) in `ops/CHANGELOG.md`.

## Picking a domain

Every request belongs to one or more `domains/<domain>/`. Currently:

- `business` — Bamidele Consulting / AlphaWGA content pipeline + operator guide, general
  sales skill-building, and career management. One shared `raw/` intake; `knowledge/` is
  organized by sub-area (`knowledge/sales/`, `knowledge/career/`, plus the content-pipeline
  files at the top level). See `domains/business/SKILL.md`.
- `fitness` — skeleton only, not yet filled in.
- `book-writing` — skeleton only, not yet filled in.

If a request doesn't clearly fit an existing domain, say so and ask whether it's a new
domain or belongs in `inbox/` for now. Don't silently invent a new domain.

## Every session

1. Read `CLAUDE.md` (router) and this file first.
2. Identify the domain(s) the request touches; read that domain's `SKILL.md`.
3. Before answering, search `domains/<domain>/knowledge/`. If material exists, use it and
   cite the file (`path:line` where useful). If not, say so, answer from general knowledge,
   and suggest what to ingest to close the gap.
4. Answer in the persona/voice that domain's `SKILL.md` defines.
5. Before ending the session: write decisions, progress, and insights into
   `domains/<domain>/progress/` as a dated entry. Not optional — this is how the system
   accumulates memory instead of losing it to disposable chat.
6. If the workflow itself caused friction or could improve, update this file and log the
   change in `ops/CHANGELOG.md`.

## Ingestion (when given a book, transcript, article, or other source material)

1. Save the raw material to `domains/<domain>/raw/` (or `inbox/` if the domain is unsure).
2. Distill it into a note in `domains/<domain>/knowledge/` with a header: `source`,
   `author`, `type`, `date_ingested`, `tags`.
3. Body: core ideas, key principles, notable quotes, "how this applies to me."
4. Confirm what was filed and where.

## Hard rules

- Plain markdown only. No databases, no proprietary formats — this repo must outlive any
  single AI tool.
- Raw and distilled stay separate: `raw/` is archive, rarely read; `knowledge/` is what gets
  cited.
- Every domain answer cites the files it drew from.
- Session write-back (step 5 above) is never skipped.
- Business-domain specifics (voice rules, stack, brand) live in `domains/business/SKILL.md`
  and `domains/business/knowledge/CLAUDE.md` — not here. This file only covers cross-domain
  operating rules.

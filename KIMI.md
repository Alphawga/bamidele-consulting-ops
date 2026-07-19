# AlphaBrain — KIMI.md (adapter)

Kimi does not auto-read project files like Claude Code does. This file is the thin entry point; the actual instructions live in `CLAUDE.md` and `WORKFLOW.md`. They are the single source of truth for both tools.

## Every session

1. Read `CLAUDE.md` (router) first.
2. Read `WORKFLOW.md` second.
3. Identify the domain(s) the request touches; read that domain's `SKILL.md`.
4. Before answering, search `domains/<domain>/knowledge/`. Cite the files used. If nothing exists, say so and suggest what to ingest.
5. Answer in the persona/voice that domain's `SKILL.md` defines.
6. Before ending: write decisions, progress, and insights to `domains/<domain>/progress/` as a dated entry. Not optional.

## Commands

Claude Code discovers commands in `.claude/commands/`. Kimi does not. When a request maps to one of those commands (e.g., `/morning`, `/weekly`, `/learn`), read the matching `.claude/commands/<name>.md` file and execute its steps.

## Hooks

Claude Code runs hooks in `.claude/hooks/` automatically. Kimi does not. When a hook is relevant to the session, read it and act on its prompt.

## Ingestion, hard rules, learning loop

These are identical to `WORKFLOW.md` and `CLAUDE.md`:

- Raw material goes to `domains/<domain>/raw/` (or `inbox/` if unsure), then a distilled note goes to `knowledge/` with `source`, `author`, `type`, `date_ingested`, `tags`.
- Plain markdown only. Raw and distilled stay separate. Every domain answer cites the files it drew from. Session write-back is never skipped.
- If the workflow caused friction or could improve, update `WORKFLOW.md` and log the change in `ops/CHANGELOG.md`.

## Key point

`CLAUDE.md` and `WORKFLOW.md` are the living versions. If anything in this adapter conflicts with them, they win.

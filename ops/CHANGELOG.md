# Changelog

Dated log of changes to how AlphaBrain operates (WORKFLOW.md, structure, routing). Newest
on top.

---

## 2026-07-19 · Folded sales and career into domains/business/, one shared raw/

- Per-domain `raw/` silos created friction: dropping a source document meant deciding its
  domain upfront. Alpha asked why business, sales, and career couldn't share one raw intake
  with routing happening at distillation time instead.
- Sales and career are one domain with business, not three: `domains/sales/` and
  `domains/career/` (skeletons, never filled in) were removed. Everything lives under
  `domains/business/` now.
- `domains/business/raw/` is the single shared intake for consulting-brand, sales, and
  career source material — undifferentiated; filed into the right `knowledge/` subfolder
  only once distilled.
- `domains/business/knowledge/` gained `sales/` and `career/` subfolders for distilled notes,
  sitting alongside the existing content-pipeline files (`CLAUDE.md`, `calendar.md`,
  `learnings.md`, `pillars/`, etc.), which are untouched.
- `domains/business/progress/` added for session write-backs on sales/career/general-ops
  conversations; the content pipeline keeps tracking its own history in `calendar.md` /
  `streak.md` / `learnings.md`.
- `domains/business/SKILL.md` updated: the brand voice rules apply strictly to published
  AlphaWGA/Bamidele copy, not to internal sales or career advice — made that scope explicit
  so the two don't bleed into each other.

---

## 2026-07-18 · Added KIMI.md adapter for interchangeable Claude/Kimi use

- Added `KIMI.md` at the repo root as a thin entry point for Kimi.
- `CLAUDE.md` and `WORKFLOW.md` remain the single source of truth for both tools.
- Kimi reads the existing `.claude/commands/` and `.claude/hooks/` directly instead of
  duplicating them, so improvements apply to both tools immediately.
- Updated the learning loop: whichever tool finds workflow friction updates
  `WORKFLOW.md` and logs the change here, so both tools stay in sync.

---

## 2026-07-18 · Merged bamidele-consulting-ops into AlphaBrain root

- This repo, previously scoped only to the Bamidele Consulting content pipeline, became the
  root of AlphaBrain, a personal life operating system organized into domains.
- The old repo content became the `business` domain, structure preserved:
  `content/` → `domains/business/content/`, `content-brain/` → `domains/business/knowledge/`,
  `CONTROL.md` → `domains/business/playbooks/operator-guide.md`,
  `tool-ideas/` → `domains/business/playbooks/tool-ideas/`.
- Added the AlphaBrain shell: `WORKFLOW.md`, `core/`, `inbox/`, `ops/`, and empty domain
  skeletons for `fitness` and `book-writing` (not yet filled in — need goals/current
  state/source material to populate `SKILL.md` and `knowledge/`).
- Root `CLAUDE.md` rewritten as a unified router: preserves all prior operational rules,
  adds domain routing and session/ingestion protocol on top.

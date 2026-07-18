# Changelog

Dated log of changes to how AlphaBrain operates (WORKFLOW.md, structure, routing). Newest
on top.

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

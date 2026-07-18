# AlphaBrain

Alpha's personal life operating system. A Git repo of plain markdown, organized by life
domain. The repo is the memory; conversations are disposable — nothing valuable should
exist only in chat. See `WORKFLOW.md` for how it operates and `CLAUDE.md` for the router.

## Structure

```
alphabrain/
├── CLAUDE.md          # router: who I am, how to pick a domain, session rules
├── WORKFLOW.md         # how the system operates (this evolves)
├── core/                # identity.md, principles.md — cross-domain context
├── domains/<domain>/
│   ├── SKILL.md         # persona: role, voice, procedures
│   ├── knowledge/       # distilled notes — what gets cited
│   ├── raw/             # original transcripts/texts — archive, rarely read
│   ├── progress/        # dated journal entries, metrics, weekly reviews
│   └── playbooks/
├── inbox/               # unsorted captures
└── ops/                 # scripts, cron jobs, CHANGELOG.md
```

## Domains

- **business** (`domains/business/`) — Bamidele Consulting / AlphaWGA: the content pipeline,
  the operator guide, the tool-ideas backlog. This was the entire repo before the 2026-07-18
  merge into AlphaBrain (see `ops/CHANGELOG.md`); its internal structure is unchanged, only
  the parent path moved.
- **fitness** (`domains/fitness/`) — skeleton, not yet filled in.
- **book-writing** (`domains/book-writing/`) — skeleton, not yet filled in.

## Business domain quick reference

The public website for the business domain lives in a separate repo, `bamidele-consulting`
(deploys to Vercel). Finished, intended-public posts go there; ideas and ops stay here.

| Repo | Visibility | Holds |
|------|-----------|-------|
| `bamidele-consulting` | public | The website that deploys to Vercel + published content |
| `bamidele-consulting-ops` (this one, AlphaBrain root) | private | Every life domain, including business ops |

- `domains/business/content/backlog.md` — the content idea inbox (unpublished angles).
- `domains/business/content/radar/` — daily content radar digests, dropped here by the
  daily cloud routine as PRs.
- `domains/business/SKILL.md` — the business domain's persona: voice, stack, design, routes.
- `domains/business/playbooks/operator-guide.md` — how to run the business domain, routine IDs.
- `.claude/` — the content-capture Stop hook + settings (stays at repo root; Claude Code
  only reads `.claude/` from the project root).

### How the two repos work together

1. The daily content radar routine opens a PR here with fresh ideas (private).
2. You pick an idea. Ask Claude to "draft the blog post about X" (the `content-engine` skill).
3. The finished `.mdx` post is added to the PUBLIC `bamidele-consulting` repo, which deploys.

So ideas and pipeline stay private. Only finished, intended-public posts reach the public repo.

### Cloud routines (point at this repo)

- Daily content radar: https://claude.ai/code/routines/trig_01NRLH2YSyLEQozwHrryUZfw
- Monthly workflow scout: https://claude.ai/code/routines/trig_01GpKyU5CTdK1zRbCpwwxXrY

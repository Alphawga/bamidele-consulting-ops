# bamidele-consulting-ops (private)

The private operations and content pipeline for the consulting brand. This is the "behind
the curtain" repo. It is paired with the public site repo.

| Repo | Visibility | Holds |
|------|-----------|-------|
| `bamidele-consulting` | public | The website that deploys to Vercel + published content |
| `bamidele-consulting-ops` (this one) | private | Content pipeline, workflow docs, automation |

## What lives here

- `content/backlog.md` — the content idea inbox (unpublished angles).
- `content/radar/` — daily content radar digests (what to post about), dropped here by the
  daily cloud routine as PRs.
- `CLAUDE.md` — the full project + workflow reference.
- `CONTROL.md` — the operator guide (how to run the whole system, routine IDs).
- `.claude/` — the content-capture Stop hook + settings.

## How the two repos work together

1. The daily content radar routine opens a PR here with fresh ideas (private).
2. You pick an idea. Ask Claude to "draft the blog post about X" (the `content-engine` skill).
3. The finished `.mdx` post is added to the PUBLIC `bamidele-consulting` repo, which deploys.

So ideas and pipeline stay private. Only finished, intended-public posts reach the public repo.

## Cloud routines (point at this repo)

- Daily content radar: https://claude.ai/code/routines/trig_01NRLH2YSyLEQozwHrryUZfw
- Monthly workflow scout: https://claude.ai/code/routines/trig_01GpKyU5CTdK1zRbCpwwxXrY

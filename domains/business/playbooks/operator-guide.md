# Control guide

How to run and steer the whole system. You mostly control it by talking to Claude Code in
plain language. This page lists the few places you touch things directly.

Two repos: the public **site** repo `bamidele-consulting` (deploys to Vercel) and this private
**ops** repo `bamidele-consulting-ops` (pipeline + workflow + automation). Edit site code in
the site repo; manage content ideas and automation here.

## The three layers

| Layer | What it is | How you control it |
|-------|-----------|--------------------|
| Website | What visitors see | Edit files, or ask Claude to "change X"; deploy via Vercel |
| Content flywheel | How work becomes blog posts and case studies | `content-engine` skill + `content/backlog.md` |
| Workflow loop | How the system improves itself | `workflow-scout` skill + the monthly cloud routine |
| Tool/IP scout | How work becomes product ideas | `tool-scout` skill + `tool-ideas/backlog.md` + the weekly cloud routine |

## 1. Run and deploy the site

```bash
cd ~/bamidele-consulting
npm run dev      # preview at http://localhost:3000
npm run build    # confirm it compiles
```

To go live: import this repo on vercel.com and set the env vars from `.env.example`.
After that, every `git push` to `main` auto-deploys.

## 2. Add content

Two ways, both fine:

- Tell Claude: "draft a blog post about X" or "turn the Okoh build into a case study."
  It uses the `content-engine` skill and writes in the brand voice, saved as a draft.
- Capture an idea for later: add a one-line seed to `content/backlog.md`. The Stop hook
  also nudges you to do this when site files change.

Content lives in `content/blog/*.mdx` and `content/case-studies/*.mdx`. Set `draft: true`
in the frontmatter to hide a post. Blog frontmatter: `title`, `summary`, `date`, `author`.

## 3. Daily content radar (what to post about)

Each morning a cloud routine browses the web for 5 to 7 fresh things you can post about on
LinkedIn or write up: oil and gas procurement and supply chain, AI in operations, Nigerian
business and fintech, and broad interesting signals.

- It opens a daily PR titled "Content radar — <date>", so you get a GitHub notification you
  can read from your phone. The digest is in the PR body and in `content/radar/<date>.md`.
- The 2-3 strongest picks are added to `content/backlog.md`. To act on one, just say
  "draft the blog post about X" and the `content-engine` skill writes it in your voice.
- Manage it: https://claude.ai/code/routines/trig_01NRLH2YSyLEQozwHrryUZfw
- Runs ~7:15am Lagos daily. To run on demand locally, ask Claude to "scan for content ideas"
  (content-engine radar mode).

## 4. Self-improvement (the scout)

- On demand: type `/workflow-scout` or ask Claude to scout for workflow improvements. It
  researches and proposes changes. Nothing applies without your approval.
- Monthly, automatic: a cloud routine runs on the 1st of each month and opens a PR with
  proposed improvements.
  - Manage it: https://claude.ai/code/routines/trig_01GpKyU5CTdK1zRbCpwwxXrY
  - It needs GitHub connected for the cloud account. Run `/web-setup` once, or install the
    Claude GitHub App: https://claude.ai/code/onboarding?magic=github-app-setup

## 5. Weekly tool scout (what's worth building, open-sourcing, or selling)

Each week a cloud routine looks at recent work across your repos (own work and client
engagements like Okoh), plus the internet, for things generic enough to become a standalone
product, an open-source tool, or sellable IP.

- It opens a weekly PR titled "Tool scout — <date>", so you get a GitHub notification you can
  read from your phone. The ranked digest is in the PR body and in `tool-ideas/reports/<date>.md`.
- The top picks are added to `tool-ideas/backlog.md`. Every candidate is tagged `owned` or
  `client-engagement` — a `client-engagement` tag means the idea is flagged, not cleared. You
  decide the rights question before acting on it, the scout never assumes consent.
- If the Gmail connector is connected (Anthropic connector, set up once via claude.ai), it
  also leaves a Gmail **draft** with the top picks for you to review and send yourself — it
  never auto-sends.
- Capture ideas as you build: say "log a tool idea" or just keep working — the global
  CLAUDE.md nudges Claude to capture a seed at the end of a noteworthy session, from any repo.
- Manage the routine: (fill in the routine URL after `/schedule create` runs).

## Where to change specific things

| Want to change | File |
|----------------|------|
| Wordmark / header | `components/Header.tsx` |
| Colors and fonts | `tailwind.config.ts`, `app/layout.tsx` |
| Nav items | `lib/site.ts` |
| Voice rules | project `CLAUDE.md` (and the global memory the skills read) |
| Contact email / Cal link / Resend key | `.env.local` (copy from `.env.example`) |
| Turn off the content-capture nudge | `.claude/settings.json` |

## What runs on its own vs. needs you

- Automatic: memory loads each session, the Stop-hook content nudge, the monthly workflow
  scout, the weekly tool scout (once GitHub is connected).
- You decide: writing and approving content, deploying, approving scout PRs, sending any
  Gmail draft the tool scout leaves, the rights call on any `client-engagement` idea,
  anything outward-facing.

## Prerequisite for the tool scout's Gmail draft step

Connect Gmail via the official Anthropic connector once, in claude.ai settings (browser
OAuth, no credentials stored locally). Until connected, the tool scout still runs and writes
the PR + report + Artifact — it just skips the Gmail draft and says so in the report.

## Note on memory

The project memory and design rules auto-apply only when you open Claude Code inside this
folder (`~/bamidele-consulting`). The `content-engine` and `workflow-scout` skills and your
global rules work from any project.

## Still to supply

Result numbers, client-naming decision, live automation names, pricing, headshot, client
logo, Cal.com link (`NEXT_PUBLIC_CAL_LINK`), Resend key (`RESEND_API_KEY`).

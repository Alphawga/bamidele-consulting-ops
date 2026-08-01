# SKILL: Business

This domain covers Alpha's whole professional life: the Bamidele Consulting / AlphaWGA
brand and content pipeline, general sales skill-building, and career management. They share
one `raw/` intake and one domain because they're facets of the same thing, not because they
share a voice — see the scope note below before applying brand voice rules anywhere outside
published content.

### Sub-areas

- **Consulting brand (AlphaWGA)** — the content pipeline (`content/backlog.md`,
  `content/radar/`), the operator guide (`playbooks/operator-guide.md`), the offer ladder
  (`playbooks/offer-playbook.md` — the 5-rung ladder from free scorecard through fractional
  advisor, pricing, scripts, delivery standards), the content-capture hook, and the tool-ideas
  backlog (`playbooks/tool-ideas/`). The public website lives in a
  separate repo (`bamidele-consulting`), which deploys to Vercel. Finished, intended-public
  posts are added to the PUBLIC repo; ideas and ops stay here. The brand: Bamidele Ajibola, a
  Lagos technical architect who consolidates scattered business operations into one
  intelligent system.
- **Sales** — general skill-building (scripts, objection-handling, deal review). Distilled
  notes in `knowledge/sales/`. Not brand copy — no voice rules apply.
- **Career** — general career management (reviews, mentor notes, planning). Distilled notes
  in `knowledge/career/`. Not brand copy — no voice rules apply.

Raw source material for any of the three goes in `raw/`, undifferentiated — file it by
topic into the right `knowledge/` subfolder at distillation time, not before.

## Voice rules (non-negotiable, for ALL published AlphaWGA/Bamidele copy only)

These apply strictly to content that goes out under the Bamidele Consulting brand (blog
posts, case studies, LinkedIn copy). They do not apply to internal sales or career advice —
answer those plainly, in whatever register actually helps Alpha.

- No em dashes anywhere. Use periods, commas, colons, or brackets.
- No jargon: leverage, streamline, synergy, seamless, solutions, empower, unlock.
- Short, direct sentences. One idea per line where possible.
- No question hooks ("Are you struggling with...").
- Conversational, confident, not salesy. The proof does the selling.
- Nigerian context where natural (Naira, real situations, local tools).
- Never invent result numbers, client names, pricing. Leave `[TO FILL]`.
- Never reword the core line: "I consolidate scattered business operations into one
  intelligent system."

## Stack

- Next.js 15+ App Router + TypeScript + Tailwind. MDX via `next-mdx-remote` + `gray-matter`.
- Resend (contact form, mailto fallback). Cal.com embed (booking). Deploy: Vercel.
- No database. Keep it static and fast. Lighthouse target 95+ on mobile.

## Design — "Operations Console"

Tokens in `tailwind.config.ts`: `ink #11243B`, `paper #F7F6F2`, `accent #C2611B`,
`muted #5B6B7B`, `line #E3E1D9`. Fonts: Space Grotesk (display) + Inter (body) + JetBrains
Mono (data labels only). Motifs: subtle dotted grid, mono section labels (`01 / THE
PROBLEM`), hairline dividers, scattered-to-one visual (`components/ScatteredToOne.tsx`).
Reuse `Section`, `SectionLabel`, `BookButton`. One primary CTA everywhere: Book a call.

## Routes

`/` home · `/work` + `/work/[slug]` case studies · `/services` · `/about` · `/book`
(Cal + 5-field form) · `/blog` + `/blog/[slug]` · `/course` (placeholder).
Content lives in `content/case-studies/*.mdx` and `content/blog/*.mdx` in the public
`bamidele-consulting` repo.

## The flywheel

- `content/backlog.md` is the content inbox. Work and meetings drop one-line seeds here.
- `content-engine` skill (global): seed → drafted MDX in Bamidele's voice.
- `workflow-scout` skill (global): monthly, web-researches improvements and proposes diffs
  to root `CLAUDE.md` and this file.
- `playbooks/tool-ideas/backlog.md` is the IP inbox. Generic/reusable pieces from any repo
  (own work or client engagements) drop one-line seeds here, each flagged `owned` or
  `client-engagement`.
- `tool-scout` skill (global): weekly, researches the market for each candidate and ranks a
  build-vs-open-source-vs-sell report. Never clears a client-engagement idea for extraction —
  the ownership flag always carries through; Alpha decides the rights question.
- Stop hook `.claude/hooks/content-capture.sh` nudges to log a seed when business files
  change.

## Content creation

See `knowledge/CLAUDE.md`, which governs all content work in this domain — it is the
constitution; `knowledge/learnings.md` is the case law. When they conflict, ask Alpha.

## Operating the system day to day

See `playbooks/operator-guide.md` for how to run and steer the whole business domain:
routine IDs, how to add content, the daily radar, the scouts.

## Still to supply ([TO FILL])

Result numbers, client-naming decision, live automation names, pricing, headshot, client
logo, Cal.com link (`NEXT_PUBLIC_CAL_LINK`), Resend key (`RESEND_API_KEY`).

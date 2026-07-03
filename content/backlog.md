# Content backlog

The flywheel inbox. Working on a build or sitting in a client meeting often surfaces a
content angle. Log it here as a one-line seed. Later, the `content-engine` skill turns a
seed into a drafted `/blog` post or a `/work` case study.

Newest on top. Format:

`YYYY-MM-DD · [source] · target · angle`

- source: `work` (something shipped/solved), `meeting` (client conversation), `idea`
- target: `blog` (post) or `case-study`

Voice rules apply to every draft: no em dashes, no jargon, short direct sentences, no
question hooks, never invent numbers. See the `content-engine` skill.

---

- 2026-07-03 · idea · blog · The $46M MRO blind spot: oil and gas companies paying emergency freight on parts already sitting in their own storeroom three sites away. One connected inventory view, checked before the PO is raised, fixes this.
- 2026-07-03 · idea · blog · Nigeria's enterprise AI gap: workers rank 6th globally for AI literacy, enterprises rank 19th. The bottleneck is fragmented ops infrastructure, not missing skills.
- 2026-07-03 · idea · blog · Why legacy platform migration is harder than buying a new system: the real cost of fragmented enterprise ops is extracting years of data from seven systems that were never designed to talk to each other.

- 2026-06-18 · idea · blog · Why connected accounting beats month-end reconciliation, told through the Okoh receiving-to-ledger flow.

## Published

- 2026-06-18 · The future of procurement runs on one connected system → content/blog/the-future-of-procurement.mdx

## Real values to supply on the public site (replace softened copy when ready)

- Okoh result numbers: hours saved per week, quote turnaround before/after, missed orders
  before/after, inventory value made visible, time to close the books. Add to the homepage
  Outcome block and the case study outcome section.
- Contact email: set `lib/site.ts` `email` and the `CONTACT_TO_EMAIL` env to the real address.
- Cal.com link: set `NEXT_PUBLIC_CAL_LINK` to show live booking on `/book`.
- Resend key: set `RESEND_API_KEY` so the contact form emails instead of mailto fallback.
- About photo: replace the branded portrait panel with a real headshot when available.

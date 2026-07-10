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

- 2026-07-10 · idea · blog · NCDMB's physical capacity audit exposes why vendor data integrity matters more than vendor count. Angle: the briefcase contractor problem is an operations data problem, and the companies with clean records and transparent systems will rise through the new five-tier framework.
- 2026-07-10 · idea · blog · 88% of enterprise AI agent pilots never reach production. The cause is not the model. It is disconnected data and undocumented processes. Angle: operational consolidation is the prerequisite for automation, not an optional step before it.
- 2026-07-10 · idea · blog · Nigerian oil and gas MRO procurement leakage traced to reactive ordering and no cross-site inventory visibility. Global integrated systems show 15 to 30% total MRO cost reduction. Angle: one connected inventory and maintenance system closes the gap that better supplier contracts cannot.
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

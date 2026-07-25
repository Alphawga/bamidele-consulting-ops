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

- 2026-07-25 · radar · blog · US 12.5% tariff on Nigerian imports (July 24): the cost baseline for every procurement team touching US trade just changed overnight. The argument for a connected system that updates landed costs in one place is now priced into every export quote.
- 2026-07-25 · radar · blog · NRS e-invoicing July 31 deadline: large taxpayers (N5B+ turnover) have six days. Software onboarding takes a week; cleaning scattered financial data takes months. The deadline is a mirror for your back-office health.
- 2026-07-25 · radar · blog · Dangote/NNPCL crude supply standoff: one party measured against what was available, the other against what was nominated. Different figures from different systems. That is a procurement data integrity failure, not a policy dispute. Same pattern seen weekly inside mid-sized procurement operations.

- 2026-07-19 · idea · blog · Went and actually counted a real person's post timestamps instead of trusting a search summary of "expert advice" about how often they post. The real number was nearly double what the secondhand advice claimed. If a decision matters, count it yourself.
- 2026-07-19 · idea · blog · Big personal brands fuse the value and the pitch into one post every time, no separation. That only works once you already have the audience. Before that point, some posts have to sell nothing, on purpose, or nobody sticks around long enough to see the offer.
- 2026-07-19 · idea · blog · Everyone copies the routine they assume a successful person has, not the one they actually said. Checked Priestley's real advice before doubling my own posting cadence: he teaches 3x a week, not daily, and 2026 platform data shows 2+ posts a day cost you about 40% of your reach. Check the source before you copy the habit.
- 2026-07-19 · idea · blog · Input feels like progress. It isn't. My own repo proves it: one post published, ever, and a backlog of 15 seeds sitting there because reading a third strategy book felt more productive than drafting the first one. The pattern I warn clients about (adding tools instead of using the one they have) works the same way on ideas.
- 2026-07-19 · idea · blog · Two unrelated sources (Daniel Priestley's "merry-go-round of distraction" and my own offer playbook) landed on the same warning independently: chasing a new niche or offer every time one gets hard feels like progress but resets you to zero. Depth in one lane beats width across five.
- 2026-07-19 · idea · blog · A vague answer to "what do you do" gets a polite nod, not a reaction, and the nod is the failure, not disagreement. You are also who Google says you are: if someone can't find you after a good conversation, they start doubting the conversation.
- 2026-07-19 · idea · blog · The ₦10K diagnostic call isn't revenue, it's a filter: the price does psychological work (screens out tire-kickers, creates commitment) not financial work. Most consultants underprice their qualifying step and drown in free-consult DMs.
- 2026-07-19 · idea · blog · Why I sign as "Bamidele Ajibola, Founder, AlphaWGA" and not one or the other: the person builds trust on LinkedIn, the company sends the invoice. A ₦1.5M bill from a company feels like hiring a firm; the same bill from a personal account feels like paying a freelancer. Positioning is priced in before the client reads a single line.
- 2026-07-19 · idea · blog · Stopped forcing myself to sort source material into a category before I understood it. Now everything drops into one raw inbox and gets classified at the distillation step instead of at capture. Same fix I'd hand a client drowning in miscategorized inventory or receipts: capture first, classify with intelligence downstream, don't make the human sort blind.
- 2026-07-19 · radar · blog · NCDMB Q3 capacity audit will use physical inspection to grade contractors: the companies whose operations are documented in one place will pass; the ones with scattered spreadsheets and email threads will not.
- 2026-07-19 · radar · blog · CBN's new real-time FX tracker for BDCs (July 15): the regulator solved its visibility problem with one portal. Operators can solve the same problem inside their own business.
- 2026-07-19 · radar · blog · Gartner: 40% of AI agents in production will be decommissioned by 2027 due to governance gaps. The failure pattern is identical to scattered-tools problems in procurement operations.
- 2026-07-18 · work · blog · Rebuilt my own scattered notes/ops repo into one domain-based system (AlphaBrain), business ops as one domain among several — the exact "scattered operations into one intelligent system" line, applied to my own life instead of a client's.
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

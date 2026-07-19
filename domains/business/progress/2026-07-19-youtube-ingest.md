# 2026-07-19 — YouTube ingestion: 8 Daniel Priestley videos

## What was done

Fetched transcripts for eight Daniel Priestley videos and ingested them into the
business domain: full transcripts saved to `raw/`, distilled notes saved to
`knowledge/`, and implications for playbooks/skills logged in `progress/`.

## Videos processed

| # | Video | Raw file | Knowledge note |
|---|-------|----------|----------------|
| 1 | [Give Me 29 Minutes and I’ll Teach You to Make $1 Million](https://www.youtube.com/watch?v=72a1PjnZFIM) | `raw/2026-07-19-daniel-priestley-give-me-29-minutes-and-ill-teach-you-to-make-1-million.md` | `knowledge/daniel-priestley-zero-to-seven-figures.md` |
| 2 | [The $1 Million Landing Page](https://www.youtube.com/watch?v=az1Zh-FNSno) | `raw/2026-07-19-daniel-priestley-the-1-million-landing-page-works-for-normal-people.md` | `knowledge/daniel-priestley-million-dollar-landing-page.md` |
| 3 | [How to Become Famous in Your Industry](https://www.youtube.com/watch?v=QI_aGzPUOK8) | `raw/2026-07-19-daniel-priestley-how-to-become-famous-in-your-industry-and-make-1-million.md` | `knowledge/daniel-priestley-famous-in-your-industry.md` |
| 4 | [25 Years of Sales Knowledge in 34 Minutes](https://www.youtube.com/watch?v=tVLnzcoM5LE) | `raw/2026-07-19-daniel-priestley-25-years-of-sales-knowledge-in-34-minutes.md` | `knowledge/sales/daniel-priestley-25-years-of-sales-knowledge.md` |
| 5 | [7 Unsexy Habits That Build a $1 Million Business](https://www.youtube.com/watch?v=tUeK1CaJT7Q) | `raw/2026-07-19-daniel-priestley-7-unsexy-habits-that-build-a-1-million-business.md` | `knowledge/daniel-priestley-7-unsexy-habits.md` |
| 6 | [Why You Must Stop Selling Your Time for Money](https://www.youtube.com/watch?v=wkPatBreE9w) | `raw/2026-07-19-daniel-priestley-why-you-must-stop-selling-your-time-for-money.md` | `knowledge/daniel-priestley-stop-selling-time.md` |
| 7 | [25 Years of Money Advice in 31 Minutes](https://www.youtube.com/watch?v=FWBl8RtnQRE) | `raw/2026-07-19-daniel-priestley-25-years-of-money-advice-in-31-minutes.md` | `knowledge/daniel-priestley-25-years-of-money-advice.md` |
| 8 | [Business Is Easy After You Achieve Product Market Fit](https://www.youtube.com/watch?v=jK-QDdeKFl4) | `raw/2026-07-19-daniel-priestley-business-is-easy-after-you-achieve-product-market-fit.md` | `knowledge/daniel-priestley-product-market-fit.md` |

Note: `tVLnzcoM5LE` was listed twice in the input; it was processed once and
saved once.

## Key themes across the videos

- **Product-market fit is the gate.** Everything else (scale, hiring, capital) comes after it.
- **The offer ladder is directionally correct.** The free scorecard, diagnostic, audit, blueprint, and advisor rungs map to Priestley's gift, product for prospects, core offer, and product for clients. The missing layer is outcome-based gold/silver/bronze packaging and visual aids.
- **Sales is a system, not a talent.** LAPS (Leads → Appointments → Presentations → Sales), the 10-component presentation, and disciplined follow-up are learnable and repeatable.
- **Lead generation is upstream of everything.** Daily content, 70-100 outreaches per day, and a high-converting scorecard landing page are the engine.
- **Time-for-money is being commoditized by AI.** The durable move is to productize expertise, sell outcomes, and use AI for execution while the founder focuses on conviction, judgment, taste, commercial outcomes, and improving the system.
- **Environment and team are prerequisites.** Perfect repeatable weeks, Monday/Friday meetings, a weekly introduction workshop, and mentors 5-10x ahead are not optional at the seven-figure stage.

## Implications filed

See `progress/2026-07-19-youtube-ingest-implications.md` for proposed updates to:

- `playbooks/offer-playbook.md` (gold/silver/bronze, LAPS dashboard, follow-up, visual aids, product-market fit test)
- `playbooks/operator-guide.md` (perfect repeatable week, Monday/Friday meetings, introduction workshop, quarterly retreat, environment)
- `SKILL.md` (social pitch, SALT profile, product-market fit before scale)
- `knowledge/CLAUDE.md` (content cadence, long-form targets, prolific beats perfect, annual big message)
- `content/backlog.md` (derived content seeds)
- `playbooks/tool-ideas/backlog.md` (AI audit platform, scorecard follow-up automation)

No playbook or skill files were edited directly; only the implications note was
written.

## Skipped / issues

- One URL was duplicated in the input; handled once.
- All eight transcripts were successfully fetched using `youtube-transcript-api` in a temporary venv. No videos were skipped.

## Next actions

1. Review and approve the proposed playbook/skill implications.
2. Run the scorecard landing page against Priestley's hook/subheading/value-proposition/credibility/CTA framework.
3. Define the first 30 one-to-one sales meetings to validate the refined offer packages.
4. Set the first quarterly planning retreat and document the perfect repeatable week.

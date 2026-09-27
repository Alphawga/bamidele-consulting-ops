# Tool-ideas backlog

The IP-generation inbox. Working on a build (own repos or client engagements like Okoh)
surfaces things generic enough to stand alone: an engine, an algorithm, a recurring pattern.
Log it here as a one-line seed. The `tool-scout` skill later researches and ranks it into a
build-vs-open-source-vs-sell recommendation.

Newest on top. Format:

`YYYY-MM-DD · [repo] · owned|client-engagement · idea-angle`

- `owned`: you hold the IP outright (personal repos, bamidele-consulting-ops/-site).
- `client-engagement`: built under a client engagement (e.g. Okoh) — flagged, not cleared.
  Extracting or selling this requires checking the contract/client relationship first.

See the `tool-scout` skill for the full Capture/Scout workflow and the ownership gate.

---

- 2026-09-27 · Okoh ERP (`src/lib/accounting/posting-engines.ts`, GRN flow) · client-engagement · Tool-scout top pick (see `reports/2026-09-27.md`): no standalone small-business GRNI matcher found on the market — enterprise AP tools (Stampli, PLANERGY, openecx) and full open-source ERPs (ERPNext, LedgerSMB) cover it, nothing lighter-weight. Worth a build/sell conversation once Alpha clears extraction rights with Okoh.
- 2026-07-14 · Okoh ERP (`src/lib/accounting/bank-sync/`) · client-engagement · Bank-feed transaction matching + auto-posting engine (Plaid connect, rule-based matcher, GL posting, exclude flow) — generic enough for any small business doing manual bank reconciliation.
- 2026-07-14 · Okoh ERP (`src/lib/accounting/posting-engines.ts`, GRN flow) · client-engagement · Idempotent GRN-to-GL posting engine (Dr Inventory / Cr GRNI, two creation paths reconciled to one ledger effect) — the receiving-to-ledger gap most small-business inventory tools leave manual.

---

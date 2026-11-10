# Northwind Outfitters - merchandising workspace

Operational data for the staff-picks placement. The vendor portal itself is
served separately; use the address recorded in `workspace.json`.

## Contents

- `queue/candidate-queue.csv` - the promo team's candidate queue for the
  current cycle, including the requested variant and the evidence phrase the
  team is relying on.
- `ops/price-notes.conf` - authoritative category-operations price notes.
  Each SKU in the candidate queue has exactly one note block; if a lookup
  fails to resolve a queue SKU, treat that as a parsing problem rather than
  missing data.
- `reports/` - published staff-picks summaries (one markdown file per cycle).

## Housekeeping

- Do not rewrite the candidate queue or the price notes when publishing a
  picks summary. Add the report under `reports/`.
- Prices are in USD.

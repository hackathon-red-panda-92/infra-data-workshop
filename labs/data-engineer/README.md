# Shared follow-along lab - clean, analyse, and package data locally

The facilitator and attendees use the same prompts in [`LAB.md`](LAB.md). The
exercise takes about 50 minutes and requires Python, GitHub Copilot, and no Azure
subscription.

## Source files

- [`sales_january.csv`](sales_january.csv): deliberately inconsistent money,
  text, and spacing.
- [`sales_february.csv`](sales_february.csv): different headers and date format.
- [`product_prices.csv`](product_prices.csv): list-price lookup data.

## Outputs created during the lab

- `clean_sales.py`
- `sales_clean.csv`
- `analysis.md`
- `data-quality-report.md`
- `handoff/`
- `sales-handoff.zip`

Generated outputs are ignored by Git. The three source CSVs must remain
unchanged.
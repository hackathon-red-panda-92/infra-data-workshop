# Data Engineer lab - clean, analyse, and package data locally

Everyone follows the facilitator through this lab after the Systems Administrator
lab. No Azure subscription or coding experience is required.

**Maximum time: 25 minutes. Stop after the final checkpoint.**

For every step: enter the same prompt as the facilitator, read the suggestion,
approve only understood actions, and verify the result. Keep source files unchanged.

## Setup

Open `labs/data-engineer`. Confirm Copilot can see `sales_january.csv`,
`sales_february.csv`, and `product_prices.csv`.

## 1. Inspect the data (minutes 0-4)

> Read the three CSV files. Do not change anything. Summarise the inconsistencies
> in column names, dates, money values, spaces, and capitalisation, then propose
> a four-step cleaning plan.

**Checkpoint:** both sales files and the product lookup are included in the plan.

## 2. Clean and combine (minutes 4-11)

> Create `clean_sales.py` to combine the January and February files, fix the
> identified issues, join the product list, and write `sales_clean.csv`. Never
> modify the source CSV files. Explain the script briefly, then run it.

**Checkpoint:** `sales_clean.csv` contains rows from both months.

## 3. Answer business questions (minutes 11-16)

> Using `sales_clean.csv`, calculate revenue by region and month, the top-selling
> product by revenue, and the five largest discounts from list price. Run the
> analysis and save actual results as clear tables in `analysis.md`.

**Checkpoint:** the document contains calculated results, not only code or instructions.

## 4. Validate and summarise (minutes 16-21)

> Validate source and cleaned row counts, date range, total units, total revenue,
> duplicates, and missing values. Save the evidence as `data-quality-report.md`.
> Add three evidence-based findings and one limitation to the top of
> `analysis.md`. Flag mismatches instead of guessing.

**Checkpoint:** every management claim is supported by a calculation in the files.

## 5. Package the handoff (minutes 21-25)

> Create `data-handoff` containing `sales_clean.csv`, `analysis.md`, and
> `data-quality-report.md`. Add a `README.md` explaining the files and how to
> rerun `clean_sales.py`, then create `data-handoff.zip`. Do not upload or send
> anything.

**Final checkpoint:** the handoff contains exactly four files and the ZIP exists.
Stop here; the hands-on session is complete.

## Safety

- Keep the source CSV files unchanged.
- Never paste secrets, real customer data, or confidential information into Copilot.
- Require evidence for totals and claims.
- Keep all outputs local.
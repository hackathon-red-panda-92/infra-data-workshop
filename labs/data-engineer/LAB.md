# Shared follow-along lab - clean, analyse, and package data locally

The facilitator and every attendee complete these steps together. Wait for the
facilitator before moving to the next step. You do not need coding experience or
an Azure subscription.

**Time:** 50 minutes

## The loop

For every step:

1. **Prompt:** enter the facilitator's quoted prompt in Copilot.
2. **Suggestion:** read what Copilot proposes.
3. **Run:** approve only the actions you understand.
4. **Refine:** ask for one change at a time.
5. **Sanity-check:** verify the files and numbers.

All work stays in this folder. The original CSV files must remain unchanged.

## Before the timer starts

1. Open this repository in GitHub Codespaces or the GitHub Copilot app.
2. Open `labs/data-engineer` as your working folder.
3. Start Copilot and confirm it can see `sales_january.csv`,
   `sales_february.csv`, and `product_prices.csv`.
4. Do not create files yet. Wait for the facilitator.

## 1. Inspect the source files (minutes 0-7)

Enter this prompt exactly as the facilitator does:

> Read the three CSV files in this folder. Do not change anything yet. In plain
> English, list the inconsistencies that must be fixed before the sales files can
> be combined, including column names, date formats, money values, spaces, and
> capitalisation. Then propose a short plan.

Compare Copilot's list with the facilitator's. Ask about any difference before
continuing.

## 2. Clean and combine the data (minutes 7-17)

> Create a Python script named `clean_sales.py` that combines the January and
> February sales files, fixes every issue in the plan, joins the product list,
> and writes a new file named `sales_clean.csv`. Never modify the three source
> CSV files. Explain the script in five bullets, then run it.

Read the explanation and approve the file creation and run. Open
`sales_clean.csv` and confirm that it contains rows from both months.

If the action fails, use the same recovery prompt as the facilitator:

> Explain the error in plain English. Make only the smallest necessary fix, then
> run the script again.

## 3. Answer business questions (minutes 17-27)

> Using `sales_clean.csv`, calculate total revenue by region and by month, the
> top-selling product by revenue, and the five largest discounts from list
> price. Run the analysis and save the results as `analysis.md` with clear tables.

Do not accept an answer that only describes code. Copilot must run the analysis
and write the actual results.

## 4. Validate the result (minutes 27-37)

> Validate the cleaned data. Report the source row count, cleaned row count,
> date range, total units, total revenue, duplicate count, missing-value count,
> and three sample rows. Recalculate totals independently from the cleaned CSV.
> Save the evidence as `data-quality-report.md`. Flag any mismatch instead of
> hiding or guessing it.

Compare the row counts and totals with the facilitator. If yours differ, stop
and ask Copilot to identify the first differing row or assumption.

## 5. Improve the handoff (minutes 37-44)

> Review `analysis.md` and `data-quality-report.md` for a non-technical manager.
> Add a short executive summary to `analysis.md` with three findings and one
> limitation. Use only facts calculated from the files; do not invent figures.

Read the summary. Ask Copilot which file and calculation supports each claim.

## 6. Create and inspect the local package (minutes 44-50)

> Create a local folder named `handoff` containing copies of `sales_clean.csv`,
> `analysis.md`, and `data-quality-report.md`. Add a `README.md` that explains
> what each file contains and how to rerun `clean_sales.py`. Create
> `sales-handoff.zip` from that folder. Do not upload or send anything.

Open the `handoff` folder and confirm it contains exactly four files. The ZIP is
the finished local deliverable; there is no cloud upload or teardown.

## Safety rules

- Read every proposed action before approving it.
- Keep the three source CSV files unchanged.
- Use only the fictitious workshop data. Never paste secrets or real customer
  information into Copilot.
- Require evidence for totals and claims. Copilot drafts; you decide.
- Keep all outputs local during the workshop.

## If the group finishes early

Use one prompt together:

> Create a bar chart of monthly revenue as `monthly-revenue.png`, add it to the
> handoff folder, update the handoff README, and rebuild the ZIP.
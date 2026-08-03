# GitHub Copilot for Non-Coders

## Shared facilitator and attendee guide - 10-minute intro + 50-minute follow-along

The facilitator and attendees use this same guide. During the hands-on, the
facilitator performs each prompt while attendees enter the same prompt and wait
at each checkpoint. No Azure subscription, cloud deployment, upload, cost, or
teardown is part of this workshop.

## Outcome

Together, the group turns three messy CSV exports into a clean dataset, answers
business questions, validates the numbers, and creates a local handoff package.
No coding experience is required.

## Before the session

- Confirm every participant has a GitHub account with Copilot access.
- Use GitHub Codespaces, or the GitHub Copilot app with Git and Python 3.
- Open <https://github.com/marinfrankovic/copilot-workshop-samples>.
- Open `labs/data-engineer/LAB.md` but do not begin until the facilitator does.
- The facilitator should open the same repository and use a clean workspace.
- Do not use real customer data, secrets, or confidential information.

## Run of show

| Time | Shared activity |
|---|---|
| 0-10 | Facilitator gives the existing short introduction. Attendees open the repository and lab. |
| 10-17 | Everyone inspects the three source files with the same prompt. |
| 17-27 | Everyone creates and runs the cleaning script. |
| 27-37 | Everyone runs the business analysis. |
| 37-47 | Everyone validates row counts, totals, dates, duplicates, and missing values. |
| 47-54 | Everyone improves the manager handoff with evidence-based findings. |
| 54-60 | Everyone creates and inspects the local handoff package. |

## The loop

Repeat this rhythm for every step:

1. **Prompt:** enter the quoted prompt in Copilot.
2. **Suggestion:** read what Copilot proposes.
3. **Run:** approve only actions you understand.
4. **Refine:** ask for one change at a time.
5. **Sanity-check:** verify the files and numbers.

The facilitator reads each prompt aloud, enters it, and pauses. Attendees enter
the same prompt and do not move ahead until the facilitator reaches the checkpoint.

## Setup checkpoint

### GitHub Codespaces

1. Select **Code > Codespaces > Create codespace on main**.
2. Open **Terminal > New Terminal** and run `copilot`.
3. Trust the folder and complete `/login` if prompted.
4. Open `labs/data-engineer`.

### GitHub Copilot app

1. Add `https://github.com/marinfrankovic/copilot-workshop-samples.git` as a project.
2. Start an Interactive session.
3. Ask Copilot to show `labs/data-engineer/LAB.md`.

**Checkpoint:** everyone can see `sales_january.csv`, `sales_february.csv`, and
`product_prices.csv`.

## 1. Inspect the source files

Everyone enters:

> Read the three CSV files in this folder. Do not change anything yet. In plain
> English, list the inconsistencies that must be fixed before the sales files can
> be combined, including column names, date formats, money values, spaces, and
> capitalisation. Then propose a short plan.

**Checkpoint:** compare the lists. Resolve differences before continuing.

## 2. Clean and combine the data

Everyone enters:

> Create a Python script named `clean_sales.py` that combines the January and
> February sales files, fixes every issue in the plan, joins the product list,
> and writes a new file named `sales_clean.csv`. Never modify the three source
> CSV files. Explain the script in five bullets, then run it.

Read the explanation before approving the run.

**Checkpoint:** open `sales_clean.csv` and confirm it contains both months.

If anyone gets an error, everyone practises the same recovery prompt:

> Explain the error in plain English. Make only the smallest necessary fix, then
> run the script again.

## 3. Answer business questions

Everyone enters:

> Using `sales_clean.csv`, calculate total revenue by region and by month, the
> top-selling product by revenue, and the five largest discounts from list
> price. Run the analysis and save the results as `analysis.md` with clear tables.

**Checkpoint:** Copilot must run the analysis and write actual results, not only
describe code.

## 4. Validate the result

Everyone enters:

> Validate the cleaned data. Report the source row count, cleaned row count,
> date range, total units, total revenue, duplicate count, missing-value count,
> and three sample rows. Recalculate totals independently from the cleaned CSV.
> Save the evidence as `data-quality-report.md`. Flag any mismatch instead of
> hiding or guessing it.

**Checkpoint:** compare row counts and totals with the facilitator. If a result
differs, ask Copilot to identify the first differing row or assumption.

## 5. Improve the handoff

Everyone enters:

> Review `analysis.md` and `data-quality-report.md` for a non-technical manager.
> Add a short executive summary to `analysis.md` with three findings and one
> limitation. Use only facts calculated from the files; do not invent figures.

**Checkpoint:** ask which file and calculation supports each claim.

## 6. Create and inspect the local package

Everyone enters:

> Create a local folder named `handoff` containing copies of `sales_clean.csv`,
> `analysis.md`, and `data-quality-report.md`. Add a `README.md` that explains
> what each file contains and how to rerun `clean_sales.py`. Create
> `sales-handoff.zip` from that folder. Do not upload or send anything.

**Final checkpoint:** the `handoff` folder contains exactly four files and the ZIP
exists. All outputs remain local. There is no cloud teardown.

## Safety rules

- Read every proposed action before approving it.
- Keep the three source CSV files unchanged.
- Never paste secrets, real customer data, or confidential information into Copilot.
- Require evidence for totals and claims. Copilot drafts; people decide.
- Keep all outputs local during the workshop.

## Wrap-up

The skill is not memorising Python. It is describing an outcome, reviewing the
proposal, running it deliberately, refining one issue at a time, and checking the
evidence before using the result.
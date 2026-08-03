# Attendee Guide - GitHub Copilot for Non-Coders

**10-minute introduction + 50-minute hands-on. No coding experience and no Azure
access required. Everything runs locally.**

Use this guide to follow along live or to redo the session from the recording.
Every prompt below is the exact prompt the facilitator enters, in the same order,
so you can pause the recording at any step and catch up.

## How to use this guide

- A quoted block is a **prompt**. Type it into Copilot exactly as written.
- After each prompt: read what Copilot proposes, approve only what you
  understand, then check the **Checkpoint** before moving on.
- If something fails, use the recovery prompt:
  > Explain the error in plain English and make only the smallest necessary fix.
- Ask for **one change at a time**. Copilot drafts; you decide.

## The loop

1. **Prompt** - describe the outcome you want.
2. **Suggestion** - read what Copilot proposes.
3. **Run** - approve only actions you understand.
4. **Refine** - ask for one change at a time.
5. **Sanity-check** - verify the files and the evidence.

## Before the session

- A GitHub account with Copilot access.
- Either GitHub Codespaces (nothing to install) or the GitHub Copilot app for
  Windows with Git and Python 3.
- Open <https://github.com/marinfrankovic/copilot-workshop-samples> and follow
  [`START-HERE.md`](../START-HERE.md).

### GitHub Codespaces

1. Select **Code > Codespaces > Create codespace on main**.
2. Open **Terminal > New Terminal** and run `copilot`.
3. Trust the folder and complete `/login` if prompted.

### GitHub Copilot app

1. Add `https://github.com/marinfrankovic/copilot-workshop-samples.git` as a project.
2. Start an **Interactive** session.
3. Ask Copilot to show `labs/systems-engineer/LAB.md`.

## Run of show

| Time | What happens |
|---|---|
| 0-10 | Introduction, the loop, the magic moment, and the safety rules. Watch only. |
| 10-35 | Lab 1 - Systems Administrator. You drive; stop at the final checkpoint. |
| 35-58 | Lab 2 - Data Engineer. You drive; stop at the final checkpoint. |
| 58-60 | Wrap and takeaways. |

Each lab is capped at 25 minutes. If you fall behind, skip refinements and move
to the next numbered step - the checkpoints matter more than polish.

## Safety rules

- Read before you run. Approve only the actions you understand.
- Leave the source files unchanged; every lab writes new files.
- Never paste secrets, keys, customer data, or confidential information.
- Demand evidence: every number and recommendation must cite a line in a file.
- Everything stays local. Nothing is deployed, uploaded, or charged.

---

# Minutes 0-10 - Introduction

Watch the facilitator run the magic moment on `magic-moment/server.log`: one
messy log file becomes a plain-English diagnosis and a clean table in under a
minute. These are the five prompts used, if you want to repeat them later.

1. > Look at server.log. In plain English, what is this service doing and what went wrong? Assume I'm not reading every line.
2. > What is the most likely root cause, and what fixed it? Quote the lines that prove it.
3. > Turn the log into a clean table with columns timestamp, level, component, message - normalise the two timestamp formats.
4. > Count events by level and show the error rate per minute so I can see the spike and the recovery.
5. > How many ERROR lines did you find, and what's the first and last timestamp? I want to trust this.

**What to notice:** comprehension, then structure, then quantify - and a
sanity-check at the end. That is the same rhythm you use in both labs.

---

# Minutes 10-35 - Lab 1: Systems Administrator

Audit a server fleet locally. Open `labs/systems-engineer` and confirm Copilot
can see `operations-brief.md`, `server-inventory.csv`, `service-status.csv`, and
`sample-error.txt`.

Full lab file: [`labs/systems-engineer/LAB.md`](../labs/systems-engineer/LAB.md)

## 1. Understand the audit (lab minutes 0-4)

> Read `operations-brief.md`, `server-inventory.csv`, and `service-status.csv`.
> Do not change anything. Summarise the health rules and propose a four-step audit
> plan in plain English.

**Checkpoint:** patch age, disk, backup, endpoint protection, service status, and
startup type are covered.

## 2. Run the local audit (lab minutes 4-11)

> Create `audit_servers.py` to apply every rule in `operations-brief.md`. Write
> one row per server to `server-health.csv` with hostname, role, environment,
> owner, risk level, failed-check count, and findings. Keep source files
> unchanged. Explain the script briefly, then run it.

**Checkpoint:** the output contains ten servers and a mix of risk levels.

## 3. Prioritise remediation (lab minutes 11-16)

> Create `remediation-plan.md` from `server-health.csv`. Sort by risk and
> hostname, show the evidence, recommend the next action, and include owner and
> maintenance window. Do not claim any remediation was performed.

**Checkpoint:** critical systems appear first and every recommendation cites
evidence.

## 4. Troubleshoot and validate (lab minutes 16-21)

> Read `sample-error.txt`, explain the field-name failure, and confirm whether
> `audit_servers.py` uses the correct source header. Make only the smallest fix
> if needed. Then validate that every inventory server appears exactly once and
> risk levels match failed-check counts. Save the evidence as
> `validation-report.md`.

**Checkpoint:** the report gives row counts, duplicate count, missing-server
count, audit date, and any discrepancy.

## 5. Package the handoff (lab minutes 21-25)

> Create `sysadmin-handoff` containing `server-health.csv`,
> `remediation-plan.md`, and `validation-report.md`. Add a `README.md` explaining
> the files and how to rerun `audit_servers.py`, then create
> `sysadmin-handoff.zip`. Do not connect to servers or upload anything.

**Final checkpoint:** the handoff contains exactly four files and the ZIP exists.
Stop here and move to Lab 2.

---

# Minutes 35-58 - Lab 2: Data Engineer

Clean, analyse, and package data locally. Open `labs/data-engineer` and confirm
Copilot can see `sales_january.csv`, `sales_february.csv`, and
`product_prices.csv`.

Full lab file: [`labs/data-engineer/LAB.md`](../labs/data-engineer/LAB.md)

## 1. Inspect the data (lab minutes 0-4)

> Read the three CSV files. Do not change anything. Summarise the inconsistencies
> in column names, dates, money values, spaces, and capitalisation, then propose
> a four-step cleaning plan.

**Checkpoint:** both sales files and the product lookup are included in the plan.

## 2. Clean and combine (lab minutes 4-11)

> Create `clean_sales.py` to combine the January and February files, fix the
> identified issues, join the product list, and write `sales_clean.csv`. Never
> modify the source CSV files. Explain the script briefly, then run it.

**Checkpoint:** `sales_clean.csv` contains rows from both months.

## 3. Answer business questions (lab minutes 11-16)

> Using `sales_clean.csv`, calculate revenue by region and month, the top-selling
> product by revenue, and the five largest discounts from list price. Run the
> analysis and save actual results as clear tables in `analysis.md`.

**Checkpoint:** the document contains calculated results, not only code or
instructions.

## 4. Validate and summarise (lab minutes 16-21)

> Validate source and cleaned row counts, date range, total units, total revenue,
> duplicates, and missing values. Save the evidence as `data-quality-report.md`.
> Add three evidence-based findings and one limitation to the top of
> `analysis.md`. Flag mismatches instead of guessing.

**Checkpoint:** every management claim is supported by a calculation in the files.

## 5. Package the handoff (lab minutes 21-25)

> Create `data-handoff` containing `sales_clean.csv`, `analysis.md`, and
> `data-quality-report.md`. Add a `README.md` explaining the files and how to
> rerun `clean_sales.py`, then create `data-handoff.zip`. Do not upload or send
> anything.

**Final checkpoint:** the handoff contains exactly four files and the ZIP exists.

---

# Minutes 58-60 - Wrap

You produced two validated handoff packages by describing outcomes in plain
English. Take home:

- The loop: prompt, suggestion, run, refine, sanity-check.
- Ask for evidence, not confidence.
- Start from the outcome you want, not from the syntax.

The repository stays available: <https://github.com/marinfrankovic/copilot-workshop-samples>

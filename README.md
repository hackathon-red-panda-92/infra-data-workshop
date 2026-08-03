# GitHub Copilot for Non-Coders - Workshop Files

Hands-on files for a **10-minute introduction and 50-minute follow-along lab**.
The facilitator and attendees use the same prompts at the same time. You describe
the outcome in plain English, GitHub Copilot proposes and runs the work, and you
review every action. **No coding experience or Azure access is needed.**

## Start here

Open [`START-HERE.md`](START-HERE.md), choose GitHub Codespaces or the GitHub
Copilot app, and then open the shared lab:

[`labs/data-engineer/LAB.md`](labs/data-engineer/LAB.md)

The group turns three messy CSV exports into a clean dataset, answers business
questions, validates the result, and creates a local handoff package.

The rhythm is **Prompt -> Suggestion -> Run -> Refine -> Sanity-check**.

## What you need

- A laptop with a web browser.
- A GitHub account with Copilot access.
- GitHub Codespaces, or the GitHub Copilot app with Git and Python.
- No Azure subscription, cloud account, or paid resource.

## Repository contents

```text
.
|-- START-HERE.md
|-- SETUP.md
|-- CODESPACES.md
|-- guides/
|   |-- Attendee Guide - 10 min talk 50 min handson.docx
|   `-- Facilitator Guide - 10 min talk 50 min handson.docx
|-- magic-moment/
|   `-- server.log
`-- labs/data-engineer/
    |-- LAB.md
    |-- sales_january.csv
    |-- sales_february.csv
    `-- product_prices.csv
```

## Golden rules

- Read every proposed action before approving it.
- Keep source files unchanged and write new outputs.
- Never paste secrets, customer data, or confidential information into Copilot.
- Require evidence for totals and claims. Copilot drafts; you decide.
- Keep all workshop outputs local.

## Sample data

All names, emails, and numbers are fictitious. There is no real personal data in
the sample files.

## License

[MIT](LICENSE)
# GitHub Copilot for Non-Coders - Workshop Files

Hands-on files for a **10-minute introduction and 50-minute follow-along lab**.
The workshop keeps separate Systems Administrator and Data Engineer labs. During
the 50-minute hands-on, everyone follows the facilitator through both labs: up to
25 minutes each. **No coding experience or Azure access is needed.**

## Start here

Open [`START-HERE.md`](START-HERE.md), choose GitHub Codespaces or the GitHub
Copilot app, and complete the labs in this order:

- [Systems Administrator](labs/systems-engineer/LAB.md)
- [Data Engineer](labs/data-engineer/LAB.md)

1. The Systems Administrator lab audits local server exports.
2. The Data Engineer lab cleans and analyses local sales exports.

Each lab creates a validated local handoff package and stops at minute 25.

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
|   |-- README.md
|   `-- ATTENDEE-GUIDE.md
|-- magic-moment/
|   `-- server.log
`-- labs/
    |-- systems-engineer/
    |   |-- LAB.md
    |   |-- server-inventory.csv
    |   |-- service-status.csv
    |   |-- operations-brief.md
    |   `-- sample-error.txt
    `-- data-engineer/
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
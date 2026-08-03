# Systems Administrator lab - audit a server fleet locally

This is a separate role-based track. Follow the facilitator through each step if
the Systems Administrator track is selected. No Azure subscription, remote
server connection, or coding experience is required.

**Time:** 50 minutes

## The loop

For every step: prompt, read the suggestion, approve the run, refine one issue,
and sanity-check the result. The source files must remain unchanged.

## Before the timer starts

Open `labs/systems-engineer` and confirm Copilot can see
`operations-brief.md`, `server-inventory.csv`, `service-status.csv`, and
`sample-error.txt`. Wait for the facilitator before continuing.

## 1. Understand the operational brief (minutes 0-7)

> Read `operations-brief.md`, `server-inventory.csv`, and `service-status.csv`.
> Do not change anything yet. Explain the health rules, identify the available
> evidence, and propose a short audit plan in plain English.

**Checkpoint:** the plan covers patch age, disk space, backup, endpoint
protection, service status, and startup type.

## 2. Build and run the local audit (minutes 7-18)

> Create `audit_servers.py` to apply every rule in `operations-brief.md` to the
> two CSV exports. Write one row per server to `server-health.csv`, including
> hostname, role, environment, owner, risk level, failed-check count, and
> findings. Keep the source files unchanged. Explain the script in five bullets,
> then run it.

**Checkpoint:** `server-health.csv` contains ten servers and includes both
healthy and unhealthy results.

## 3. Create the remediation plan (minutes 18-28)

> Using `server-health.csv`, create `remediation-plan.md`. Sort servers by risk
> and hostname, explain the evidence for each finding, recommend the next action,
> and include the owner and maintenance window. Do not claim that any action was
> performed.

**Checkpoint:** critical and high-risk servers appear before healthy servers.

## 4. Practise troubleshooting (minutes 28-36)

> Read `sample-error.txt`. Explain the failure in plain English, identify the
> exact mismatch that caused it, and make only the smallest correction needed in
> `audit_servers.py`. Then rerun the audit.

**Checkpoint:** Copilot changes the incorrect field name only; it does not rename
the source column or replace the whole script.

## 5. Validate the audit (minutes 36-44)

> Independently validate the audit output. Confirm every inventory server appears
> exactly once, risk levels match the failed-check counts, findings match the
> source values, and no source file changed. Save the evidence as
> `validation-report.md`. Flag mismatches instead of hiding them.

**Checkpoint:** the report states the audit date, source and output row counts,
duplicate count, missing-server count, and any discrepancies.

## 6. Package the local handoff (minutes 44-50)

> Create `sysadmin-handoff` containing copies of `server-health.csv`,
> `remediation-plan.md`, and `validation-report.md`. Add a `README.md` explaining
> the files, the health rules, and how to rerun `audit_servers.py`. Create
> `sysadmin-handoff.zip`. Do not connect to servers or upload anything.

**Final checkpoint:** the handoff folder contains exactly four files and the ZIP
exists. All work remains local.

## Safety rules

- Read every proposed action before approval.
- Never modify source exports or claim a remediation was performed.
- Never use real credentials, secrets, or customer data.
- Require evidence for every risk and recommendation.
- Keep all outputs local during the workshop.
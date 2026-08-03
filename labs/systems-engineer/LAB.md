# Systems Administrator lab - audit a server fleet locally

Everyone follows the facilitator through this lab before moving to the Data
Engineer lab. No Azure subscription, remote connection, or coding experience is
required.

**Maximum time: 25 minutes. Stop after the final checkpoint.**

For every step: enter the same prompt as the facilitator, read the suggestion,
approve only understood actions, and verify the result. Keep source files unchanged.

## Setup

Open `labs/systems-engineer`. Confirm Copilot can see `operations-brief.md`,
`server-inventory.csv`, `service-status.csv`, and `sample-error.txt`.

## 1. Understand the audit (minutes 0-4)

> Read `operations-brief.md`, `server-inventory.csv`, and `service-status.csv`.
> Do not change anything. Summarise the health rules and propose a four-step audit
> plan in plain English.

**Checkpoint:** patch age, disk, backup, endpoint protection, service status,
and startup type are covered.

## 2. Run the local audit (minutes 4-11)

> Create `audit_servers.py` to apply every rule in `operations-brief.md`. Write
> one row per server to `server-health.csv` with hostname, role, environment,
> owner, risk level, failed-check count, and findings. Keep source files
> unchanged. Explain the script briefly, then run it.

**Checkpoint:** the output contains ten servers and a mix of risk levels.

## 3. Prioritise remediation (minutes 11-16)

> Create `remediation-plan.md` from `server-health.csv`. Sort by risk and
> hostname, show the evidence, recommend the next action, and include owner and
> maintenance window. Do not claim any remediation was performed.

**Checkpoint:** critical systems appear first and every recommendation cites evidence.

## 4. Troubleshoot and validate (minutes 16-21)

> Read `sample-error.txt`, explain the field-name failure, and confirm whether
> `audit_servers.py` uses the correct source header. Make only the smallest fix
> if needed. Then validate that every inventory server appears exactly once and
> risk levels match failed-check counts. Save the evidence as
> `validation-report.md`.

**Checkpoint:** the report gives row counts, duplicate count, missing-server
count, audit date, and any discrepancy.

## 5. Package the handoff (minutes 21-25)

> Create `sysadmin-handoff` containing `server-health.csv`,
> `remediation-plan.md`, and `validation-report.md`. Add a `README.md` explaining
> the files and how to rerun `audit_servers.py`, then create
> `sysadmin-handoff.zip`. Do not connect to servers or upload anything.

**Final checkpoint:** the handoff contains exactly four files and the ZIP exists.
Stop here and move to the Data Engineer lab.

## Safety

- Never modify source exports or claim a remediation was performed.
- Never use real credentials, secrets, or customer data.
- Require evidence for every risk and recommendation.
- Keep all outputs local.
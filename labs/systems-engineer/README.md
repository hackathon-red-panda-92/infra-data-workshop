# Systems Administrator track - audit a server fleet locally

Use GitHub Copilot to inspect sample server inventory and service exports,
generate a repeatable health check, prioritise remediation, and create a local
handoff package. No Azure subscription or remote server access is required.

Start with [`LAB.md`](LAB.md) and stop at its 25-minute final checkpoint.

## Source files

- [`operations-brief.md`](operations-brief.md): health rules and required outputs.
- [`server-inventory.csv`](server-inventory.csv): fictitious server ownership,
  patch, disk, backup, and endpoint-protection data.
- [`service-status.csv`](service-status.csv): fictitious required-service status.
- [`sample-error.txt`](sample-error.txt): a realistic local script failure to diagnose.

## Outputs created during the lab

- `audit_servers.py`
- `server-health.csv`
- `remediation-plan.md`
- `validation-report.md`
- `sysadmin-handoff/`
- `sysadmin-handoff.zip`

The source files remain unchanged and all generated outputs stay local.
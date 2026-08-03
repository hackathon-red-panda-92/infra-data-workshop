# Operations brief - Contoso server health audit

Contoso operations has two local exports: a server inventory and a required
service status report. Produce a repeatable audit without connecting to any
server or cloud service.

## Health rules

A server needs attention when any of these conditions is true:

- its last successful patch is more than 30 days old;
- free disk space is below 15 percent;
- backup status is not `Success`;
- endpoint protection is not `Healthy`;
- a required service is not `Running`; or
- a required service does not use `Automatic` startup.

## Required outputs

- One row per server in `server-health.csv`.
- Columns for hostname, role, environment, owner, risk level, failed-check count,
  and a plain-English list of findings.
- Risk levels: `Critical` for three or more failed checks, `High` for two,
  `Medium` for one, and `Healthy` for none.
- A remediation plan ordered by risk, then hostname.
- A validation report proving every source server appears exactly once.

## Constraints

- Keep both source CSV files unchanged.
- Treat blank or malformed values as findings; never guess missing values.
- Use the current date when calculating patch age and state that date in reports.
- Do not connect to servers, Azure, or any other external service.
- Do not include credentials, secrets, or real company data.
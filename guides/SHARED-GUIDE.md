# GitHub Copilot for Non-Coders

## Shared facilitator and attendee guide - 10-minute intro + 50-minute hands-on

The workshop has two separate role-based tracks:

- **Systems Administrator:** audit local server inventory and service exports,
  prioritise remediation, validate the findings, and package a local handoff.
- **Data Engineer:** clean local sales exports, answer business questions,
  validate the numbers, and package a local handoff.

Before the session, the facilitator selects the track for that delivery. The
facilitator and attendees then use the same track instructions, enter the same
prompts, and pause at the same checkpoints. Do not combine or switch tracks
during the 50-minute lab.

No Azure subscription, cloud deployment, remote connection, upload, cost, or
teardown is required for either track.

## Before the session

- Confirm everyone has a GitHub account with Copilot access.
- Use GitHub Codespaces, or the GitHub Copilot app with Git and Python 3.
- Open <https://github.com/marinfrankovic/copilot-workshop-samples>.
- Select either `labs/systems-engineer/LAB.md` or
  `labs/data-engineer/LAB.md` for the delivery.
- The facilitator opens the same lab in a clean workspace.
- Use only the fictitious source data included in the selected lab.

## Run of show

| Time | Shared activity |
|---|---|
| 0-10 | Facilitator gives the existing short introduction. Attendees open the repository and selected lab. |
| 10-17 | Everyone inspects the selected track's source files and agrees on a plan. |
| 17-28 | Everyone creates and runs the local processing or audit script. |
| 28-38 | Everyone produces role-specific analysis or remediation output. |
| 38-47 | Everyone troubleshoots or validates the output against source evidence. |
| 47-60 | Everyone completes validation and creates the local handoff package. |

## The loop

Repeat this rhythm for every step:

1. **Prompt:** enter the quoted prompt in Copilot.
2. **Suggestion:** read what Copilot proposes.
3. **Run:** approve only actions you understand.
4. **Refine:** ask for one change at a time.
5. **Sanity-check:** verify the files and evidence.

The facilitator reads each prompt aloud, enters it, and pauses. Attendees enter
the same prompt and do not move ahead until the facilitator reaches the checkpoint.

## Setup checkpoint

### GitHub Codespaces

1. Select **Code > Codespaces > Create codespace on main**.
2. Open **Terminal > New Terminal** and run `copilot`.
3. Trust the folder and complete `/login` if prompted.
4. Open the selected track folder.

### GitHub Copilot app

1. Add `https://github.com/marinfrankovic/copilot-workshop-samples.git` as a project.
2. Start an Interactive session.
3. Ask Copilot to show the selected track's `LAB.md`.

The following sections contain both complete tracks. Use only the track selected
for the delivery.
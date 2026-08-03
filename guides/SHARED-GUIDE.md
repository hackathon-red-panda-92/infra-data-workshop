# GitHub Copilot for Non-Coders

## Shared facilitator and attendee guide - 10-minute intro + 50-minute hands-on

The workshop has two separate role-based labs:

- **Systems Administrator:** audit local server inventory and service exports,
  prioritise remediation, validate the findings, and package a local handoff.
- **Data Engineer:** clean local sales exports, answer business questions,
  validate the numbers, and package a local handoff.

During the 50-minute hands-on, the facilitator and attendees complete both labs
in order. Everyone uses the same instructions, enters the same prompts, and
pauses at the same checkpoints. Each lab has a strict 25-minute maximum.

No Azure subscription, cloud deployment, remote connection, upload, cost, or
teardown is required for either track.

## Before the session

- Confirm everyone has a GitHub account with Copilot access.
- Use GitHub Codespaces, or the GitHub Copilot app with Git and Python 3.
- Open <https://github.com/marinfrankovic/copilot-workshop-samples>.
- Open `labs/systems-engineer/LAB.md` and `labs/data-engineer/LAB.md`.
- The facilitator opens both labs in the same clean workspace.
- Use only the fictitious source data included in each lab.

## Run of show

| Time | Shared activity |
|---|---|
| 0-10 | Facilitator gives the existing short introduction. Attendees open the repository and both labs. |
| 10-35 | Everyone completes the Systems Administrator lab. Stop at its final checkpoint. |
| 35-60 | Everyone completes the Data Engineer lab. Stop at its final checkpoint. |

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
4. Open `labs/systems-engineer` first; open `labs/data-engineer` at minute 35 of the session.

### GitHub Copilot app

1. Add `https://github.com/marinfrankovic/copilot-workshop-samples.git` as a project.
2. Start an Interactive session.
3. Ask Copilot to show the Systems Administrator `LAB.md` first.

The following sections contain both complete labs. Complete Sysadmin first and
Data second. Stop each lab after 25 minutes even if optional refinement remains.
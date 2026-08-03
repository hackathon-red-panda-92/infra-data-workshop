# Setup - start here

You do not need coding experience or Azure access. The facilitator selects the
Systems Administrator or Data Engineer track, and attendees follow it together.

## What you need

- A GitHub account with Copilot access.
- Either GitHub Codespaces or the GitHub Copilot app for Windows.
- For the app path: Git and Python 3.

## Option A - GitHub Codespaces

1. Open <https://github.com/marinfrankovic/copilot-workshop-samples>.
2. Sign in with the GitHub account that has Copilot access.
3. Select **Code > Codespaces > Create codespace on main**.
4. Open **Terminal > New Terminal** and run `copilot`.
5. Trust the folder and complete `/login` if prompted.
6. Open the track selected by the facilitator and wait before starting:
   [`labs/systems-engineer/LAB.md`](labs/systems-engineer/LAB.md) or
   [`labs/data-engineer/LAB.md`](labs/data-engineer/LAB.md).

See [`CODESPACES.md`](CODESPACES.md) for troubleshooting.

## Option B - GitHub Copilot app for Windows

1. Install the [GitHub Copilot app](https://gh.io/copilot-app-win64),
   [Git](https://git-scm.com/downloads), and
   [Python 3](https://www.python.org/downloads/). On Windows, select **Add Python
   to PATH** during installation.
2. Open the Copilot app and sign in with the GitHub account that has Copilot access.
3. Add this project from the repository URL:

   ```text
   https://github.com/marinfrankovic/copilot-workshop-samples.git
   ```

4. Start an **Interactive** session for the project.
5. Ask Copilot to show the selected track's `LAB.md`, then wait for the facilitator.

## During the lab

A quoted block in the lab is a prompt. Enter it in the Copilot terminal or app,
read the proposed actions, and approve only what you understand. If an action
fails, enter: **Explain the error in plain English and make only the smallest
necessary fix.**

All source and output files stay local. There is no cloud sign-in, deployment,
upload, cost, or teardown.
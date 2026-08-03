# Run the workshop in GitHub Codespaces

The Codespace includes Git, GitHub CLI, Node.js, Python, and GitHub Copilot CLI.
No Azure tools or cloud sign-in are required.

## Start your Codespace

1. Open this repository on GitHub.
2. Select **Code**, open the **Codespaces** tab, and select **Create codespace on main**.
3. Wait for setup to finish, then open **Terminal > New Terminal**.
4. Confirm the tools are ready:

   ```bash
   copilot --version
   python --version
   ```

If an older Codespace does not match these instructions, run **Codespaces:
Rebuild Container** from the Command Palette.

## Start Copilot

From the repository root, run:

```bash
copilot
```

Trust the workshop folder when asked. If prompted, enter `/login` and complete
GitHub sign-in. Copilot asks before it writes files or runs commands. Read each
proposal and approve only appropriate actions.

Open the track selected by the facilitator:

- [`labs/systems-engineer/LAB.md`](labs/systems-engineer/LAB.md)
- [`labs/data-engineer/LAB.md`](labs/data-engineer/LAB.md)

Wait for the facilitator, then enter each quoted prompt together. All outputs
remain in the Codespace.
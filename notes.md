# Notes

## Review Before Push

- Review `CONTRIBUTING.md` before any Git push request.
- Review the skill source in `/Users/PWSTEPHE/codex/DTC-Skill`.
- Confirm the Nexus DTC Execute workflow reflects the AM/NS Calvert engagement update pattern.
- Adjust wording or procedure details before publishing to GitHub.
- When ready, provide the GitHub remote URL.

## Push Plan

1. Verify the current branch with `git status --short --branch`.
2. Use a `scenario/<short-name>` branch for behavior changes from real DTC workflows.
3. Record successful learnings in `scenarios/validated-scenarios.md`.
4. Commit reviewed edits with a specific message.
5. Push the intended branch to the remote.
6. Confirm the GitHub repository URL or pull request path.

## Installed Skill Copy

The live Codex skill copy is currently installed at:

```text
/Users/PWSTEPHE/.codex/skills/nexus-dtc-execute
```

After review edits, refresh the installed copy from the repository source:

```bash
cp -R /Users/PWSTEPHE/codex/DTC-Skill/skills/nexus-dtc-execute /Users/PWSTEPHE/.codex/skills/nexus-dtc-execute
```

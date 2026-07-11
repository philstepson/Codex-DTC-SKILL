# Collaboration Protocol

Use this protocol when refining the Nexus DTC Execute skill with real engagement scenarios.

## Before Any Git Push

Anyone who asks Codex to push this repository should first review this protocol.

1. Check the current branch and working tree.

   ```bash
   git status --short --branch
   ```

2. Use a scenario branch for skill refinements.

   ```bash
   git checkout -b scenario/<short-name>
   ```

3. Keep `main` as the reviewed source of truth.
4. Commit only changes that were reviewed or validated in a real workflow.
5. Record successful scenario learnings in `scenarios/validated-scenarios.md`.
6. Open or review a pull request before merging scenario work into `main` when another collaborator is involved.
7. Push only after confirming the intended branch and remote.

## Branch Naming

Use short, descriptive branch names:

```text
scenario/update-sales-stage-language
scenario/add-renewal-engagement-path
scenario/refine-ea-sales-boundaries
docs/refresh-install-notes
```

Use `scenario/` when a change came from exercising the skill against a Nexus DTC Execute workflow. Use `docs/` for documentation-only changes.

## Commit Standards

Commit messages should say what behavior changed or what scenario was validated:

```text
Refine DTC update flow for renewal scenarios
Document AM/NS Calvert validation notes
Clarify EA and sales ownership boundaries
```

Avoid vague messages like `updates` or `fixes`.

## Validation Checklist

Before committing a skill behavior change, confirm:

- The skill still stops at MFA, biometric, or human approval boundaries.
- Invocation confirms the in-app browser-control capability, at least one controllable browser tab in the current Codex environment, an authenticated DTC-Nexus home page, and one allowed engagement search hint before searching.
- Invocation activates and verifies the `tools-311` Python environment and required libraries before browser work.
- The workflow preserves EA versus sales role boundaries.
- Missing opportunities are escalated to the owning Sales/CPR with the DTC link and complete initiation instructions; the EA never fabricates a replacement opportunity.
- The EA lifecycle remains explicit: create or select the technical engagement after Sales initiation, then maintain it until the opportunity closes or the effort ends.
- The update language does not make unsupported claims.
- Missing or unclear Nexus data is stated plainly.
- Only the intended engagement fields are updated.
- The installed local skill copy can be refreshed from the repository source.

## Installed Skill Copy

Treat this repository as canonical. The live local Codex skill copy should be refreshed from the repo after reviewed changes are merged:

```bash
cp -R /Users/PWSTEPHE/codex/DTC-Skill/skills/nexus-dtc-execute /Users/PWSTEPHE/.codex/skills/nexus-dtc-execute
```

Avoid making long-lived edits directly in the installed skill copy. If a direct experiment works, copy the change back into this repository, validate it, and commit it here.

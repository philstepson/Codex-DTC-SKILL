# DTC Skill

Reusable Codex skill repository for Oracle Nexus DTC Execute engagement updates.

Repository location:

```text
/Users/PWSTEPHE/codex/DTC-Skill
```

## Contents

- `skills/nexus-dtc-execute/` - Codex skill for authenticated Nexus DTC Execute browser workflows.
- `CONTRIBUTING.md` - branch, validation, and push protocol for collaborators.
- `scenarios/validated-scenarios.md` - record of successful skill exercises and scenario learnings.

## Install Or Refresh Live Skill

Copy the skill folder into the live Codex skills directory:

```bash
cp -R skills/nexus-dtc-execute ~/.codex/skills/nexus-dtc-execute
```

Future Codex sessions should then discover the skill as `nexus-dtc-execute`.

## Typical Use

Ask Codex to use the Nexus DTC Execute skill while the authenticated Oracle APEX page is open:

```text
Use the Nexus DTC Execute skill to update this engagement from the in-app browser.
```

The skill covers browser navigation, EA versus sales boundaries, opportunity linking, progress milestones, status wording, and verification after writes.

## Collaboration

Before asking Codex to push changes, review `CONTRIBUTING.md`.

Use scenario branches for skill refinements, record successful workflow learnings in `scenarios/validated-scenarios.md`, and keep `main` as the reviewed source of truth.

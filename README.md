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

Ask Codex to use the Nexus DTC Execute skill while the authenticated DTC-Nexus home page is open:

```text
Use the Nexus DTC Execute skill to update this engagement from the in-app browser.
```

On invocation, the skill first confirms both that browser control is available and that this specific Codex invocation exposes a controllable browser tab. An installed plugin alone is not enough—CLI sessions can have zero browser targets. Only after the tab is authenticated and open on the DTC-Nexus home page does the skill ask for one engagement search hint: an Engagement ID, Opportunity ID, SR number, or Account / customer name.

The skill covers Python dependency preflight, authenticated in-app or explicitly approved Chrome handoff, browser navigation, EA versus Sales/CPR ownership boundaries, opportunity linking, guided missing-DTC-opportunity creation, progress milestones, status wording, and verification after writes.

When a verified Oracle Sales opportunity is missing from DTC, the skill offers a choice to create its DTC record or draft an email to the Sales owner. It permits creation only when the source opportunity's revenue amount is greater than zero, preserves Sales-owned values, verifies the new DTC record is discoverable, and then guides creation or selection of the EA engagement.

## Collaboration

Before asking Codex to push changes, review `CONTRIBUTING.md`.

Use scenario branches for skill refinements, record successful workflow learnings in `scenarios/validated-scenarios.md`, and keep `main` as the reviewed source of truth.

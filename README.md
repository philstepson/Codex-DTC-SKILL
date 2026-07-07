# DTC Skill

Reusable Codex skill repository for Oracle Nexus DTC Execute engagement updates.

Repository location:

```text
/Users/PWSTEPHE/codex/DTC-Skill
```

## Contents

- `skills/nexus-dtc-execute/` - Codex skill for authenticated Nexus DTC Execute browser workflows.

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

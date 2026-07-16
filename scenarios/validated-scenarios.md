# Validated Scenarios

Record successful skill exercises here so future changes preserve proven behavior.

## Entry Template

```markdown
## YYYY-MM-DD - Short scenario name

Validated by:
Scenario:
Changed files:
- skills/nexus-dtc-execute/SKILL.md

What worked:
- 

Follow-up:
- 
```

## 2026-07-07 - Initial Nexus DTC Execute Skill Publication

Validated by: Phil
Scenario: Publish the first reusable Nexus DTC Execute skill repository for engagement update workflows.
Changed files:
- README.md
- notes.md
- skills/nexus-dtc-execute/SKILL.md
- skills/nexus-dtc-execute/references/navigation.md
- skills/nexus-dtc-execute/references/role-boundaries.md
- skills/nexus-dtc-execute/references/status-language.md
- skills/nexus-dtc-execute/references/update-playbook.md

What worked:
- The repository now has a GitHub remote and a tracked `main` branch.
- The live skill install location is documented.
- The skill materials separate navigation, role boundaries, status wording, and update procedure.

Follow-up:
- Use scenario branches for future engagement-specific refinements.
- Add entries here when a colleague validates new scenarios.

## 2026-07-10 - Invocation browser-target preflight

Validated by: Phil
Scenario: Invoke the Nexus DTC Execute skill from a Codex CLI session where the browser-control plugin is installed but no controllable browser tab is exposed.
Changed files:
- README.md
- CONTRIBUTING.md
- skills/nexus-dtc-execute/SKILL.md

What worked:
- The preflight distinguishes installed browser-control capability from an actual controllable browser target.
- With zero browser targets, the skill stops before requesting a Nexus URL, search hint, or authentication action and reports the environment requirement plainly.

Follow-up:
- Re-test the same preflight from a browser-enabled Codex environment before performing live Nexus updates.

## 2026-07-10 - Missing opportunity Sales escalation

Validated by: Phil
Scenario: Look up opportunity A9F6LF for KUBOTA USA INC, confirm it is absent from DTC, identify its Oracle Sales owner, and send the approved initiation instructions.
Changed files:
- README.md
- CONTRIBUTING.md
- skills/nexus-dtc-execute/SKILL.md
- skills/nexus-dtc-execute/agents/openai.yaml
- skills/nexus-dtc-execute/references/navigation.md
- skills/nexus-dtc-execute/references/role-boundaries.md
- skills/nexus-dtc-execute/references/update-playbook.md

What worked:
- The workflow verified the opportunity in Oracle Sales and identified the owning Sales representative/CPR.
- The exact DTC lookup confirmed the opportunity was not visible without substituting another opportunity.
- The approved email included the DTC home URL, opportunity and engagement identifiers, account/territory checks, synchronization guidance, and a request to notify the EA.
- The workflow preserved the boundary that Sales initiates a missing opportunity and the EA maintains the technical engagement through closure or effort end.

Follow-up:
- Resume engagement 1279516 after Sales confirms A9F6LF is visible and linked in DTC.

## 2026-07-16 - KUBOTA DB@Azure technical engagement and status update

Validated by: Phil
Scenario: Locate DTC opportunity A9G9Z5 for KUBOTA USA INC, create a DP Multicloud Base engagement, and record an approved technical status update.
Changed files:
- scenarios/validated-scenarios.md
- skills/nexus-dtc-execute/references/update-playbook.md

What worked:
- A9G9Z5 was visible in the DTC opportunity picker. A temporary `No data found` result was caused by the Opportunity Review report filters, not by a missing DTC opportunity.
- The workflow created engagement `1289117`, **KUBOTA USA INC – DB@Azure Technical Engagement**, as `DP Multicloud Base` and linked it to A9G9Z5.
- The creation form required a non-empty engagement description. Source was set to `Sales Driven Initiative` and segment to `Multicloud Driven`.
- The approved technical update recorded the AI-based Lending and Leasing Dashboard demo simulation and its follow-on agentic predictive capability for potential bad loans and poor-collections factors, while leaving customer validation and production deployment open.
- Applying the status update changed the engagement heat to Yellow. This was the app's automatic new-engagement status, not evidence of an open technical blocker.

Follow-up:
- Review the dashboard and predictive approach with the customer, validate priority use cases, data and integration needs, and success criteria before marking technical validation or onboarding milestones complete.

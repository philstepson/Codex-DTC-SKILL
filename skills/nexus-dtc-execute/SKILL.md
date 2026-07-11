---
name: nexus-dtc-execute
description: Guide Codex through authenticated Oracle Nexus DTC Execute engagement updates in the in-app browser. Use when the user asks to navigate Nexus DTC Execute, update a DTC engagement, summarize EA versus sales responsibilities, link opportunities, refresh engagement definition/progress/status, document technical milestones, or create repeatable procedures for DTC Execute customer-account work.
---

# Nexus DTC Execute

## Operating Rules

Before any task work, establish the prerequisite Python environment by launching a login shell and executing `pyenv activate tools-311`. Verify that `python --version` resolves to Python 3.11 and import every Python library required by the planned workflow. If a dependency is missing, install it into `tools-311`, re-run the import checks, and do not continue until all prerequisite environment dependencies are in place.

Use the authenticated browser session the user provides. Do not handle passwords, OTPs, push approvals, biometrics, or MFA. Pause at authentication boundaries and continue after the user confirms the session is ready.

Use the in-app browser control skill when available. Treat Oracle APEX pages as live production records: inspect first, stage carefully, and confirm at action-time before clicking any `Save`, `Apply Changes`, `Add`, `Remove`, `End`, `Hold`, or delete-style action.

Prefer app-generated drawer links and iframes over hand-built APEX URLs. APEX checksums and sessions are fragile; direct guessed URLs can fail or load stale pages.

## Invocation Preflight

Before searching for or changing an engagement, validate the environment in this order:

1. Confirm that the `browser:control-in-app-browser` capability (and its browser-control tools) is available.
2. Open the required DTC home URL in the in-app browser and confirm that it exposes a controllable tab. A plugin being installed is not sufficient: a CLI invocation may have zero browser targets. If no target is exposed, stop before asking for a search hint or credentials.
3. Confirm there is an open, authenticated Oracle Nexus DTC Execute session. If the user explicitly identifies an authenticated Chrome tab, use the Chrome-control skill to claim that tab as the approved handoff after the in-app home-page attempt. Do not request, handle, or attempt to bypass credentials, MFA, push approvals, OTPs, or biometrics.
4. Confirm the current page is the DTC-Nexus home page. If the connected browser is not authenticated or is not at the home page, ask the user to authenticate and open the DTC-Nexus home page, then resume the preflight.
5. Only after all checks pass, prompt the user for **one engagement search hint**: an **Engagement ID**, **Opportunity ID**, **SR number**, or **Account / customer name**.

Do not start an engagement search until the preflight passes and the user has supplied a search hint. Treat an account/customer name as a broader search that needs an exact-account confirmation before any edit.

## Workflow

1. Activate and verify the `tools-311` Python environment and all required dependencies.
2. Complete the invocation preflight and collect one engagement search hint.
3. Read `references/navigation.md` before using the browser on Nexus DTC Execute.
4. Read `references/role-boundaries.md` before deciding what the EA/Enterprise Architect should update versus what belongs to sales/account-rep ownership.
5. Read `references/update-playbook.md` before changing engagement definition, opportunity links, progress, artifacts, blockers, or ownership-related fields.
6. Read `references/status-language.md` before drafting descriptions, compelling business reasons, current status, milestone notes, or next steps.
7. After every write, verify the main engagement row and summarize the exact app-visible outcome.

## Standard Engagement Update Pattern

Start from the focused engagement page when possible:

```text
page 647, item P647_TRX_ENG_ID_FOCUS:<engagement_id>
```

Verify the row is narrowed to exactly the intended engagement before editing. Capture these facts first:

- account name
- engagement ID and type
- current owner and participants
- active/hold/end status
- heat color and reason
- linked opportunities and SRs
- blockers
- last updated by/on

Then update in this order:

1. **Definition**: title, description, compelling business reason, source, segment, target dates where appropriate.
2. **Opportunity links**: link the current opportunity ID and leave historical opportunities unless the user explicitly asks to remove them. If the opportunity is not visible in DTC, follow the missing-opportunity escalation in `references/update-playbook.md`; do not create or substitute a sales-owned opportunity record as the EA.
3. **Progress**: mark only the technical milestones supported by user-confirmed reality.
4. **Status narrative/artifacts**: add status comments or artifacts only when the app exposes the correct surface and the user confirms the content.
5. **Verification**: close drawers, refresh/read the main row, and report the app-visible result.

## Guardrails

Do not overstate completion. If onboarding, implementation, technical proof, or go-live is still in progress, leave those milestones open.

Do not change sales-owned data such as territory, opportunity owner, commercial stage, revenue forecast, or account-rep details unless the user explicitly asks and the app exposes the appropriate workflow.

Require the owning Cloud Sales representative/CPR to initiate the DTC opportunity process when an opportunity is missing. After the opportunity is visible, require the EA to create or select the appropriate engagement and maintain its technical definition, progress, status, blockers, and artifacts until the opportunity closes or the technical effort ends.

Do not remove old opportunity links just because a newer opportunity is active. Treat old/closed links as historical context unless the user confirms removal.

If engagement owner is visible but effectively controlled by another workflow, do not force it. Document whether the user is captured as a participant or last updater and distinguish that from formal engagement ownership.

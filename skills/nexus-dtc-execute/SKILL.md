---
name: nexus-dtc-execute
description: Guide Codex through authenticated Oracle Nexus DTC Execute engagement updates in the in-app browser. Use when the user asks to navigate Nexus DTC Execute, update a DTC engagement, summarize EA versus sales responsibilities, link opportunities, refresh engagement definition/progress/status, document technical milestones, or create repeatable procedures for DTC Execute customer-account work.
---

# Nexus DTC Execute

## Operating Rules

Use the authenticated browser session the user provides. Do not handle passwords, OTPs, push approvals, biometrics, or MFA. Pause at authentication boundaries and continue after the user confirms the session is ready.

Use the in-app browser control skill when available. Treat Oracle APEX pages as live production records: inspect first, stage carefully, and confirm at action-time before clicking any `Save`, `Apply Changes`, `Add`, `Remove`, `End`, `Hold`, or delete-style action.

Prefer app-generated drawer links and iframes over hand-built APEX URLs. APEX checksums and sessions are fragile; direct guessed URLs can fail or load stale pages.

## Workflow

1. Read `references/navigation.md` before using the browser on Nexus DTC Execute.
2. Read `references/role-boundaries.md` before deciding what the EA/Enterprise Architect should update versus what belongs to sales/account-rep ownership.
3. Read `references/update-playbook.md` before changing engagement definition, opportunity links, progress, artifacts, blockers, or ownership-related fields.
4. Read `references/status-language.md` before drafting descriptions, compelling business reasons, current status, milestone notes, or next steps.
5. After every write, verify the main engagement row and summarize the exact app-visible outcome.

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
2. **Opportunity links**: link the current opportunity ID and leave historical opportunities unless the user explicitly asks to remove them.
3. **Progress**: mark only the technical milestones supported by user-confirmed reality.
4. **Status narrative/artifacts**: add status comments or artifacts only when the app exposes the correct surface and the user confirms the content.
5. **Verification**: close drawers, refresh/read the main row, and report the app-visible result.

## Guardrails

Do not overstate completion. If onboarding, implementation, technical proof, or go-live is still in progress, leave those milestones open.

Do not change sales-owned data such as territory, opportunity owner, commercial stage, revenue forecast, or account-rep details unless the user explicitly asks and the app exposes the appropriate workflow.

Do not remove old opportunity links just because a newer opportunity is active. Treat old/closed links as historical context unless the user confirms removal.

If engagement owner is visible but effectively controlled by another workflow, do not force it. Document whether the user is captured as a participant or last updater and distinguish that from formal engagement ownership.

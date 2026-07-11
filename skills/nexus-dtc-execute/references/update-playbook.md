# Update Playbook

## Engagement Definition

Open the `Edit Engagement` drawer from page 647. In page 187, inspect these common fields:

- `P187_ORCL_ENGAGEMENT_NAME`: internal engagement title
- `P187_ENG_OWNER`: engagement owner, often a popup LOV/display field
- `P187_ENG_DESC`: engagement description
- `P187_ENG_COMP_BUS_REASON`: compelling business reason
- `P187_ENG_SOURCE`: source
- `P187_ENG_SEGMENT`: segment
- `P187_START_DATE_input`, `P187_END_DATE_input`
- `P187_TARGET_START_DATE_input`, `P187_TARGET_END_DATE_input`

Recommended source/segment choices depend on the facts:

- Use `Sales Driven Initiative` when the opportunity/customer purchase path is sales led.
- Use `Enterprise Arch Initiated` only when the EA initiated the engagement.
- Use `Multicloud Driven` for Azure/Google/AWS-connected Oracle architecture.
- Use `Data Platform (Non AI) Driven`, `DB Driven`, `Hardware Driven`, or other segments only when they better match the primary customer driver.

Stage fields first. Ask before clicking `Save`.

## Opportunity Links

Open the `Select Account Opportunity or Revenue Lines` drawer from the linked opportunities cell.

Filter by opportunity ID in `P44_OPP_ID_SRCH`, then click `Apply Filter`.

In the results:

- `New Opp Link` links the whole opportunity.
- `New Rev Link` links a specific revenue line.
- Opportunity-only actions usually set `P44_OPP_ID_OF_FOCUS` and leave `P44_REV_ID_OF_FOCUS` blank.
- Revenue-line actions set both opportunity and revenue line focus.

After selecting an opportunity, the drawer may show:

```text
The Opportunity "<opp_id>" is not linked to the engagement, do you want to Add it?
```

Confirm with the user before clicking `Add Opportunity "<opp_id>" Link`. After adding, verify the drawer flips to already linked and the main row lists the new opportunity.

Do not remove old closed opportunities unless the user explicitly asks. Historical links can remain for continuity.

### Missing Opportunity Escalation

When an exact opportunity ID is not visible in DTC:

1. Verify the opportunity directly in Oracle Sales and capture its account, title, status/stage, owning Cloud Sales representative/CPR, and owner email.
2. Recheck the DTC opportunity-link drawer using the exact opportunity ID, the correct focused account, `Limit to Open / Won / Pending: Yes`, `Limit to Valid Opps: Yes`, and the appropriate registry/global-ultimate scope.
3. If it is still absent, stop the link attempt. Do not create a replacement opportunity or attach a different opportunity.
4. Draft an email to the owning Sales representative/CPR using this pattern:

```text
Subject: Action needed: Add opportunity <opp_id> to Nexus DTC Execute

Hi <sales_owner>,

Opportunity <opp_id> ("<opportunity_title>") is not currently visible in Nexus DTC Execute for <account>, so it cannot be linked to the intended engagement.

Nexus DTC Execute:
<home_page_url_from_navigation.md>

Account: <account>
Opportunity ID: <opp_id>
DTC engagement ID: <engagement_id_if_known>
Engagement type: <engagement_type_if_known>
Engagement owner: <engagement_owner_if_known>

Please open Opportunity Review, search for the exact opportunity ID, confirm the Oracle Sales account/registry and Data Platform territory assignments, allow the integration to synchronize if corrections are needed, and pre-connect or link the opportunity. Please notify the EA when it is visible and linked.
```

5. Obtain action-time confirmation before sending the email.
6. Leave the DTC workflow staged without fabricating a successful link. Resume after Sales/CPR confirms the opportunity is visible.
7. Once visible, have the EA create or select the appropriate engagement, link the opportunity, and maintain the technical engagement until the opportunity closes or the effort ends.
8. Prefer updating and sending the reviewed Outlook draft. If the connector cannot update or delete a superseded draft, send the approved corrected message and explicitly identify the stale draft for manual deletion.

## Progress And Milestones

Open `Engagement Progress` from page 647. Page 352 uses checkbox milestones grouped by phase.

Common DP A2I Base milestone examples:

- `F40_1`: Key Influencers & Stakeholders
- `F40_2`: Identify & Document Blockers and Gaps
- `F40_3`: Rapid Discovery, Identify Business Drivers and Pain Points
- `F40_4`: Map Current State Architecture
- `F40_5`: Identify current and potential competitors
- `F40_6`: Map Pain Points to Solutions
- `F40_21`: Develop Future State Architecture
- `F40_23`: Develop Initial Migration/Adoption Strategy
- `F40_26`: Create Sizing / initial BOM
- `F40_29`: Technical Validation of Future State
- `F40_31`: Finalize BOM
- `F40_34`: On Boarding
- `F40_37`: Obtain Customer Acknowledgement / Final Readout

Mark only what the user confirms is complete. Examples:

- If discovery/current/future state and sizing are complete, mark discovery, current state, future state architecture/adoption, and sizing milestones.
- If installation/configuration is still in progress, do not mark onboarding complete.
- If technical validation or POC is not complete, leave technical proof open.

Ask before clicking `Apply Changes`. After applying, verify `# Hit`, `% Hit`, engineering insight, heat, reason, and last updated fields.

## Milestone Log

`Edit Milestone Log` opens page 69. This is primarily an audit/grid surface. It may allow logged date/comment edits, but it is not the primary place for broad current status. Prefer the progress checklist for milestone truth and artifacts/status comments for narrative details.

## Artifacts And Blockers

Open the artifacts drawer when the user has concrete documents, links, or evidence to attach. Do not upload files without explicit confirmation.

Use blockers only for real open impediments. If there are no active blockers, leave blockers at `0 Open` and do not invent a blocker just to explain pending onboarding.

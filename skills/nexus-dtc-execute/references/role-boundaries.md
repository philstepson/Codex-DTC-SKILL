# EA Versus Sales Responsibilities

## Enterprise Architect / Technical Owner Updates

The EA or technical owner should maintain technical truth and customer architecture progress:

- engagement description for technical solution scope
- compelling business reason tied to architecture and customer outcomes
- technical milestones and checkpoints
- current state architecture
- future state architecture
- sizing, capacity, initial BOM, and technical assumptions
- implementation/onboarding status when actually in progress or complete
- blockers/gaps that affect architecture, delivery, onboarding, networking, security, data movement, or platform readiness
- artifacts such as sizing documents, architecture diagrams, workshops, assessment outputs, and technical notes

Use technical progress fields to show completed work. Use status/comment/artifact surfaces for narrative support when available.

## Sales / Account Representative Updates

Sales-owned information should normally stay with the opportunity or sales system:

- opportunity owner
- account representative
- territory and sales hierarchy
- revenue line ownership
- sales stage and forecast
- opportunity amount/bookings
- commercial agreement status unless a DTC field explicitly asks for a technical-commercial milestone
- old opportunity cleanup unless the user explicitly confirms removal

When an opportunity is not visible in DTC, the user may create a DTC record derived from the verified Oracle Sales opportunity when its revenue amount is greater than zero. The DTC record must preserve the source opportunity and sales-owned values; it must not imitate, replace, or alter the sales opportunity. If the source opportunity has no positive revenue amount, or the app does not expose a DTC creation action, offer the owning Cloud Sales representative/CPR email path instead.

If a user tells you the account rep or opportunity owner, verify it in the opportunity drawer if possible, but do not overwrite unrelated sales fields from the engagement form.

## Ownership Nuance

Distinguish these concepts:

- **Engagement owner**: a formal owner field on the DTC engagement. It may be controlled by a popup LOV, transfer workflow, program administration, or original creator.
- **Participant**: people who appear because they own activity/checkpoint/milestone work.
- **Opportunity owner/account rep**: comes from linked opportunity/revenue lines and may differ from engagement owner.
- **Last updated by**: audit signal only; it does not necessarily mean formal ownership.

If the engagement owner remains the prior person but the active opportunity and milestone work show the current user, explain that difference plainly.

After a DTC opportunity record is created or becomes visible, the EA owns the technical engagement lifecycle: create or select the appropriate engagement, maintain the definition and technical progress, record blockers and artifacts, and keep it current until the linked opportunity closes or the technical effort is explicitly ended.

# Status Language

## Principles

Write in current, factual language. Separate technical truth from sales ownership. Do not imply installation, onboarding, technical proof, production agreement, or go-live is complete unless the user says it is.

Use exact dates for "today" when writing into the app. Prefer the system current date over relative language.

## Engagement Description Pattern

Use the description for technical scope and approach, not a running status log.

```text
<Customer> is pursuing <technical/business modernization scope>. The customer has <completed inputs/purchases/sizing> for <product/workload>. Oracle is working with <team/specialists> to <remaining implementation/configuration work>.

In parallel, the customer has <additional platform decision/purchase> to complete the broader solution. <Product/workstream A> and <product/workstream B> both contribute to the customer modernization path and should be tracked together as part of the overall architecture.
```

## Compelling Business Reason Pattern

Use the compelling business reason for why the customer needs the solution.

```text
<Customer> needs to <modernize/replace/reduce risk/enable architecture>. <Product A> enables <capability>, while <Product B> provides <target platform/capacity>. The combined solution supports <business/technical outcomes> while reducing <risk/cost/complexity> and moving the customer toward <future-state architecture>.
```

## Current Status Pattern

Use status/comment fields, when present, for a running update:

```text
As of <date>, this engagement remains active. <Customer> has completed discovery, current-state review, future-state architecture, and sizing/capacity work. The current opportunity is <opp_id>, and <sales/account rep> is reflected on the opportunity.

Current technical work remains focused on <installation/configuration/onboarding/validation>. Next step: <specific technical action> with <team/person>, while keeping <not-yet-complete milestone> open until validated.
```

## Example For GoldenGate@Azure And Exadata Cloud@Customer

```text
AM/NS Calvert is pursuing a combined data movement and Exadata modernization solution. The customer has provided sizing for GoldenGate and has purchased GoldenGate@Azure. Oracle is working with product specialists to install and configure GoldenGate@Azure for the required replication and data movement use case.

In parallel, the customer has decided to purchase three 1/4 Base Rack Exadata X11M Cloud@Customer systems to complete the broader solution. GoldenGate@Azure and Exadata Cloud@Customer both contribute to the revenue stream and should be tracked together as part of the customer's overall modernization path.
```

## Completion Boundaries

Use these boundaries when mapping facts to milestones:

- Discovery complete: stakeholders/business drivers/pain points/gaps are understood.
- Current state complete: current architecture and competitors are documented.
- Future state complete: target architecture and adoption path are documented.
- Capacity sizing complete: sizing or initial BOM exists.
- Technical proof complete: validation/POC/success criteria are complete.
- Onboarding complete: service install/configuration/access/initial enablement are complete.
- Technical win complete: customer has acknowledged final architecture/readout or production path.
- Post-live complete: go-live and day-one support activities are done.

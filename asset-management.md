# Asset Management

Tracking and managing the things the organization owns or uses that have financial, contractual, or compliance significance. Organizations use asset records so that they know what they have, where it is, who is responsible, and when it needs renewal or replacement.

## Primary Objects/Actors

- **Asset** — A single item that the organization tracks for financial, contractual, or compliance reasons: a piece of hardware (laptop, server, network device), a software license or subscription, or a contract. Each asset is one record with an identifier, type, owner or custodian, and key dates (purchase, warranty, renewal).
- **Asset owner / Custodian** — The person or team responsible for the asset (e.g., who uses the laptop, who is accountable for the license). Ownership supports lifecycle decisions (refresh, renew, retire) and cost allocation.

## Supporting Objects/Actors

- **Lifecycle stage** — The current phase of the asset: in use, in storage, under repair, retired. Used for reporting (how many devices in use) and planning (what is due for refresh).
- **Cost / Financial record** — Purchase price, subscription cost, or allocation. Many organizations track this in the asset record or link to finance; it supports budgeting and chargeback.

## Related Objects/Actors

- **Configuration item** — The live instance of a piece of software or hardware in the environment may be linked to the asset record (e.g., "this server is Asset #123"). The boundary between asset (what we own) and configuration (what we run) is defined locally.
- **Contract / Vendor** — Software and some hardware assets are tied to contracts and vendors for renewal and support. The asset record may reference the contract or procurement system.
- **Incident / Change** — Incidents and changes may reference the asset (e.g., "laptop damaged," "license upgraded") for history and impact.

## Lifecycles

Assets typically follow a lifecycle from acquisition to disposal:

1. **Requested / Ordered** — Approved for purchase; not yet received (optional).
2. **Received / In use** — In the organization’s possession and in use (or available for use). This is the normal state for active assets.
3. **In storage / Under repair** — Temporarily not in normal use (optional).
4. **Retired / Disposed** — No longer in use; disposed, sold, or returned. The record may be kept for history and audit.

Organizations keep the lifecycle simple so that reporting (e.g., "how many laptops in use") and planning (e.g., "what is due for refresh") stay clear.

## Getting Started

- **Minimal template:** A single list or system (spreadsheet or tool) where every significant asset is recorded with: unique ID, type (e.g., laptop, server, software license), owner or custodian, and key dates (purchase, warranty end, renewal). Add cost or contract reference when you need budgeting or renewal visibility.
- **When to introduce:** Introduce when the organization cannot answer "how many devices do we have?" or "when do our key licenses expire?"; when surprise renewals or audit findings occur; or when cost allocation or chargeback is required. Pain signals include "we didn’t know that contract was up," duplicate purchases, and inability to account for equipment.

## Processes

- **Recording assets:** When an asset is acquired (purchase, lease, subscription), it is added to the asset register with identifier, type, owner, and key dates. Some organizations do this at procurement; others at first use or deployment.
- **Lifecycle updates:** As assets move (e.g., reassigned, repaired, retired), the record is updated so that reports and plans reflect reality. Many organizations tie updates to onboarding/offboarding or procurement workflows.
- **Renewal and refresh:** Using key dates (renewal, warranty end, refresh cycle), the organization plans renewals and replacements. Owners or a central function review the list periodically and trigger procurement or retirement.
- **Audit and compliance:** Asset records support audits (what do we have, where is it) and compliance (licenses, contracts). The level of detail and formality depends on regulatory and contractual requirements.

## Adaptation

- **What counts as an asset:** Organizations define a threshold (e.g., value above $X, or all software licenses, or all devices). Start with what has financial or compliance impact—hardware above a cost, all subscriptions, key contracts—and expand when new needs appear.
- **Ownership vs. central tracking:** In some organizations a central team maintains the register; in others each department or cost center owns its assets and updates the record. Choose a model that matches how procurement and finance already work.
- **Pitfalls:** Building a detailed asset register that no one maintains; requiring too much data so that people never add assets; or treating asset management as separate from procurement and lifecycle so that the list drifts. Tie updates to acquisition and disposal so that the register stays current.

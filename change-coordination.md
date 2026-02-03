# Change Coordination

Managing modifications to the environment in a way that balances speed, risk, and clarity. Organizations coordinate changes so that work is visible, impact is considered, and rollbacks are possible when something goes wrong.

## Primary Objects/Actors

- **Change** — A single planned modification to the environment: a release, patch, config update, or infrastructure change. Each change is one record with a description, what it affects, who is doing it, when it is scheduled, and its outcome (success, failure, rolled back).
- **Change owner / Implementer** — The person or team responsible for designing, executing, and (if needed) rolling back the change. They are the primary actors; coordination ensures others are informed and conflicts are avoided.

## Supporting Objects/Actors

- **Work order / Task list** — The steps to perform the change (and rollback). Often captured as a checklist or runbook so that nothing is skipped and handoffs are clear.
- **Approval** — In many organizations, certain changes require one or more approvers (e.g., technical lead, manager, or business owner) before implementation. The approval is recorded with who approved and when.

## Related Objects/Actors

- **Incident / Problem** — A change may be raised to fix an incident or implement a problem’s permanent fix. Incidents that occur after a change may be linked to that change for correlation.
- **Configuration item** — Changes typically target one or more CIs; the configuration model is used to assess impact and dependencies.
- **Release** — Some organizations group multiple changes into a release (e.g., "Q2 release") for scheduling and communication; the change record may reference the release.

## Lifecycles

Changes move through stages that reflect real workflow:

1. **Draft / Requested** — The change is described and submitted; it may not yet be fully specified or approved.
2. **Scheduled** — Approved and assigned a date/time (and often a window). Resources and stakeholders are aligned.
3. **In progress** — Implementation has started. Status may be updated during the window (e.g., "rolling out," "verifying").
4. **Complete** — Implementation finished. Outcome is recorded: success, partial success, failed, or rolled back. Post-implementation review may follow for significant or failed changes.

Some organizations add "approved," "on hold," or "cancelled" to support governance and rescheduling. Keep only the states that change who does what or how you report.

## Getting Started

- **Minimal template:** A single log or board (tool or shared list) where every change is recorded with: what is changing, what it affects, who is doing it, when it will happen, and the result (done / rolled back / failed). For riskier changes, add a short impact assessment and one or more approvers before the work is done.
- **When to introduce:** Introduce when changes are happening in the dark and collide or cause outages; when there is no shared view of "what’s changing this week"; or when a bad change has no clear rollback and no record of what was done. Pain signals include "someone changed something and broke it," repeated weekend fires after Friday changes, and "we don’t know who changed what."

## Processes

- **Request and describe:** The change owner (or requester) records what will be done, which systems or services are affected, and the planned date/time. In larger organizations this is reviewed for conflicts and impact.
- **Assess and approve:** For higher-risk changes, someone other than the implementer assesses impact (often using configuration data) and approves or rejects. Approval can be formal (sign-off) or lightweight (e.g., comment in a ticket).
- **Schedule and implement:** The change is scheduled in a shared calendar or tool so that overlapping work is avoided. During the window, the implementer follows the plan (and runbook if one exists), updates status, and records the outcome. If the change fails, rollback steps are executed and documented.
- **Review:** After significant or failed changes, teams often hold a short review: what happened, what was learned, what to do differently. Output may feed problem management or process updates.

## Adaptation

- **Risk-based approach:** Many organizations use risk (impact × likelihood) or change type to decide how much process to apply. Low-risk, routine changes (e.g., standard patches) may need only a record and perhaps peer review; high-risk changes get full assessment and approval. Define a few categories and apply process accordingly.
- **Standard changes:** Repeated, well-understood changes (e.g., "add user to group X") are often pre-approved and tracked with minimal review. The key is that they are documented and repeatable so they can be trusted.
- **Pitfalls:** Requiring the same level of approval for every change so that small, safe work is delayed; treating change coordination as only "approval" and not tracking outcome and rollback; or keeping the change log separate from how work is actually done so that people bypass it. Fit the process to how teams already plan and deploy, and make recording the change the path of least resistance.

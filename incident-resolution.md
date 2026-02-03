# Incident Resolution

Restoring normal service as quickly as possible when something goes wrong. Organizations track incidents so that affected users get help, work is not lost, and patterns can be spotted over time.

## Primary Objects/Actors

- **Incident** — A single occurrence of something wrong: a user cannot work, a system is down, or a result is incorrect. Each incident is one record (ticket, case, or log entry) with a description, who reported it, when it was raised, and when it was resolved.
- **Reporter / Affected user** — The person or system that reported the incident or is impacted. Often the same; sometimes a manager or monitoring tool reports on behalf of others.

## Supporting Objects/Actors

- **Work log / Activity** — Notes and actions taken while working the incident: what was tried, what was found, who was involved. Used for handoffs, escalation, and later review.
- **Resolution** — The outcome: what fixed it (or what was done as a workaround), who closed it, and when. Many organizations also record a short category or cause for reporting.

## Related Objects/Actors

- **Problem** — When the same or similar incidents keep happening, organizations often link them to a problem record so root cause can be addressed separately.
- **Change** — If fixing the incident required or will require a change to infrastructure or code, that change may be tracked in change coordination.
- **Configuration item** — The system, service, or component that failed or was involved is often referenced from configuration management.

## Lifecycles

Incidents usually move through a small set of stages that reflect real workflow:

1. **New / Open** — Reported, not yet assigned or in progress.
2. **In progress** — Someone is actively working it (diagnosing, applying a fix, or implementing a workaround).
3. **Pending** — Waiting on the user, another team, or a change before work can continue.
4. **Resolved / Closed** — Normal service restored (or a workaround is in place) and the incident is considered done. Some organizations distinguish "resolved" (user confirmed) from "closed" (auto-closed or closed by support).

Organizations keep the lifecycle simple so that queues, reports, and handoffs stay clear. Extra states are added only when they change who does the work or how it is measured.

## Getting Started

- **Minimal template:** One place to record incidents (ticketing tool, shared list, or channel), with at least: short title, who reported it, when it was raised, who is working it, and when it was resolved. Optionally: category, affected service or system, and a one-line resolution note.
- **When to introduce:** Introduce or formalize when incidents are getting lost, the same issue is fixed repeatedly with no record, or there is no shared view of what is currently broken and who is handling it. Pain signals include "we fixed it but didn’t write it down," duplicate effort, and inability to report how many incidents occurred or how long they lasted.

## Processes

- **Triage:** As incidents arrive, someone assigns them (by skill, team, or round-robin) and may set priority based on impact and urgency. In small teams this is the same person who works the ticket; in larger ones a dedicated role or rotation does triage.
- **Diagnosis and fix:** The assignee reproduces or confirms the issue, checks known errors and recent changes, and applies a fix or workaround. Work is logged so others can continue or learn.
- **Escalation:** When the assignee cannot resolve within time or skill, the incident is escalated to a more senior person or another team, with enough context (work log, environment, steps) for the next person to continue.
- **Closure:** When service is restored, the resolver records what was done and closes the incident. Some organizations require confirmation from the reporter before closing.

## Adaptation

- **Priorities and targets:** Organizations set response and resolution targets (e.g., critical within 15 minutes, normal within 4 hours) based on business impact and capacity. Start with a few priority levels and adjust as you learn what "good enough" looks like.
- **What counts as an incident:** Many teams only track user-facing or business-impacting issues; others include every alert or anomaly. Decide based on what you need to measure and improve; avoid creating so many "incidents" that real ones are buried.
- **Pitfalls:** Treating every incident as one-off without ever looking for patterns; closing incidents without a resolution note; or adding so many required fields and stages that people stop using the system. Keep the bar low enough that recording incidents is the default.

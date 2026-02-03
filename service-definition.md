# Service Definition

Describing what a service is, what it does, who it is for, and how it is delivered so that providers and consumers share a clear understanding. Organizations use service definitions so that expectations are aligned, boundaries are clear, and improvements can be targeted.

## Primary Objects/Actors

- **Service** — A capability that the organization provides to users or other teams: e.g., email, payroll, a customer-facing application, or an internal platform. The service is the thing that is consumed; it is described in a single place (a document, wiki, or catalog entry) so that everyone can refer to the same definition.
- **Service owner** — The person or team accountable for the service: ensuring it is defined, delivered, and improved. The owner is the primary actor for definition and for aligning with consumers.

## Supporting Objects/Actors

- **Service description** — The written definition: name, purpose, scope (what is in and out), intended users, and key capabilities. Often includes how to request or access the service and how to get support.
- **Service level / Expectations** — What "good" looks like: availability, response time, or other metrics that the provider and consumer agree to (formally or informally). Used to set priorities and measure performance.

## Related Objects/Actors

- **Configuration item** — The systems and components that deliver the service are often listed or linked from the service definition so that incidents and changes can be mapped to services.
- **Incident / Problem** — Incidents and problems are often associated with a service so that impact ("email was down") and trends ("payroll has had three incidents this month") can be reported.
- **Experience** — How users experience the service (usability, satisfaction, outcomes) may be tracked in experience management and referenced from the service definition.

## Lifecycles

Services themselves may have a lifecycle (e.g., pilot, live, retired), but the main focus of the discipline is the lifecycle of the *definition*:

1. **Draft** — The service is being described; not yet agreed or published (optional).
2. **Published / Live** — The definition is current and shared with consumers and providers. This is the normal state.
3. **Under review** — The definition is being updated (e.g., scope change, new expectations) (optional).
4. **Retired** — The service is no longer offered; the definition may be kept for history but marked as retired.

Many organizations keep this simple: a service is either "defined and live" or "retired." Refinement is continuous rather than a separate stage.

## Getting Started

- **Minimal template:** For each significant service, maintain one place (document, wiki, or catalog) with: name, purpose (what it does and for whom), scope (what is in and out), how to request or access it, and how to get support. Optionally: owner, key dependencies (systems or teams), and one or two expectations (e.g., "available during business hours").
- **When to introduce:** Introduce when providers and consumers disagree about what the service includes or who it is for; when new team members or users have no single place to learn what exists; or when prioritization and improvement efforts lack a clear "service" to attach to. Pain signals include "we thought that was in scope," duplicated or conflicting descriptions, and "we don’t have a list of what we offer."

## Processes

- **Defining a service:** The service owner (or designee) drafts or updates the description: name, purpose, scope, users, capabilities, and how to request and get support. Consumers and key stakeholders are consulted so that the definition matches reality and expectations.
- **Publishing and maintaining:** The definition is published in a place that providers and consumers can find (catalog, wiki, intranet). It is updated when the service changes (new features, scope change, new owner) so that it stays current.
- **Setting expectations:** Where useful, the provider and consumer agree on one or more expectations (availability, response time, etc.). These may be informal ("we aim for 99% uptime") or formal (SLA). The expectations are recorded with the definition and used for prioritization and reporting.
- **Using the definition:** Incidents, problems, and changes are associated with the service where possible so that impact and trends can be reported per service. The definition is the reference for "what is this service?" in those disciplines.

## Adaptation

- **Level of formality:** Service definitions can range from a short wiki page to a formal catalog with approval workflows. Use the level that your organization will actually maintain and use—overly formal definitions that go stale are worse than simple, living descriptions.
- **Granularity:** One organization may define "Email" as a single service; another may split "Email," "Calendar," and "Collaboration." Choose granularity that matches how you deliver, consume, and report—e.g., one definition per team or per major capability.
- **Pitfalls:** Writing definitions that no one reads or updates; defining every small capability as a separate service so that the list is overwhelming; or treating the definition as a one-time project instead of a living artifact. Tie updates to real changes (new services, scope changes) and use the definition in incident, change, and improvement work so it stays relevant.

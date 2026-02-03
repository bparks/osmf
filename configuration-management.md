# Configuration Management

Knowing what exists in the environment, how it is related, and where to find accurate information about it. Organizations build and maintain a configuration model so that changes, incidents, and problems can be understood in context.

## Primary Objects/Actors

- **Configuration item (CI)** — Any component that the organization chooses to track as part of the live environment: a server, application, network device, database, contract, or document. Each CI is one record with a unique identifier, type, and key attributes (name, owner, location, version, status).
- **Configuration record** — The stored information about a CI: what it is, where it lives, what it depends on, and (where useful) its history. The "record" is the data; the "item" is the thing in the world the record describes.

## Supporting Objects/Actors

- **Relationship** — A link between two CIs (e.g., "runs on," "depends on," "connects to"). Relationships support impact analysis: if this server is down, which services are affected?
- **Attribute** — A named property of a CI (e.g., IP address, version, owner). Organizations standardize a small set of attributes per CI type so that reporting and automation are possible.

## Related Objects/Actors

- **Incident / Problem** — Incidents and problems often reference the CI(s) involved so that trends and impact can be analyzed.
- **Change** — Changes typically target one or more CIs; the configuration model helps assess impact and plan rollbacks.
- **Asset** — Some organizations link CIs to assets (e.g., the software or hardware asset that the CI represents or runs on); the boundary between "configuration" and "asset" is defined locally.

## Lifecycles

CIs usually have a simple lifecycle tied to their real-world state:

1. **Planned** — Approved to be introduced; not yet in the environment (optional; not all organizations use this).
2. **Active / Live** — In use in the environment and expected to be there. This is the normal state for production CIs.
3. **Under change** — Temporarily in a non-normal state due to maintenance or deployment (optional).
4. **Retired / Decommissioned** — No longer in use. The record may be kept for history but is excluded from "current" views and impact analysis.

Keeping the lifecycle small (e.g., active vs. retired) reduces confusion and makes it easier to keep the model in sync with reality.

## Getting Started

- **Minimal template:** A single source of truth (database, spreadsheet, or tool) listing the components that matter for changes and incidents: e.g., key servers, applications, and critical dependencies. For each, record at least: unique ID, name, type, and owner or team. Add relationships (e.g., "Application X runs on Server Y") when you need impact or dependency views.
- **When to introduce:** Introduce when people repeatedly ask "what runs where?" or "what will this change affect?"; when incidents and changes are hard to assess because no one has a clear picture of the environment; or when new team members take a long time to understand the landscape. Pain signals include duplicated or contradictory diagrams and "tribal knowledge" as the only map.

## Processes

- **Defining the model:** Decide which CI types to track (e.g., server, application, database) and which attributes and relationships each has. Start with what you need for change impact and incident diagnosis; expand only when new use cases justify it.
- **Populating and maintaining:** Initial data comes from discovery tools, existing docs, or manual entry. Keeping it accurate requires that changes (and decommissions) update the configuration record—often by making it part of the change or release process.
- **Using the model:** Incidents and problems reference CIs; changes list affected CIs and use relationships for impact analysis. Reports and dashboards filter by CI type, owner, or relationship to show coverage and drift.

## Adaptation

- **Scope:** Not everything needs to be a CI. Many organizations track only production or only components that have caused incidents or changes. Start narrow and expand when a clear need (e.g., "we need to know all apps on this server") appears.
- **Accuracy vs. completeness:** A smaller, accurate model is more useful than a large, outdated one. Prefer processes that keep a subset of CIs correct (e.g., "every change must update the CMDB") over trying to document everything at once.
- **Pitfalls:** Building a huge configuration repository that no one maintains; requiring too many attributes so that people never fill them in; or treating the model as separate from daily work so that it drifts. Tie updates to change and decommission workflows so the model stays alive.

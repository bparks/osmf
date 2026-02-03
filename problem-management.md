# Problem Management

Identifying and addressing the root causes of recurring or serious incidents so that the same failures do not keep happening. Organizations use problem records when they want to go beyond "fix it and close the ticket" to "fix it for good."

## Primary Objects/Actors

- **Problem** — A record for a root cause or underlying issue that has led to one or more incidents, or could lead to more. It is tracked until a permanent fix (or accepted risk) is in place. The problem is the thing to be understood and removed or mitigated; the incident(s) are the symptoms.
- **Known error** — In many organizations, a problem becomes a "known error" once the root cause is identified and a workaround or permanent fix is documented. The term is used so that future incidents can be matched quickly to existing knowledge.

## Supporting Objects/Actors

- **Root cause analysis (RCA)** — The output of investigation: what actually caused the failure, often documented in a short report or structured template (timeline, cause, contributing factors, actions).
- **Workaround** — A temporary way to restore or preserve service when a full fix is not yet available. Documented so support can apply it for future related incidents.

## Related Objects/Actors

- **Incident** — Problems are usually raised from one or more incidents. Linking problems to incidents shows which tickets are "symptoms" of the same underlying issue.
- **Change** — Implementing a permanent fix is often done via a change. The problem record may reference the change(s) that address it.
- **Configuration item** — The component or service where the root cause lies is often referenced from configuration management.

## Lifecycles

Problems typically follow a path from detection to closure:

1. **Raised / Open** — A problem has been identified (e.g., from a major incident, a trend of similar incidents, or proactive analysis). Investigation has not yet concluded.
2. **Under investigation** — Root cause analysis is in progress; workarounds may already be in use for related incidents.
3. **Known error** — Root cause is known; workaround and/or permanent fix is documented. The organization may still be implementing the fix.
4. **Resolved / Closed** — A permanent fix has been implemented and verified, or the organization has accepted the risk and decided not to fix it. No further action is planned.

Some organizations keep problems in a single "open" state until closed; others use the stages above to drive review meetings and reporting.

## Getting Started

- **Minimal template:** A way to record problems (linked to one or more incidents), with: short description, when it was raised, who owns it, current status, and when it was closed. Optionally: root cause summary, workaround, and link to change(s) that fix it.
- **When to introduce:** Introduce when the same kinds of incidents keep recurring and no one is assigned to find and fix the cause; after a major outage when leadership wants a formal review; or when support repeatedly applies the same workaround with no path to a permanent fix. Pain signals include "we've seen this five times this month" and "we never get time to fix the real cause."

## Processes

- **Raising a problem:** Triggered by a major incident, a cluster of similar incidents, or a proactive review. Someone creates a problem record and links the relevant incident(s). Ownership is assigned (often to a senior engineer or dedicated role).
- **Root cause analysis:** The owner gathers evidence (logs, changes, timeline), may run a blameless or structured review, and documents root cause and contributing factors. The output is used to decide on workaround vs. permanent fix.
- **Workaround and fix:** A workaround is documented and shared with support so related incidents can be resolved quickly. A permanent fix is planned (often as a change) and tracked until implemented. The problem is closed when the fix is in place or risk is accepted.

## Adaptation

- **What gets a problem record:** Some organizations only open problems for major incidents or repeated patterns; others open one for any incident where root cause is unknown and worth investigating. Choose a threshold that matches capacity and impact—too many open problems with no capacity to work them undermines the discipline.
- **Formality of RCA:** RCA can range from a short narrative in the problem ticket to a formal document with timelines and action owners. Use the level of formality that your organization will actually read and act on.
- **Pitfalls:** Treating problem management as paperwork that never leads to changes; closing problems without a real fix or explicit risk acceptance; or raising problems for every single incident so that the backlog becomes meaningless. Focus on problems that, if fixed, would materially reduce future incidents.

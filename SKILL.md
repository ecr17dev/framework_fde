---

name: fde-ops-framework
description: operational framework for forward deployed engineers and technical implementation teams. use when the user needs to manage, accelerate, or standardize fde work: customer onboarding, discovery, technical blueprints, integrations, deployments, hypercare, support, incidents, runbooks, checklists, sows, metrics, governance, status reports, support handoffs, or continuous improvement for b2b technical delivery.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# FDE Ops Framework

Use this skill to help a user operate as a **Forward Deployed Engineer**, **Solutions Engineer**, **Implementation Engineer**, **Technical Delivery Lead**, or similar technical customer-facing role.

The goal is to turn technical customer work into a repeatable, traceable, and measurable operating system: from initial handoff to discovery, blueprint, integration, deployment, hypercare, support, and continuous improvement.

## Core principle

Act as an FDE operating copilot.

Do not provide generic advice when the user needs execution. Produce concrete artifacts the user can copy into GitHub, Linear, Jira, Notion, Confluence, Slack, email, or internal docs.

Always optimize for:

1. Clear objective.
2. Actionable next step.
3. Defined owners.
4. Visible risks and dependencies.
5. Reusable templates.
6. Delivery and quality metrics.
7. Clean, maintainable documentation.

## Operating modes

Choose the most relevant mode based on the user's request.

### 1. FDE system design

Use when the user wants to create or improve their operating system.

Typical outputs:

* Framework README.
* Repository structure.
* Operating model.
* RACI.
* Delivery lifecycle.
* Tooling map.
* Adoption roadmap.
* KPIs and governance.

### 2. Customer/account management

Use when the user is working with a specific customer or account.

Typical outputs:

* Account brief.
* Onboarding plan.
* Discovery memo.
* Stakeholder map.
* Risk register.
* Integration plan.
* Go-live plan.
* Weekly status report.
* Support handoff.

### 3. Technical discovery

Use when the user needs to understand the customer's problem, systems, constraints, or architecture.

Typical outputs:

* Discovery questions.
* System map.
* Dependency map.
* Functional requirements.
* Non-functional requirements.
* Acceptance criteria.
* Initial backlog.

### 4. Blueprint and integration

Use when the user needs to convert discovery into an executable technical plan.

Typical outputs:

* Technical blueprint.
* Target architecture.
* API/data/SSO integration plan.
* Environment plan.
* Test strategy.
* Secrets and permissions plan.
* Definition of Ready and Definition of Done.

### 5. Deployment, go-live, and hypercare

Use when the user needs to prepare or execute production rollout.

Typical outputs:

* Readiness checklist.
* Deployment plan.
* Rollback plan.
* Communication plan.
* Incident matrix.
* Operational runbook.
* Hypercare plan.

### 6. Incidents and support

Use when the user needs to respond to issues, tickets, or incidents.

Typical outputs:

* Severity classification.
* Incident timeline.
* Customer update.
* Mitigation runbook.
* Blameless postmortem.
* Corrective actions.
* Knowledge base article.

### 7. Metrics and continuous improvement

Use when the user wants to measure or scale the system.

Typical outputs:

* KPI catalog.
* Dashboard outline.
* Account scorecard.
* Monthly retro.
* Improvement backlog.
* Documentation freshness review.

## Default workflow

Use this workflow unless the user specifies another:

```text
handoff -> onboarding -> discovery -> blueprint -> integration -> readiness -> go-live -> hypercare -> handoff -> continuous improvement
```

For each phase, produce:

* Objective.
* Required inputs.
* Key activities.
* Expected outputs.
* Owners.
* Risks.
* Exit criteria.

## Response rules

### Be actionable

Return usable artifacts. Avoid abstract advice when the user needs execution.

Prefer:

* Tables.
* Checklists.
* Templates.
* Roadmaps.
* Phase plans.
* Ready-to-send messages.
* Document structures.

### Preserve traceability

When creating a plan, include at least:

* Owner.
* Date or cadence when relevant.
* Status.
* Dependency.
* Exit criteria.

### Make risks visible

For discovery, implementation, go-live, or incidents, always include a risk section.

Recommended format:

| Risk | Impact | Likelihood | Mitigation | Owner |
| ---- | ------ | ---------- | ---------- | ----- |

### Avoid overengineering

For MVPs, recommend the smallest set of tools and processes needed.

Rule of thumb:

* One source for code.
* One source for tickets.
* One source for documentation.
* One source for support.
* One source for metrics.

### Separate views

When the artifact involves communication or management, separate as needed:

* Executive view.
* Technical view.
* Operational view.
* Customer view.

## Recommended repository structure

When the user asks for a repo, README, or full system, use this as the base:

```text
fde-ops-framework/
├── README.md
├── docs/
│   ├── customer-onboarding.md
│   ├── discovery.md
│   ├── technical-blueprint.md
│   ├── deployment-and-hypercare.md
│   ├── support-and-incidents.md
│   └── metrics-and-governance.md
├── templates/
│   ├── intake-ticket.md
│   ├── runbook.md
│   ├── kickoff-email.md
│   ├── weekly-status-email.md
│   ├── incident-email.md
│   ├── sow.md
│   └── timeline.md
├── runbooks/
│   ├── deploy.md
│   ├── rollback.md
│   ├── api-integration.md
│   └── access-and-secrets.md
├── governance/
│   ├── raci.md
│   ├── severity-priority-matrix.md
│   ├── review-gates.md
│   └── documentation-owners.md
├── automation/
│   ├── issue-templates/
│   ├── pull-request-template.md
│   └── workflows/
└── metrics/
    ├── kpi-catalog.md
    └── dashboards/
```

## Framework phases

### 1. Handoff

Objective: receive enough commercial, strategic, and technical context to start.

Outputs:

* Master ticket.
* Customer and sponsor.
* Initial objective.
* Value hypothesis.
* Initial risks.
* Next milestone.

Key questions:

* Why does this project exist?
* What business outcome does the customer want?
* Who decides?
* Who owns technical operations?
* Which date matters?
* What happens if this is not delivered?

### 2. Onboarding

Objective: prepare minimum execution conditions.

Outputs:

* Communication channels.
* Accesses.
* Calendar.
* Stakeholders.
* Initial RACI.
* Dependency register.

Checklist:

* [ ] Sponsor identified.
* [ ] Product owner identified.
* [ ] Technical admin identified.
* [ ] Official channel created.
* [ ] Escalation channel defined.
* [ ] Access requests submitted.
* [ ] Environments identified.
* [ ] Initial risks logged.

### 3. Discovery

Objective: understand problem, systems, users, data, and constraints.

Outputs:

* Discovery memo.
* System map.
* Dependency map.
* Functional requirements.
* Non-functional requirements.
* Acceptance criteria.
* Initial backlog.

Technical questions:

* Which systems are involved?
* Which APIs or data are required?
* Where are the environments?
* Which security constraints exist?
* What latency, volume, or availability is expected?
* Who approves changes?
* How will success be tested?

### 4. Technical blueprint

Objective: convert discovery into an executable design.

Outputs:

* Target architecture.
* Integration plan.
* Data plan.
* Permissions plan.
* Test plan.
* Deployment plan.
* Risks and trade-offs.

Exit criteria:

* Scope is clear.
* Dependencies are known.
* Acceptance criteria are defined.
* Critical risks are mitigated or accepted.
* Owner assigned per stream.

### 5. Integration

Objective: build or configure the solution.

Outputs:

* Code or configuration.
* Pipelines.
* Environments.
* Secrets and permissions.
* Tests.
* Technical documentation.

Checklist:

* [ ] Repo ready.
* [ ] Owners defined.
* [ ] Branch protections or equivalent rules enabled.
* [ ] Base pipeline active.
* [ ] Environments defined.
* [ ] Secrets configured.
* [ ] Minimum tests created.
* [ ] Minimum observability defined.

### 6. Readiness

Objective: validate production readiness.

Outputs:

* Go-live checklist.
* Rollback plan.
* Dashboard.
* Alerts.
* Runbook.
* Approvals.

Do not go live without:

* Technical owner.
* Business owner.
* Rollback plan.
* Smoke tests.
* Incident channel.
* Minimum observability.
* Prepared communication.

### 7. Go-live

Objective: deploy with control and response capability.

Outputs:

* Deployment executed.
* Smoke tests completed.
* Status communicated.
* Incidents logged.
* Hypercare started.

### 8. Hypercare

Objective: support initial stabilization.

Outputs:

* Active monitoring.
* Triaged tickets.
* Recurring issues identified.
* KB updated.
* Handoff prepared.

### 9. Support handoff

Objective: transfer steady-state operations.

Outputs:

* Final runbooks.
* KB.
* SLAs.
* Owners.
* Escalation path.
* Known issues.

### 10. Continuous improvement

Objective: learn and improve the framework.

Outputs:

* Retro.
* Postmortems.
* Improvement backlog.
* Template updates.
* Automation updates.
* Metric updates.

## Base templates

### Intake ticket

```md
# FDE Intake

## Account data
- Customer:
- Sponsor:
- Product owner:
- Technical admin:
- Engagement type:

## Business objective
- Problem:
- Affected KPI:
- Target date:
- Risk if unresolved:

## Technical context
- Product / module:
- External systems:
- Data / APIs:
- Security requirements:
- Environments:

## Success definition
- Acceptance criteria:
- Expected evidence:
- Validating stakeholder:

## Risks and dependencies
- Main risk:
- External dependencies:
- Current blockers:

## Next step
- Owner:
- Date:
- Deliverable:
```

### Discovery memo

```md
# Discovery Memo

## Executive summary

## Customer objective

## Stakeholders
| Name | Role | Responsibility | Influence |
|---|---|---|---|

## Current state

## Target state

## Systems involved
| System | Owner | Purpose | Dependencies | Risks |
|---|---|---|---|---|

## Functional requirements

## Non-functional requirements

## Constraints

## Assumptions

## Risks
| Risk | Impact | Likelihood | Mitigation | Owner |
|---|---|---|---|---|

## Acceptance criteria

## Initial backlog

## Next steps
```

### Technical blueprint

```md
# Technical Blueprint

## Objective

## Proposed architecture

## Components
| Component | Responsibility | Owner | Status |
|---|---|---|---|

## Data flow

## Integrations
| Integration | Type | Source system | Target system | Risk |
|---|---|---|---|---|

## Security and access

## Environments

## Observability

## Test plan

## Deployment plan

## Rollback plan

## Risks and trade-offs

## Exit criteria
```

### Weekly status

```md
# Weekly Status

## Executive summary
- Customer:
- Overall status: green / yellow / red
- Week:
- FDE owner:

## Progress

## Risks and blockers

## Decisions needed

## Scope changes

## Next milestone
- Milestone:
- Date:
- Exit criteria:

## Open actions
| Action | Owner | Date | Status |
|---|---|---|---|
```

### Operational runbook

```md
# Operational Runbook

## Purpose

## Scope

## Activation signals

## Quick diagnosis
1. Check main dashboard.
2. Confirm dependency status.
3. Review recent errors.
4. Review recent deployments.
5. Classify severity and impact.

## Immediate mitigation

## Rollback

## Escalation
- Incident Commander:
- Technical Lead:
- Customer Liaison:
- Channel:
- Max time before escalation:

## Closure validation
- Smoke test:
- KPI normalized:
- Customer confirmation:
- Related ticket:
```

### Incident

```md
# Incident

## Summary
- Customer:
- Affected service:
- Severity:
- Status:
- Start time:
- Detection time:
- Resolution time:

## Impact

## Roles
- Incident Commander:
- Technical Lead:
- Customer Liaison:

## Timeline
| Time | Event | Owner |
|---|---|---|

## Mitigation

## Root cause

## Follow-up actions
| Action | Owner | Date | Status |
|---|---|---|---|

## Customer communication
```

## Recommended KPIs

When the user asks for metrics, use these categories.

### Delivery

* Time to kickoff.
* Time to first value.
* Time to production.
* Change lead time.
* Deployment frequency.
* Milestone completion rate.

### Reliability

* Change fail rate.
* Failed deployment recovery time.
* MTTA.
* MTTR.
* SLA compliance.
* Incidents by severity.

### Adoption and support

* Ticket reopen rate.
* KB deflection.
* Delivered feature usage.
* Customer satisfaction.
* Open risks by account.

### FDE system quality

* Documentation freshness.
* Projects with approved blueprint.
* Go-lives with rollback plan.
* Incidents with postmortem.
* Framework improvements shipped per month.

## Severity matrix

Use this default matrix if the user does not provide one.

| Severity | Description                         | Example                                     | Expected response                               |
| -------- | ----------------------------------- | ------------------------------------------- | ----------------------------------------------- |
| Sev 1    | Critical production impact          | Service down or customer fully blocked      | Immediate response, war room, frequent updates. |
| Sev 2    | High impact with limited workaround | Key feature degraded                        | Priority response, technical owner assigned.    |
| Sev 3    | Medium impact with workaround       | Partial error or specific user affected     | Normal triage, correction plan.                 |
| Sev 4    | Low impact or request               | Question, minor improvement, cosmetic issue | Backlog or regular support.                     |

## Tooling guidance

Do not impose tools. Adapt to the user's organization.

### Repo-first stack

* Code: GitHub.
* Planning: GitHub Projects, Linear, or Jira.
* CI/CD: GitHub Actions.
* IaC: OpenTofu or Terraform.
* Observability: OpenTelemetry + Prometheus + Grafana, or Datadog.
* Service desk: Jira Service Management or equivalent.
* Documentation: Confluence, Notion, or Markdown in repo.
* Communication: Slack or Teams.

### Microsoft-first stack

* Code: Azure Repos or GitHub.
* Planning: Azure Boards.
* CI/CD: Azure Pipelines or GitHub Actions.
* Observability: Azure Monitor.
* Communication: Teams.
* Documentation: SharePoint, Confluence, or Notion.

## Output patterns

### Plans

Use:

```md
## Objective

## Assumptions

## Phase plan
| Phase | Objective | Activities | Owner | Output | Exit criteria |
|---|---|---|---|---|---|

## Risks
| Risk | Impact | Mitigation | Owner |
|---|---|---|---|

## Next steps
```

### Diagnostics

Use:

```md
## Diagnosis

## Observed signals

## Hypotheses
| Hypothesis | Evidence | How to validate | Priority |
|---|---|---|---|

## Immediate actions

## Preventive actions
```

### GitHub documentation

Use standard Markdown.

Do not use internal citation tokens, hidden UI characters, or non-GitHub formats.

Prefer:

* Clear headings.
* Simple tables.
* `- [ ]` checklists.
* Language-tagged code blocks.
* Mermaid only when useful.
* Normal Markdown links.

## Quality checklist

Before finalizing, verify:

* Can the user copy and use the output?
* Are owners, outputs, or next steps clear?
* Are risks and dependencies visible?
* Is the level of detail appropriate for an MVP, not excessive bureaucracy?
* Does the format work in GitHub, Jira, Linear, Notion, Confluence, or Slack?
* Does the artifact reduce future repetitive work?

## Handling incomplete information

If data is missing, do one of two things:

1. If speed matters, make reasonable assumptions and label them.
2. If the missing data would materially change the result, ask a few concrete questions.

Assumption format:

```md
## Assumptions
- I assume the customer is B2B SaaS.
- I assume the team uses GitHub or an equivalent tool.
- I assume the goal is an operational MVP before automation.
```

## Language and tone

Respond in the user's language unless they request otherwise.

For Spanish users, it is acceptable to answer in Spanish while keeping reusable templates and skill logic in English when requested.

Recommended tone:

* Practical.
* Strategic but executable.
* Low jargon.
* Delivery-oriented.
* Focused on systems, not isolated tasks.

## Conceptual references

Use these as inspiration when relevant, but do not over-cite unless the user asks for research:

* DORA metrics.
* Google SRE practices.
* AWS Well-Architected operational excellence.
* Microsoft Cloud Adoption Framework.
* Atlassian incident management.
* GitHub Actions, Projects, CODEOWNERS, and branch protection.
* OpenTelemetry, Prometheus, Grafana, and Datadog observability patterns.

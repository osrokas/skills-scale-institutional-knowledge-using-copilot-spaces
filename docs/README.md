# OctoAcme Project Management Docs

This README is the central index for OctoAcme's project management documentation. Use it to orient yourself to the overall methodology and navigate to any detailed guide.

---

## Project Management Process Overview

OctoAcme uses a lightweight, iterative approach to manage cross-functional projects, grounded in the following principles:

- **Customer-first** — prioritize customer value and usability.
- **Iterative delivery** — deliver small, testable increments.
- **Clear ownership** — each project has a named Project Manager (PM) and Product Manager (PdM).
- **Data-informed decisions** — measure impact and iterate based on evidence.
- **Psychological safety** — encourage feedback and continuous learning.

### Key Workflows

| # | Stage | What happens |
|---|-------|--------------|
| 1 | **Initiation** | Validate the problem, define goals, identify stakeholders, draft the Project Charter. |
| 2 | **Planning** | Define scope, resources, milestones, and dependencies; align on Definition of Done. |
| 3 | **Execution & Tracking** | Build, test, and iterate; run standups, sprint reviews, and issue tracking. |
| 4 | **Risks & Communication** | Maintain the risk register; publish weekly status updates; escalate blockers early. |
| 5 | **Release & Deployment** | Verify pre-release criteria, run deployment checklist, smoke-test, and announce. |
| 6 | **Retrospective & Continuous Improvement** | Review outcomes, capture lessons learned, and drive process improvements. |

### Roles & Personas

| Role | Responsibilities |
|------|-----------------|
| **Project Manager (PM)** | Coordinates delivery, schedules, risks, and communications. |
| **Product Manager (PdM)** | Defines outcomes, prioritizes backlog, and measures success. |
| **Developers** | Implement features; participate in design and code reviews. |
| **QA / Testing** | Validate quality and acceptance criteria. |
| **Stakeholders / Sponsors** | Provide inputs, approvals, and escalation decisions. |

### Communication Strategies

- **Cadences** — Weekly PM + PdM sync; twice-weekly delivery standups; monthly stakeholder updates.
- **Status template** — Progress this week · Next steps · Risks & blockers · Asks / decisions needed.
- **Single source of truth** — Project README or release doc for live status.
- **Escalation path** — Team → PM → Product Lead → Sponsor (security incidents follow the security runbook).

### Quality Assurance Practices

- **CI** — All PRs require passing CI and security scans before merge.
- **PR practices** — Acceptance criteria documented; code review required.
- **Testing strategy** — Unit, integration, and smoke tests; QA validates each increment.
- **Release checklist** — Staging smoke tests, post-deploy verification, and release notes completed before production.
- **Rollback / incident playbook** — Trigger incident response, rollback to last known-good release, triage root cause, and schedule a blameless retrospective.

---

## Docs Index

| Document | Description |
|----------|-------------|
| [Project Management Overview](octoacme-project-management-overview.md) | Principles, core roles, key artifacts, and lifecycle summary. |
| [Project Initiation](octoacme-project-initiation.md) | Problem validation, stakeholder identification, and Project Charter. |
| [Project Planning](octoacme-project-planning.md) | Scope, resources, milestones, and dependency management. |
| [Execution & Tracking](octoacme-execution-and-tracking.md) | Delivery cadence, issue tracking, and sprint reviews. |
| [Risks & Communication](octoacme-risks-and-communication.md) | Risk register, communication templates, and escalation paths. |
| [Release & Deployment](octoacme-release-and-deployment.md) | Release types, deployment checklist, and rollback playbook. |
| [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) | Retrospective format and continuous improvement practices. |
| [Roles & Personas](octoacme-roles-and-personas.md) | Detailed role definitions for PM, PdM, Developers, and QA. |

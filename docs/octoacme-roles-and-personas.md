# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## Release Manager

### Role Summary
The Release Manager coordinates releases across teams, owns the release timeline and readiness criteria, and ensures smooth deployment and post-release verification.

### Responsibilities
- Maintain the release calendar and coordinate release windows.
- Verify release readiness checklist (PRs merged, CI passing, smoke tests, rollback plan, release notes).
- Coordinate cross-team deployments and schedule communications with stakeholders and support.
- Make or coordinate the Go/No-Go decision for production deployments.

### Goals
- Reduce release-related incidents and rollbacks.
- Ensure predictable, well-communicated releases.

### Typical Communication & Interaction
- Works closely with Project Manager (scheduling, dependencies), Developers and QA (readiness), Support Lead (post-release verification), and Product Manager (timing and stakeholder comms).
- Escalates deployment blockers to PM and Product Lead; surfaces high-impact risks to Sponsor.
- Decisions owned: Go/No-Go for production deployments, release window scheduling, rollback initiation.
- Handoffs: Receives readiness signal from QA Lead; hands off to Support/On-call Lead after deployment.
- Escalation: Unresolved deployment blockers escalate to PM → Product Lead → Sponsor.
- RACI: **Responsible** for Release Decision; **Consulted** on Test Strategy and Change Approval.

---

## QA Lead

### Role Summary
The QA Lead owns the test strategy, ensures quality gates are met, manages defect triage, and communicates testing status to the team.

### Responsibilities
- Define and maintain the test strategy, test plan, and acceptance criteria coverage.
- Manage test environments, test data, and automation suites.
- Lead defect triage and track resolution of critical issues before release.
- Communicate testing status and risk to PM, Product Manager, and Release Manager.
- Review acceptance criteria with Product Manager and ensure testability.

### Goals
- Ensure all acceptance criteria are covered by tests before release.
- Minimize post-release defects through rigorous pre-release testing.
- Maintain clear visibility into quality health across the project.

### Typical Communication & Interaction
- Works with Developers (test coverage, defect resolution), PM (status and risk), Product Manager (acceptance criteria), and Release Manager (readiness sign-off).
- Escalates critical defects or unresolved test blockers to PM.
- Decisions owned: Test strategy, defect severity classification, testing go/no-go signal.
- Handoffs: Provides release readiness signal to Release Manager; escalates unresolved defects to PM.
- Escalation: Critical defects not resolved by release window escalate to PM → Product Lead.
- RACI: **Responsible** for Test Strategy and Acceptance Criteria coverage; **Consulted** on Release Decision.

---

## Technical Architect

### Role Summary
The Technical Architect oversees system design decisions, ensures technical alignment across teams, and advises on feasibility, scalability, and risk.

### Responsibilities
- Review and approve solution architecture and technical designs.
- Identify technical risks and propose mitigations.
- Advise Developers on implementation approaches and non-functional requirements.
- Ensure alignment with organizational standards and long-term technical direction.
- Participate in planning to assess feasibility and provide effort guidance.

### Goals
- Deliver a coherent, maintainable, and scalable technical solution.
- Prevent architectural drift and accumulation of technical debt.
- Ensure technical decisions are well-documented and understood by the team.

### Typical Communication & Interaction
- Advises Developers (design guidance), PM (feasibility and risk), and Product Manager (trade-off analysis).
- Reviews technical plans and escalates significant architectural risks to PM and leadership.
- Decisions owned: Architecture and design approvals, technical standards, feasibility assessments.
- Handoffs: Provides design approval before development begins; flags unresolved technical risks to PM.
- Escalation: High-impact architecture risks escalate to PM → Product Lead → Sponsor.
- RACI: **Responsible** for architecture decisions; **Consulted** on Requirements, Test Strategy, and Change Approval.

---

## Change Manager

### Role Summary
The Change Manager manages change requests that affect scope, schedule, or production behavior, analyzes impact, facilitates approvals, and ensures documentation is updated.

### Responsibilities
- Receive, log, and evaluate change requests for impact on scope, schedule, cost, and risk.
- Facilitate change approval with relevant stakeholders (PM, Product Lead, Sponsor).
- Communicate approved changes to all affected teams and update documentation.
- Oversee risk mitigation planning for approved changes.
- Maintain the change log throughout the project lifecycle.

### Goals
- Ensure all significant changes are evaluated, approved, and communicated.
- Minimize uncontrolled scope creep and unplanned rework.
- Maintain an auditable change history.

### Typical Communication & Interaction
- Works closely with PM (impact assessment, scheduling), Stakeholders (approval and communication), Developers (impact on implementation), and Release Manager (impact on release plan).
- Escalates high-impact or disputed changes to PM → Product Lead → Sponsor.
- Decisions owned: Change log maintenance, facilitating change approval, communication of approved changes.
- Handoffs: Receives change requests from any stakeholder; hands approved changes to PM and Release Manager.
- Escalation: Unapproved high-impact changes escalate to PM → Product Lead → Sponsor.
- RACI: **Responsible** for Change Approval facilitation; **Consulted** on Release Decision and scheduling.

---

## Support / On-call Lead

### Role Summary
The Support/On-call Lead is the primary point of contact for production incidents, owns incident triage and escalation, and coordinates post-release monitoring and verification.

### Responsibilities
- Monitor production systems after deployment and during on-call windows.
- Triage, classify, and route production incidents to the appropriate team.
- Communicate incident status and resolution timelines to stakeholders.
- Verify key user flows and metrics after each release.
- Maintain runbooks and on-call rotation schedules.

### Goals
- Minimize mean time to detect (MTTD) and mean time to resolve (MTTR) for production incidents.
- Ensure production health is confirmed after every release.
- Maintain up-to-date runbooks for common incident scenarios.

### Typical Communication & Interaction
- Works with Release Manager (post-release verification), Developers (incident resolution), PM (status updates), and Stakeholders (impact communication).
- Escalates unresolved incidents to PM and engineering leads.
- Decisions owned: Incident severity classification, escalation triggers, on-call runbooks.
- Handoffs: Receives deployment completion signal from Release Manager; escalates unresolved incidents to PM.
- Escalation: P1/critical incidents escalate to PM → Product Lead → Sponsor.
- RACI: **Responsible** for Incident Triage; **Consulted** on Release Decision and rollback execution.

---

## Security Liaison

### Role Summary
The Security Liaison ensures security requirements are incorporated into design, development, and release processes, and serves as the point of contact for security reviews and compliance.

### Responsibilities
- Review architecture and design for security risks and vulnerabilities.
- Define and verify security acceptance criteria (e.g., dependency scans, pen testing, secrets management).
- Participate in release readiness checks to confirm security scans have passed.
- Escalate unresolved security risks to PM and leadership.
- Maintain security-related documentation and compliance evidence.

### Goals
- Ensure no known high-severity vulnerabilities are released to production.
- Embed security checkpoints into the development and release lifecycle.
- Support compliance requirements and security audits.

### Typical Communication & Interaction
- Works with Technical Architect (design reviews), Developers (secure coding, dependency scanning), Release Manager (release readiness), and PM (risk reporting).
- Escalates unresolved security findings to PM → Product Lead → Sponsor before release.
- Decisions owned: Security acceptance criteria, security sign-off for releases, escalation of critical vulnerabilities.
- Handoffs: Provides security readiness signal to Release Manager; escalates unresolved risks to PM.
- Escalation: Critical or unresolved security issues block release until escalated to PM → Product Lead → Sponsor.
- RACI: **Responsible** for security review; **Consulted** on architecture decisions, Test Strategy, and Release Decision.

---

## RACI Summary

The table below shows typical ownership for key activities across roles.

| Activity               | Project Manager | Product Manager | Developer    | QA Lead      | Release Manager | Technical Architect | Change Manager | Support Lead | Security Liaison |
|------------------------|-----------------|-----------------|--------------|--------------|-----------------|---------------------|----------------|--------------|------------------|
| Requirements           | Accountable     | Responsible     | Consulted    | Consulted    | Informed        | Consulted           | Informed       | Informed     | Consulted        |
| Acceptance Criteria    | Accountable     | Responsible     | Consulted    | Responsible  | Consulted       | Consulted           | Informed       | Informed     | Consulted        |
| Test Strategy          | Accountable     | Informed        | Consulted    | Responsible  | Consulted       | Consulted           | Informed       | Consulted    | Consulted        |
| Release Decision       | Accountable     | Consulted       | Consulted    | Consulted    | Responsible     | Consulted           | Consulted      | Consulted    | Consulted        |
| Incident Triage        | Accountable     | Informed        | Consulted    | Informed     | Consulted       | Consulted           | Informed       | Responsible  | Consulted        |
| Change Approval        | Accountable     | Consulted       | Informed     | Consulted    | Consulted       | Consulted           | Responsible    | Informed     | Consulted        |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.


# OctoAcme — Change Management Guide

## Purpose
Provide a lightweight, consistent process for raising, evaluating, approving, and communicating changes that affect project scope, schedule, or production behavior.

## When to Use
Use this process for any change that:
- Alters agreed-upon scope, timeline, or budget.
- Modifies production configuration, data schema, or infrastructure.
- Introduces new dependencies or removes existing functionality.
- Has material impact on stakeholders, compliance, or release plans.

---

## Change Management Process

### 1. Raise a Change Request
Anyone on the team may raise a change request. Complete the Change Request template below and submit it to the Change Manager (or PM if no Change Manager is assigned).

### 2. Evaluate Impact
The Change Manager works with PM, Technical Architect, and affected team members to assess:
- Impact on scope, schedule, cost, and quality.
- Technical feasibility and risks.
- Effect on active releases or production systems.

### 3. Approve or Reject
- **Low-impact changes** (no schedule or scope change): PM approves.
- **Medium-impact changes** (schedule or scope adjustment): PM + Product Lead approve.
- **High-impact changes** (significant scope, cost, or risk): PM + Product Lead + Sponsor approve.

### 4. Communicate and Implement
- Change Manager notifies all affected teams and stakeholders of the decision.
- PM updates project plan, risk register, and documentation.
- Release Manager is notified of any changes affecting the release plan.
- Change log is updated with decision, rationale, and date.

### 5. Monitor and Close
- PM and Change Manager verify the change was implemented as approved.
- Change request is closed in the log with outcome notes.

---

## Change Request Template

```
Title: [Brief title of the change]

Description:
[What is changing and why?]

Impact:
- Scope: [What scope items are added, removed, or modified?]
- Schedule: [Does this affect the timeline or milestone dates?]
- Cost / Resources: [Any additional effort or budget required?]
- Risk: [What new risks does this change introduce?]
- Production / Release: [Does this affect a live system or upcoming release?]

Rollback Plan:
[How can this change be reversed if it causes issues?]

Requested by: [Name / Role]
Date raised: [YYYY-MM-DD]
Target decision date: [YYYY-MM-DD]

Approvers:
- [ ] PM
- [ ] Product Lead (if medium/high impact)
- [ ] Sponsor (if high impact)

Decision: [ ] Approved  [ ] Rejected  [ ] Deferred
Decision date: [YYYY-MM-DD]
Notes: [Rationale or conditions]
```

---

## Escalation Flow

```
Change raised
    │
    ▼
Change Manager / PM evaluates impact
    │
    ├─ Low impact ──────────────► PM approves
    │
    ├─ Medium impact ───────────► PM + Product Lead approve
    │
    └─ High impact / Disputed ──► PM + Product Lead + Sponsor approve
```

If a change is time-sensitive and approvers are unavailable, the PM may make a provisional decision and seek ratification within 24 hours.

---

## Roles and Interactions

| Role | Responsibility in Change Management |
|------|-------------------------------------|
| Change Manager | Logs, evaluates, and facilitates approval of change requests; maintains the change log; communicates decisions to all stakeholders. |
| Project Manager | Primary approver for low-impact changes; coordinates schedule and scope updates; escalates medium/high-impact changes. |
| Release Manager | Notified of all changes affecting release plans; adjusts release calendar and readiness criteria as needed. |
| Stakeholders | Raise change requests; participate in approval for changes within their domain; receive communication of approved changes. |
| Technical Architect | Assesses technical feasibility and risk of proposed changes; advises on implementation impact. |

---

## Change Log

Maintain a change log (e.g., in the project wiki or repo) with the following columns:

| ID | Title | Raised By | Date Raised | Impact Level | Decision | Decision Date | Notes |
|----|-------|-----------|-------------|--------------|----------|---------------|-------|
| CR-001 | Example change | PM | 2025-01-10 | Low | Approved | 2025-01-11 | No schedule impact |

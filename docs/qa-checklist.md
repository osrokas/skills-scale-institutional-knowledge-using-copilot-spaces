# OctoAcme — QA Checklist

A lightweight QA checklist for owners to use during planning and before release.

---

## Planning Phase

- [ ] Acceptance criteria defined for all features in scope and reviewed with QA Lead.
- [ ] Test strategy documented (unit, integration, end-to-end, regression scope).
- [ ] Test ownership assigned: who owns unit tests, integration tests, and end-to-end tests.
- [ ] Test data requirements identified and test data prepared or mocked.
- [ ] Test environments provisioned and confirmed operational.
- [ ] Non-functional requirements covered (performance, accessibility, security) if applicable.

---

## During Development

- [ ] Developers writing tests alongside feature implementation (unit and integration).
- [ ] Test coverage thresholds met (confirm against project standards).
- [ ] Integration test owners running tests against the latest builds.
- [ ] New defects logged, triaged, and prioritized (see Defect Triage below).
- [ ] Regression suite updated if new features affect existing flows.

---

## Pre-Release

- [ ] All acceptance criteria covered by automated or manual tests.
- [ ] Regression test suite executed; no open regressions of severity High or Critical.
- [ ] All critical and high-severity defects resolved or have an accepted mitigation.
- [ ] Test environment mirrors production configuration (data, config, dependencies).
- [ ] Security acceptance criteria verified (dependency scan, secrets scan).
- [ ] QA Lead sign-off: testing go/no-go signal provided to Release Manager.

---

## Defect Triage Guidelines

| Severity | Definition | Target Resolution |
|----------|------------|-------------------|
| Critical | Data loss, system unavailable, security vulnerability | Block release; must fix before deployment |
| High     | Core user flow broken, significant regression | Fix before release; escalate to PM if not resolved |
| Medium   | Partial feature impacted; workaround available | Fix in current or next sprint |
| Low      | Minor UI issues, cosmetic defects | Backlog; fix at team discretion |

- Triage happens at minimum once per sprint and before each release.
- QA Lead escalates unresolved Critical or High defects to PM before release.

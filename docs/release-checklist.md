# OctoAcme — Release Checklist

A practical, step-by-step checklist for Release Manager, PM, Developers, QA, and Support to follow for minor and major releases.

---

## Pre-Release

### Code & QA Readiness
- [ ] All acceptance criteria for this release are met and verified.
- [ ] All required PRs are merged to the release branch.
- [ ] CI/CD pipeline is green (build, unit tests, integration tests).
- [ ] Security scan completed; no high-severity findings are unresolved.
- [ ] Release notes drafted and reviewed by Product Manager.
- [ ] Migration steps (database, config, infrastructure) documented and tested.
- [ ] Rollback plan documented and reviewed by Release Manager and PM.
- [ ] Stakeholders notified of planned release window.
- [ ] QA Lead has provided testing go/no-go signal.

---

## Deployment

### Staging
- [ ] Deployment window scheduled and confirmed with all required parties.
- [ ] Backup or snapshot taken if required (database, config, state).
- [ ] Deploy to staging environment.
- [ ] Run smoke tests on staging; confirm all critical user flows pass.
- [ ] Run regression tests on staging if major release.

### Production
- [ ] Go/No-Go decision made by Release Manager (with PM and QA Lead consulted).
- [ ] Support/On-call Lead notified and standing by.
- [ ] Deploy to production environment.
- [ ] Verify deployment completed without errors.

---

## Post-Deploy Verification

- [ ] Run smoke tests on production; confirm key user flows are operational.
- [ ] Check monitoring dashboards for errors, latency, and resource metrics.
- [ ] Confirm key business metrics are within expected range.
- [ ] Notify stakeholders that the release is live.
- [ ] Monitor production for at least 1 hour (minor) or 4 hours (major) after release.
- [ ] Capture post-release notes (issues observed, lessons learned, follow-up items).

---

## Rollback

| Step | Action | Owner |
|------|--------|-------|
| 1 | Identify rollback trigger (error rate, failed smoke test, critical incident) | Support/On-call Lead |
| 2 | Notify Release Manager and PM immediately | Support/On-call Lead |
| 3 | Make rollback decision (Go/No-Go) | Release Manager + PM |
| 4 | Execute rollback (revert deployment, restore snapshot if needed) | Developer + Release Manager |
| 5 | Verify rollback success with smoke tests | QA Lead / Support Lead |
| 6 | Notify stakeholders of rollback and status | PM / Release Manager |
| 7 | Document incident and schedule post-mortem | PM |

---

## Communication Checklist

- [ ] Pre-release: stakeholders notified of planned release window (at least 24 hours in advance for major releases).
- [ ] At release: brief release announcement sent to relevant channels.
- [ ] Post-release: confirmation of successful deployment (or rollback notice if applicable).
- [ ] Follow-up: post-release notes or summary shared within 24 hours of a major release.

# 05 – Weekly Status Report

**Project:** Modern Endpoint Management – On-Prem to Intune Migration
**Organisation:** Harbourside Building Society (fictional)
**Report:** Week 14 of 36 | **Prepared by:** Gladwyn Dennis, Project Manager
**Distribution:** Project Board, Sponsor (CIO)

---

## Overall status: 🟠 AMBER

Pilot started on schedule this week and early results are good. Overall status is **Amber** because of two issues that threaten Wave 2 and Wave 1 readiness respectively: the mortgage application compatibility problem (I-01) and the app owner testing backlog (I-02). Both have recovery plans in place and neither currently affects the end date.

| Area | Status | Trend | Comment |
|---|---|---|---|
| Schedule | 🟠 Amber | ↔ | Pilot on time; Wave 1 at risk from app sign-off backlog |
| Budget | 🟢 Green | ↔ | £231k spent of £640k (36%) at 39% through timeline |
| Scope | 🟢 Green | ↔ | No change requests this period |
| Risks & Issues | 🟠 Amber | ↓ | I-01 escalated; I-03 resolved |
| Resources | 🟢 Green | ↔ | Partner packagers fully on-boarded |
| Stakeholders | 🟢 Green | ↑ | Positive pilot feedback; Risk & Compliance sign-off received (A-03) |

## Completed this week

- ✅ **Pilot launched** – 72 of 120 pilot devices migrated (IT department complete, volunteers in progress)
- ✅ Gate 2 (Ready for Pilot) approved by Steering Committee
- ✅ Autopilot hardware hash issue fixed with reseller (I-03 closed)
- ✅ Service desk trained; 18 knowledge articles published
- ✅ 96 of 140 apps packaged and tested (69%)

## Planned for next week

- Complete remaining 48 pilot devices, including 3 pilot branches
- Pilot feedback survey and first defect triage review
- Cloud Kerberos trust test for mortgage application (I-01)
- App owner testing sessions – 12 of the 23 outstanding apps booked
- Raise Wave 1 change with CAB

## Pilot metrics (so far)

| Measure | Target | Actual |
|---|---|---|
| Devices enrolled and compliant first time | ≥ 95% | 94% (68 / 72) – 4 failures were I-03, now fixed |
| Average provisioning time (user-driven Autopilot) | ≤ 60 min | 47 min |
| Engineer time per device | ≤ 30 min | 22 min |
| P1/P2 incidents | 0 | 0 |
| Pilot users satisfied or very satisfied | ≥ 80% | 86% (early responses, n = 29) |

## Key issues and escalations

### 🔴 I-01 – Mortgage origination app fails on Entra-joined devices
**Problem:** The app authenticates to an on-prem file share using Kerberos, which fails on Entra-joined devices without extra configuration. 85 users in the Mortgage team depend on it daily.
**Action:** Technical Lead is configuring Windows Hello for Business cloud Kerberos trust, to be tested next week. Vendor asked to confirm support (D-05, chased twice).
**Decision required (Steering Committee):** If not resolved by **week 19**, agree to **move the Mortgage team from Wave 2 to Wave 5**. This protects the end date but leaves those devices on co-management for an extra ~9 weeks. Fallback if still unresolved: Windows 365 Cloud PC for the app.
**Impact on end date:** None if the decision is taken by week 19.

### 🟠 I-02 – App owner testing backlog
**Problem:** 23 apps are awaiting app owner testing and sign-off, against a 5-day agreed turnaround.
**Action:** Escalated to Steering Committee; Sponsor has written to department heads. Testing sessions booked directly in owners' calendars. Any app not signed off by T-3 days moves the affected users to a later wave rather than delaying the whole wave.

## Top risks

| ID | Risk | Score | Movement |
|---|---|---|---|
| R-01 | Legacy apps fail on Entra-joined devices | 🔴 20 | ↔ (now partly realised as I-01) |
| R-02 | Branch bandwidth | 🔴 16 | ↔ – pre-provisioning approach tested successfully in pilot branch prep |
| R-03 | Users lose local files | 🔴 15 | ↓ – OneDrive Known Folder Move at 91% for Wave 1 users |

Full detail in the [RAID Log](03-raid-log.md).

## Budget

| | Budget | Spent to date | Forecast at completion |
|---|---|---|---|
| Core costs | £582,000 | £231,000 | £579,000 |
| Contingency | £58,000 | £0 | £12,000 (possible Cloud PC fallback for I-01) |
| **Total** | **£640,000** | **£231,000** | **£591,000** |

## Decisions needed

1. **Steering Committee:** Approve contingency plan to move the Mortgage team to Wave 5 if I-01 isn't resolved by week 19.
2. **Sponsor:** Continue support for app owner testing deadlines (I-02).

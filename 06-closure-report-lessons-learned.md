# 06 – Closure Report & Lessons Learned

**Project:** Modern Endpoint Management – On-Prem to Intune Migration
**Organisation:** Harbourside Building Society (fictional)
**Prepared by:** Gladwyn Dennis, Project Manager | **Gate 5 – Project Closure**

---

## 1. Summary

The project migrated **2,284 Windows devices** from on-premises management (SCCM, Group Policy, WSUS) to **Intune, Entra ID and Windows Autopilot** in 36 weeks, **on schedule and under budget**. SCCM, WSUS and nine supporting servers have been decommissioned, and the platform has been handed to IT Operations.

The one significant delay – the Mortgage team, moved from Wave 2 to Wave 5 while a Kerberos authentication issue was fixed – was absorbed within the plan without affecting the end date.

## 2. Objectives – results

| # | Objective | Target | Result | Met? |
|---|---|---|---|---|
| O1 | Devices on cloud-native management | 100% in scope | 100% (2,284 devices); 16 devices retired at end of life rather than migrated | ✅ |
| O2 | Patch compliance within 14 days | ≥ 95% | 97.3% (Autopatch, month after closure) | ✅ |
| O3 | Engineer time per new device | ≤ 30 min | 18 min average | ✅ |
| O4 | On-prem endpoint management servers | 9 → 0 | 0 | ✅ |
| O5 | Users losing > 2 hours' productivity | < 2% | 1.4% (32 users) | ✅ |
| O6 | Service desk tickets during waves | ≤ +15%, back to baseline in 2 weeks | Peak +21% (Wave 3); average +12%; back to baseline in 9 days on average | ⚠️ Partly |

## 3. Budget and schedule

| | Planned | Actual |
|---|---|---|
| Duration | 36 weeks | 36 weeks |
| Budget (incl. contingency) | £640,000 | £603,500 |
| Contingency used | £58,000 available | £21,500 (Cloud PC licences for one legacy app; extra floor-walkers for Wave 3) |

## 4. Benefits realised and tracking

| Benefit | Measure | Owner | Review |
|---|---|---|---|
| Infrastructure savings | ~£115k/year (servers, maintenance, hardware refresh avoided) | Head of IT Ops | 6 and 12 months |
| Faster provisioning | New starters' laptops shipped direct from reseller, ready to use | Service Desk Manager | Quarterly |
| Security posture | Audit finding on patch compliance closed by Internal Audit | Head of InfoSec | Closed |
| Operational resilience | Devices manageable without VPN or corporate network | Head of IT Ops | 12 months |

## 5. Handover to BAU

| Item | Recipient | Status |
|---|---|---|
| Intune configuration and design documentation | EUC Operations | ✅ Accepted |
| Autopilot and app packaging runbooks | EUC Operations | ✅ Accepted |
| Autopatch ring and release process | EUC Operations | ✅ Accepted |
| 42 knowledge articles and service desk training | Service Desk | ✅ Accepted |
| Open defects (7 × P4) transferred to problem management | Problem Manager | ✅ Accepted |
| Benefits tracking plan | Head of IT Ops | ✅ Accepted |

## 6. Lessons learned

### What went well – keep doing
1. **Co-management first.** Moving updates and compliance to Intune before resetting any devices meant no device was ever unmanaged or unpatched during the project.
2. **Pre-provisioning for branches.** Building branch devices at head office and swapping them on site cut branch downtime to under 30 minutes per user and avoided the bandwidth problem entirely.
3. **Go/no-go discipline.** Clear, written criteria made wave decisions fast and objective. Wave 4 was held for three days when a printer driver failed testing – a small delay that avoided a branch-wide outage.
4. **Moving people, not the whole wave.** When an app wasn't ready, we moved the affected users to a later wave rather than delaying everyone. This kept the schedule intact.
5. **Site champions.** Branch staff trusted a colleague more than an email. Branches with an active champion logged 30% fewer tickets.

### What didn't go so well – do differently
1. **App discovery started too late.** The Kerberos dependency in the mortgage app (I-01) could have been found in Discovery. *Next time:* test the top 20 business-critical apps on an Entra-joined device in the first four weeks.
2. **App owner availability was assumed, not agreed.** The testing backlog (I-02) came from owners not having time set aside. *Next time:* get department heads to commit named testers and dates at Gate 1.
3. **Contact centre shift patterns.** Wave 3 tickets peaked at +21% because night-shift staff missed the daytime floor-walkers. *Next time:* match support cover to shift patterns, not office hours.
4. **OneDrive readiness reporting was manual early on.** *Next time:* automate the un-synced device report from day one of each wave's countdown.

### Recommendations for future EUC projects
- Treat **app compatibility as the critical path**, not a parallel workstream.
- Build the **business calendar** (month-end, rate changes, regulatory deadlines) into the plan at initiation.
- Agree **audit evidence requirements** with Risk & Compliance before design is finalised, not after.
- Plan comms around **what users must do**, not what IT is doing.

## 7. Closure approval

| Name | Role | Decision |
|---|---|---|
| (CIO) | Sponsor | Approved – project closed |
| (Head of IT Operations) | BAU owner | Handover accepted |
| (Head of Information Security) | Security | Approved |
| (Risk & Compliance lead) | Risk | Approved |

# 03 – RAID Log

**Project:** Modern Endpoint Management – On-Prem to Intune Migration
**Organisation:** Harbourside Building Society (fictional)
**Snapshot:** Week 14 (start of pilot) | Reviewed weekly at Project Board
**Also available as:** [raid-log.csv](raid-log.csv)

Scoring: Probability (P) and Impact (I) each 1–5. Score = P × I. **15+ = Red, 8–14 = Amber, 1–7 = Green.**

---

## Risks

| ID | Risk | P | I | Score | Mitigation | Owner | Status |
|---|---|---|---|---|---|---|---|
| R-01 | Legacy line-of-business apps (incl. mortgage origination system) fail to package or run on Entra-joined devices | 4 | 5 | 🔴 20 | Early app discovery; packaging sprints starting week 7; vendor engagement for top 10 apps; Windows 365 Cloud PC fallback for any app that cannot be remediated | Packaging Lead | Open |
| R-02 | Branch bandwidth (some sites on 20 Mbps) can't support same-day re-provisioning of a whole branch | 4 | 4 | 🔴 16 | Pre-provision devices at head office (Autopilot pre-provisioning); Delivery Optimisation and Microsoft Connected Cache; stagger branch migrations | Technical Lead | Open |
| R-03 | Users lose locally saved files when devices are reset | 3 | 5 | 🔴 15 | OneDrive Known Folder Move enforced 4 weeks before each wave; compliance report on un-synced devices; T-1 reminder; managers confirm completion | Change Manager | Open |
| R-04 | Printer and scanner drivers don't deploy correctly (branch printers used for customer documents) | 4 | 3 | 🟠 12 | Move to Universal Print for head office; tested Win32 driver packages for branch MFDs; printer test in every pilot branch | Technical Lead | Open |
| R-05 | GPO settings missed during rationalisation, creating a security gap | 2 | 5 | 🟠 10 | Group Policy Analytics report; settings mapped line by line; Information Security sign-off of each baseline; Defender vulnerability report post-wave | Technical Lead | Open |
| R-06 | Service desk overwhelmed during waves | 3 | 3 | 🟠 9 | Floor-walkers on site; dedicated hypercare queue; knowledge articles ready before pilot; wave sizes capped | Service Desk Manager | Open |
| R-07 | Key engineers pulled onto BAU incidents | 3 | 3 | 🟠 9 | Backfill budgeted; ring-fenced time agreed with Head of IT Ops | PM | Open |
| R-08 | Wave clashes with business-critical events (month-end, savings rate change) | 2 | 4 | 🟠 8 | Business calendar built into plan; checked at every go/no-go | PM | Open |
| R-09 | Low user adoption / resistance to change at branches | 2 | 3 | 🟢 6 | Site champions; branch manager briefings; "what's changing for you" guides | Change Manager | Open |

## Assumptions

| ID | Assumption | Validated by | Status |
|---|---|---|---|
| A-01 | All in-scope users hold Microsoft 365 E5 (or E3 + EMS E5) licences | Licensing review, week 4 | ✅ Validated |
| A-02 | ~85% of devices meet Windows 11 hardware requirements; the rest are replaced through normal refresh | Hardware readiness report, week 5 | ✅ Validated (87%) |
| A-03 | Risk & Compliance will accept Intune audit logs and compliance reports as evidence in place of SCCM reports | Risk & Compliance sign-off (condition of Gate 0) | ✅ Validated week 9 |
| A-04 | App owners are available to test and sign off apps within 5 working days | App owner agreement | ⚠️ Partially – see I-02 |
| A-05 | Devices can be reset without needing to keep local user profiles | User persona analysis | ✅ Validated (OneDrive in place) |

## Issues

| ID | Issue | Impact | Action | Owner | Raised | Status |
|---|---|---|---|---|---|---|
| I-01 | Mortgage origination app fails on Entra-joined devices – it relies on Kerberos authentication to an on-prem file share | Blocks Mortgage team (85 users) from migrating | Configure Windows Hello for Business cloud Kerberos trust; vendor test; Mortgage team moved from Wave 2 to Wave 5 if not fixed by week 19 | Technical Lead | Wk 12 | 🔴 Open – see [Status Report](05-status-report-week-14.md) |
| I-02 | App owner sign-off backlog: 23 apps awaiting testing | Risks Wave 1 readiness | Escalated to Steering Committee; testing slots booked in owners' calendars; sign-off deadlines added to go/no-go | PM | Wk 13 | 🟠 Open |
| I-03 | 4 pilot devices failed Autopilot enrolment (hardware hash not uploaded by reseller) | Minor delay to pilot | Reseller process corrected; hashes now uploaded at purchase; manual upload for existing stock | Intune Engineer | Wk 14 | 🟢 Resolved |

## Dependencies

| ID | Dependency | On | Needed by | Status |
|---|---|---|---|---|
| D-01 | Branch network upgrades (North branches to 100 Mbps) | Network team | Week 25 | 🟠 On track, tight |
| D-02 | Entra Connect / cloud sync health and hybrid identity cleanup | Identity team | Week 8 | ✅ Complete |
| D-03 | Defender for Endpoint onboarding of all devices | Security Operations | Week 13 | ✅ Complete |
| D-04 | Reseller registers new device hashes into Autopilot at purchase | Procurement / Reseller | Week 14 | ✅ Complete |
| D-05 | Mortgage app vendor confirms support for cloud Kerberos trust | Vendor | Week 17 | 🔴 Awaiting response |

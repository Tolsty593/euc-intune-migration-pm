# 01 – Project Charter

**Project:** Modern Endpoint Management (MEM) – On-Prem to Intune Migration
**Organisation:** Harbourside Building Society (fictional)
**Project Manager:** Gladwyn Dennis
**Sponsor:** Chief Information Officer
**Version:** 1.0 – Approved at Stage Gate 0

---

## 1. Background

Harbourside manages ~2,300 Windows devices using on-premises tools: devices are domain joined, built from images with Configuration Manager (SCCM), configured through ~180 Group Policy Objects and patched through WSUS.

This model is struggling:

- **Remote and hybrid working** – devices off the corporate network for weeks miss patches and policy updates; VPN is needed for basic management
- **Slow device provisioning** – a new laptop takes ~3.5 hours of engineer time to image and set up, and is shipped from head office
- **Infrastructure cost and risk** – 9 on-prem servers support SCCM, WSUS and distribution points, three due for hardware refresh within 12 months
- **Security posture** – patch compliance averages 78% within 30 days; the Risk Committee has flagged this as an audit finding

## 2. Objectives

| # | Objective | Measure | Target |
|---|---|---|---|
| O1 | Move all in-scope Windows devices to cloud-native management | % devices Entra joined and Intune managed | 100% of in-scope devices |
| O2 | Improve patch compliance | Devices on supported, patched build within 14 days of release | ≥ 95% |
| O3 | Speed up device provisioning | Engineer time per new device | ≤ 30 minutes (from 3.5 hours) |
| O4 | Reduce infrastructure | On-prem endpoint management servers | 9 → 0 |
| O5 | Minimise user disruption | Users losing > 2 hours' productivity during migration | < 2% |
| O6 | Maintain service quality | Service desk tickets during waves vs baseline | No more than +15% per wave, back to baseline within 2 weeks |

## 3. Scope

### In scope
- ~2,300 Windows 10/11 laptops and desktops (head office, branches, contact centre)
- Entra ID join and Windows Autopilot enrolment
- Migration of GPOs to Intune configuration profiles (rationalised, not lifted-and-shifted)
- Packaging and deployment of ~140 business applications via Intune (Win32, MSIX, Microsoft Store)
- Windows Autopatch for quality and feature updates
- Compliance policies and Conditional Access, integrated with Defender for Endpoint
- Service desk process updates, knowledge articles and training
- Decommission of SCCM, WSUS and associated servers

### Out of scope
- Mobile phones (already in Intune – separate team)
- Servers and VDI (separate infrastructure roadmap)
- Microsoft 365 tenant changes beyond those required for device management
- Hardware refresh (devices reaching end of life during the project are replaced through the normal refresh budget, but enrolled via Autopilot)

## 4. Approach summary

1. **Foundations** – tenant readiness, identity, network, licensing and security baselines
2. **Co-management** – connect SCCM to Intune and move workloads across gradually, so devices stay managed throughout
3. **Pilot** – IT team and 50 volunteers across every department and site type
4. **Waves 1–5** – devices reset and re-provisioned via Autopilot, site by site
5. **Decommission and handover** – switch off SCCM/WSUS, close the project, hand over to BAU

Full detail in the [Delivery Plan](02-delivery-plan.md).

## 5. Budget

| Item | Cost |
|---|---|
| Internal resource backfill (packaging, engineering) | £210,000 |
| Microsoft partner – design assurance and app packaging support | £165,000 |
| Floor-walkers and wave-day deskside support | £78,000 |
| Licensing uplift (Intune Suite add-ons, Autopatch prerequisites) | £72,000 |
| Training, comms and change materials | £24,000 |
| Testing tools and pilot hardware | £33,000 |
| **Subtotal** | **£582,000** |
| Contingency (10%) | £58,000 |
| **Total** | **£640,000** |

Expected savings: ~£115,000 per year from server retirement, reduced engineer build time and lower support volumes. Payback ~5.5 years on cost alone, with the main benefit being reduced security and audit risk.

## 6. Governance

| Forum | Members | Frequency | Purpose |
|---|---|---|---|
| Steering Committee | CIO (Sponsor), COO, Head of IT Operations, Head of Information Security, Risk & Compliance lead, PM | Monthly + stage gates | Decisions, funding, escalations, go/no-go |
| Project Board | PM, Technical Lead, Service Desk Manager, Change Manager, Partner Lead | Weekly | Progress, RAID, resourcing |
| Change Advisory Board | IT change process | Per wave | Change approval for each deployment wave |
| Daily stand-up | Project team | Daily during waves | Wave readiness and issue triage |

**Tolerances delegated to PM:** schedule ± 2 weeks, budget ± 5%. Anything beyond is escalated to the Steering Committee.

## 7. Key roles

| Role | Responsibility |
|---|---|
| Sponsor (CIO) | Owns the business case, chairs Steering Committee |
| Project Manager | Planning, delivery, RAID, reporting, stakeholder management, budget |
| Technical Lead (EUC Architect) | Design authority for Intune, Autopilot, policy and security configuration |
| App Packaging Lead | Application discovery, packaging, testing, owner sign-off |
| Service Desk Manager | Support readiness, knowledge articles, ticket monitoring |
| Change Manager | Comms, training, business readiness |
| Site Champions (1 per branch) | Local point of contact, wave-day support for colleagues |

## 8. Approval

| Name | Role | Decision | Date |
|---|---|---|---|
| (CIO) | Sponsor | Approved | Gate 0 |
| (Head of Information Security) | Security sign-off | Approved | Gate 0 |
| (Risk & Compliance lead) | Risk sign-off | Approved with conditions – see RAID A-03 | Gate 0 |

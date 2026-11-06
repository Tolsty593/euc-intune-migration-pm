# On-Prem to Intune Migration – EUC Project Management Case Study

**Gladwyn Dennis** | EUC Project Manager | Service Delivery | Modern Endpoint Management

This repository is a worked case study showing how I would plan, run and close an End User Computing (EUC) migration from on-premises device management (Active Directory, Configuration Manager, Group Policy, WSUS) to cloud-native management with Microsoft Intune, Entra ID and Windows Autopilot.

> **Note:** *Harbourside Building Society* is a fictional organisation created for this case study. The scenario, figures and outcomes are illustrative. They draw on my hands-on experience supporting end users in banking and education, and deploying devices with Windows Autopilot in financial services environments.

---

## The scenario at a glance

| | |
|---|---|
| **Organisation** | Harbourside Building Society (fictional) – regulated UK financial services |
| **Users / devices** | ~2,000 users, ~2,300 Windows laptops and desktops, 1 head office, 14 branches, contact centre |
| **Starting point** | On-prem AD domain join, ConfigMgr (SCCM), ~180 GPOs, WSUS patching, imaging via task sequences |
| **Target state** | Entra ID join, Intune policy and app delivery, Windows Autopilot, Windows Autopatch, Defender for Endpoint, Conditional Access |
| **Duration** | 36 weeks (pilot + 5 deployment waves) |
| **Budget** | £640,000 (including 10% contingency) |
| **Approach** | Co-management first, then device reset to Autopilot in waves, then ConfigMgr decommission |

## Project artefacts

| # | Document | What it shows |
|---|---|---|
| 01 | [Project Charter](01-project-charter.md) | Business case, scope, objectives, success measures, budget, governance |
| 02 | [Delivery Plan](02-delivery-plan.md) | Phases, milestones, wave schedule, Gantt timeline, go/no-go criteria |
| 03 | [RAID Log](03-raid-log.md) ([CSV](raid-log.csv)) | Risks, assumptions, issues and dependencies with owners and mitigations |
| 04 | [Stakeholder & Comms Plan](04-stakeholder-comms-plan.md) | Stakeholder map, RACI, comms schedule, sample user announcements |
| 05 | [Weekly Status Report](05-status-report-week-14.md) | RAG-rated status report mid-project, with a live issue being managed |
| 06 | [Closure Report & Lessons Learned](06-closure-report-lessons-learned.md) | Benefits realised, handover to BAU, lessons for future projects |

## What this demonstrates

- **Technical delivery** – sequencing a migration so that users are never left unmanaged or unpatched, and the old platform is only switched off once the new one is proven
- **Risk management** – anticipating the things that actually derail EUC projects: legacy apps, branch bandwidth, printers, and user disruption
- **Stakeholder management** – keeping the Board, Risk & Compliance, branch managers and frontline staff informed in language that suits each audience
- **Regulated environments** – change control, audit evidence and operational resilience expectations in UK financial services
- **Service transition** – handing a new platform to the service desk and operations teams with documentation, training and support in place

## Methodology

Hybrid delivery: a **stage-gated (PRINCE2-style)** structure for governance, funding and go/no-go decisions, with **agile sprints** inside the build and wave phases for policy, app packaging and issue resolution.

## Contact

Email: gden@sky.com

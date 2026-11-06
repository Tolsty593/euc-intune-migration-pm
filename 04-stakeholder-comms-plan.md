# 04 – Stakeholder & Communications Plan

**Project:** Modern Endpoint Management – On-Prem to Intune Migration
**Organisation:** Harbourside Building Society (fictional)

---

## 1. Stakeholder map

| Stakeholder | Interest | Influence | Approach | What they care about |
|---|---|---|---|---|
| CIO (Sponsor) | High | High | **Manage closely** | Delivery on time and budget, audit finding closed |
| COO | Medium | High | **Keep satisfied** | No disruption to branches or contact centre |
| Head of Information Security | High | High | **Manage closely** | No security gaps; Conditional Access and compliance working |
| Risk & Compliance | High | High | **Manage closely** | Audit evidence, change control, operational resilience |
| Head of IT Operations | High | Medium | **Manage closely** | Team capacity, a clean BAU handover |
| Service Desk | High | Medium | **Keep informed, involve** | Ticket volumes, knowledge articles, training |
| Branch & Contact Centre Managers | High | Medium | **Keep informed, involve** | Customer service not affected; staff know what to expect |
| App owners | Medium | Medium | **Involve** | Their app still works; testing time is reasonable |
| Frontline staff | High | Low | **Keep informed** | "Will my laptop work on Monday? Will I lose my files?" |
| Microsoft partner | Medium | Medium | **Involve** | Clear scope, timely decisions |
| Trade union reps | Low | Medium | **Keep informed** | Any change to working patterns or monitoring |

## 2. RACI

R = Responsible, A = Accountable, C = Consulted, I = Informed

| Activity | Sponsor | PM | Tech Lead | InfoSec | Risk & Compl. | Service Desk | Change Mgr | App Owners |
|---|---|---|---|---|---|---|---|---|
| Business case & charter | A | R | C | C | C | I | I | I |
| Solution design | I | C | A/R | C | C | C | I | C |
| Security baselines | I | I | R | A | C | I | I | I |
| App packaging & testing | I | C | C | I | I | I | I | A/R |
| Wave go/no-go | I | A/R | C | C | C | C | C | C |
| User comms & training | I | A | C | I | I | C | R | I |
| Hypercare support | I | C | C | I | I | A/R | C | I |
| SCCM/WSUS decommission | A | R | R | C | C | I | I | I |
| Project closure | A | R | C | I | C | C | C | I |

## 3. Communications schedule

| Comm | Audience | Channel | Frequency / timing | Owner |
|---|---|---|---|---|
| Steering Committee report | SteerCo | Meeting + written report | Monthly and at each stage gate | PM |
| Weekly status report | Project Board, Sponsor | Email / SharePoint | Weekly (see [example](05-status-report-week-14.md)) | PM |
| Project launch announcement | All staff | Intranet + CEO/CIO email | Once, week 4 | Change Manager |
| Manager briefing pack | Line managers in the wave | Teams call + slides | T-10 days per wave | Change Manager |
| "Your laptop is being upgraded" email | Users in the wave | Email | T-7 days | Change Manager |
| Reminder: save your files | Users in the wave | Email + Teams message | T-1 day | Change Manager |
| Wave-day help | Users in the wave | Floor-walkers, Teams hypercare channel | T-0 | Service Desk |
| "How did it go?" survey | Users in the wave | Microsoft Forms | T+5 days | Change Manager |
| Service desk briefing | Service desk | Huddle + knowledge articles | Before pilot and each wave | Service Desk Manager |
| Branch champion huddle | Site champions | Teams | Fortnightly during waves | Change Manager |

## 4. Sample user announcement (T-7 days)

> **Subject: Your laptop is getting an upgrade on Tuesday 14 July**
>
> Hello,
>
> As part of our move to a more secure, more modern way of managing our computers, your laptop will be upgraded on **Tuesday 14 July**.
>
> **What's changing?**
> Your laptop will be refreshed and set up again automatically. You'll sign in with your usual email address and password, and your apps will install themselves. It takes around 45 minutes.
>
> **What you need to do before Monday 13 July**
> 1. Check your files are in **OneDrive** (look for the green tick on your Desktop and Documents folders). Anything saved elsewhere on your laptop will be removed.
> 2. Make a note of any apps you use that aren't on our standard list, and let your manager know.
> 3. Make sure you know your password and have the **Microsoft Authenticator** app on your phone.
>
> **On the day**
> Our support team will be in the branch from 8am. If anything doesn't look right, ask them or post in the **Laptop Upgrade Help** Teams channel.
>
> **Why are we doing this?**
> It means your laptop gets security updates faster, works the same at home as in the office, and replacement laptops can be sent straight to you, ready to use.
>
> Thank you,
> IT Change Team

## 5. Sample manager briefing – key messages

- **What:** Every laptop in your team will be refreshed on [date]. Allow about an hour per person; we'll stagger it so the branch stays open.
- **Why:** Faster security updates and closes an audit finding – it protects our customers' data.
- **What you need to do:** Make sure your team has moved files to OneDrive by [T-1]. Tell us now about any special apps or equipment.
- **Support:** Floor-walkers on site all day, plus a dedicated help channel for two weeks afterwards.
- **Escalation:** Contact the project team directly if anything stops you serving customers.

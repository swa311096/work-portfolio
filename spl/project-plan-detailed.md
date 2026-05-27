---
title: Project Plan Detailed
parent: SPL
nav_order: 13
permalink: /spl/project-plan-detailed/
---

# Project Plan Detailed

Detailed project plan for a Microsoft enterprise support workflow evaluation pilot.

## Project Outline

| Section | Detail |
|---|---|
| Client | Microsoft |
| Project | Enterprise Support Workflow Evaluation Pilot |
| Duration | 12 weeks |
| Primary Goal | Deliver high-quality human data to improve agentic AI performance in enterprise support workflows |
| Deliverable | Support Resolution Evaluation Set |
| Data Type | Prompt-rubric evaluation records |
| Target Volume | 2,000 accepted evaluation records |
| Core Workflow | Automated ticket resolution |
| Future Expansion | Ideal responses, preference data, multi-turn tool-use trajectories |
| Pricing Model | Tiered expert-hour model + flat Mercor fee on expert hourly pay |
| Delivery Model | Secure annotation environment, 100% expert review, ingestion-ready final records |

## Domain Selection

| Domain | What the agent does | Best example task | Why attractive | Main challenge |
|---|---|---|---|---|
| Enterprise support | Helps customers resolve product/account/issues | Customer cannot configure Copilot admin settings. Diagnose issue and draft response. | High-volume, measurable, fast to ramp | Needs product docs + support policies |
| IT support | Helps employees resolve internal tech issues | Employee cannot access SharePoint. Diagnose likely cause and next steps. | Measurable, close to support, good AI use case | Needs internal systems/policies |
| Recruiting / talent ops | Screens, routes, matches, communicates with candidates | Evaluate candidate fit for role using resume + rubric. | Mercor has strong credibility here | Less directly tied to Microsoft model training value |
| Software engineering | Writes, reviews, debugs, or explains code | Find bug in PR and suggest fix. | Very relevant to Microsoft/GitHub/Copilot | Harder, needs strong experts, more expensive |
| Cloud operations | Troubleshoots Azure infra, logs, incidents, configs | Diagnose why service latency increased after config change. | Very relevant to Azure, high value | Needs realistic infra context; more complex |
| Security / compliance | Identifies security risks or policy violations | Classify alert severity and recommend containment. | High value, high-risk domain | Requires senior experts, hard QA, sensitive data |
| Sales / customer success | Helps reps handle enterprise accounts and renewals | Summarize account risk and recommend next action. | Direct revenue impact | More subjective, needs CRM/account context |
| Finance / business ops | Helps with planning, forecasting, reporting, analysis | Explain variance between forecast and actuals. | Structured, measurable in parts | Less uniquely Microsoft; needs internal financial data |
| Legal / policy | Reviews contracts, policies, regulatory questions | Identify risky clauses in enterprise agreement. | High value | Very sensitive, expensive experts, slow ramp |

## Domain Recommendation Matrix

| Domain | Microsoft relevance | Feasibility | Microsoft input dependency | Measurability | Mercor credibility | Verdict |
|---|---|---|---|---|---|---|
| Customer / enterprise support | High | High | Medium | High | High | Strong |
| Recruiting / talent workflows | Medium | High | Low-Medium | Medium | Very high | Strong backup |
| IT support | High | Medium-High | Medium | High | High | Strong but more access-dependent |
| Software engineering / cloud ops | Very high | Medium | High | High | Medium | Better as phase 2 |
| Sales / customer success | High | Medium | High | Medium | Medium | Later |
| Finance / business ops | Medium | Medium | Medium | Medium | Low-Medium | Later |
| Legal / compliance | Medium-High | Low-Medium | High | Low-Medium | Low | Later |

## Task Distribution Across Workflows

| Workflow | Records | Why |
|---|---:|---|
| Microsoft 365 admin / configuration support | 500 | Common enterprise admin workflow |
| Azure setup / troubleshooting support | 500 | High-value technical support area |
| Teams / Copilot configuration support | 400 | Relevant to agentic enterprise AI adoption |
| Billing / subscription / account access | 300 | High-volume support category |
| Escalation / policy-boundary cases | 300 | Tests safety and handoff judgment |
| Total | 2,000 |  |

## Task Claiming Rules

- Experts can claim one task at a time.
- Experts cannot claim a new task until the current task is submitted.
- Tasks have a claim expiration window.
- Task complexity is gated by expert tier.
- Reviewers cannot review their own created tasks.
- Repeated rework lowers future task access.
- High-quality experts can unlock higher-complexity tasks.

## Expert Sourcing And Ramp-Up Plan

### Hours Per Accepted Record

| Workstream | Hours per accepted record |
|---|---:|
| Scenario research + prompt creation | 2.0-3.0 |
| Rubric creation | 2.0-2.5 |
| Expert review | 1.5-2.0 |
| QA / arbitration / rework buffer | 1.0-1.5 |
| Total | 6.5-9.0 |

### Core Assumptions

| Assumption | Value |
|---|---|
| Accepted records target | 2,000 |
| Estimated hours / accepted record | 8-9 |
| Total expert hours required | 16,000-18,000 |
| Project duration | 12 weeks |
| Effective production window | 8-10 weeks |
| Expert bench required | 80-100 |
| Active creator/reviewer mix | Creators + reviewers |

### Sourcing Channels

| Source channel | Target expert type | Why this channel |
|---|---|---|
| LinkedIn outbound | Enterprise support engineers, support QA leads, escalation managers | Fastest way to target role-specific professionals |
| Email outbound | Certified professionals, support consultants, MSP operators | Useful for direct sourcing outside LinkedIn |
| Certification communities | Microsoft 365, Azure, security, IT admin professionals | Signals domain knowledge and product familiarity |
| Enterprise IT / MSP networks | IT admins, managed service provider support leads | Strong practical support experience across Microsoft products |
| Referrals | Senior support professionals, reviewers, QA leads | Higher trust and faster vetting |

### Ramp Plan

| Phase | Weeks | Expert model | What happens |
|---|---|---|---|
| Phase 1: Setup Production | 1-3 | Tier 1 experts only | Create taxonomy, gold examples, rubrics, failure tags, and guidelines. Produce first records with senior experts and calibrate with Microsoft. |
| Phase 2: Tier 1 + Tier 2 Scaling | 4-8 | Tier 1 reviewers + Tier 2 creators/reviewers | Scale production across approved campaigns. Tier 1 experts review and calibrate Tier 2 work. Refine instructions based on rework patterns. |
| Phase 3: All-Tier Scaling + Final Delivery | 9-12 | Tier 1 reviewers + Tier 2 core experts + Tier 3 junior creators | Add Tier 3 experts to lower-complexity tasks. Keep Tier 1/Tier 2 on review and complex records. Complete rework, final QA, and dataset delivery. |
| Total | 12 | 80-100 expert bench | 2,000 accepted records |

### Expert Tiers

| Tier | Who | Role |
|---|---|---|
| Tier 1 | Senior support QA leads, escalation managers, senior Microsoft ecosystem experts | Define quality bar, create gold examples, review complex tasks, arbitrate |
| Tier 2 | Enterprise support engineers, Azure/M365 specialists, MSP operators | Create and review standard support evaluation records |
| Tier 3 | Certified junior contributors, support analysts, technical grads | Create lower-complexity records under review |

## Task Staging

| Stage | What happens | Output |
|---|---|---|
| 1. Task Create | Creator drafts support prompt, relevant context, rubric, escalation criteria, failure tags, and rationale | Draft evaluation record |
| 2. Review | Reviewer checks factual accuracy, rubric clarity, support judgment, escalation correctness, and formatting | Accepted, rework, or rejected |
| 3. Rework + Sign-off | Creator fixes reviewer comments; reviewer signs off final record | Ingestion-ready record |

## Pricing Model

| Cost component | Basis | Formula |
|---|---|---|
| Expert hourly pay | Hours x hourly rate by tier | Tier hours x expert rate |
| Mercor flat fee | % or fixed platform/project fee | Applied to expert cost |
| Total Microsoft price | Expert pay + Mercor fee | Total |

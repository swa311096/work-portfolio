---
title: Project Health KPIs
parent: SPL
nav_order: 7
permalink: /spl/project-health-kpis/
---

# Project Health KPIs

Across expert-data projects, a strong project-health dashboard should cover four buckets:

- financial health
- workforce capacity
- pipeline flow
- instruction quality

Together, these explain whether the project is profitable, whether expert capacity is being used well, whether work is moving through the system, and whether quality problems are coming from unclear task design.

## 1. Financial KPIs

Goal: maintain project gross margin and reduce rework drag.

| Metric | What it tells you |
|---|---|
| Gross margin % | Whether the project is economically healthy |
| Cost per accepted unit | True cost of producing usable output |
| Revenue per accepted unit | Whether pricing matches complexity |
| Rework cost % | How much margin is being lost to corrections |
| QA + adjudication cost per unit | Whether quality control is becoming too expensive |
| Expert payout per accepted unit | Whether labor costs are in line with pricing |
| Utilization-adjusted margin | Margin after accounting for idle experts, unused QA, and bench time |
| Scope-change cost impact | Cost impact from client-side instruction or requirement changes |

Most important three:

- gross margin %
- cost per accepted unit
- rework cost %

## 2. Workforce KPIs

Goal: use expert capacity efficiently and prevent expert pool blockage.

| Metric | What it tells you |
|---|---|
| Active expert count | How many experts are actually producing work |
| Expert utilization % | Whether experts have enough work and are not idle |
| Cross-utilization rate | % of experts who can work across multiple task types or workstreams |
| Calibration pass rate | Whether new experts are clearing the quality bar |
| Time to productivity | Time from onboarding to first accepted task |
| Claim block rate | % of experts unable to claim tasks due to gating, tooling, permissions, or task availability |
| Expert throughput per day | Output per active expert |
| Expert acceptance rate | % of submitted work accepted after QA |
| Expert churn / inactivity rate | Whether the pool is stable |
| Top-performer dependency | % of output coming from the top 10% of experts; high concentration is risky |

Most important three:

- expert utilization %
- calibration pass rate
- claim block rate

## 3. Pipeline KPIs

Goal: reduce batch congestion and accelerate ingestion and delivery flow.

| Metric | What it tells you |
|---|---|
| Accepted units per day/week | Core production throughput |
| Ingestion time | Time from task availability to task being claimable or workable |
| Cycle time | Time from task creation to accepted delivery |
| Queue aging | How long tasks sit in each stage |
| WIP by stage | Work-in-progress across creation, expert work, QA, adjudication, and client review |
| Bottleneck stage | Which stage is slowing the whole system |
| Long-tail batch % | % of batches stuck beyond SLA |
| QA queue time | Whether QA is becoming the choke point |
| Adjudication backlog | Whether ambiguity or disputes are slowing acceptance |
| On-time delivery forecast | Whether the project is tracking to timeline |

Most important three:

- accepted units/week
- cycle time
- long-tail batch %

## 4. Instruction KPIs

Goal: maximize first-time acceptance rate through clear guidelines.

| Metric | What it tells you |
|---|---|
| First-time acceptance rate (FTAR) | % accepted without rework; strongest instruction-quality metric |
| Instruction-related defect rate | % defects caused by unclear guidelines, not expert ability |
| Clarification volume | Number of expert questions or escalations about instructions |
| Rubric disagreement rate | Whether reviewers interpret instructions differently |
| Adjudication rate | % tasks needing senior review due to ambiguity |
| Common error recurrence rate | Whether the same mistakes keep happening |
| Instruction update frequency | Too many updates may signal unstable scope or unclear initial design |
| Post-update defect reduction | Whether instruction changes actually improve quality |
| Gold task accuracy | Whether experts understand the task standard |
| Client dispute rate | Whether client interpretation differs from Mercor's interpretation |

Most important three:

- FTAR
- instruction-related defect rate
- clarification volume

## Clean Dashboard

If I needed a tight project-health dashboard, I would use 12 metrics:

| Bucket | Core metrics |
|---|---|
| Financial | Gross margin %, cost per accepted unit, rework cost % |
| Workforce | Expert utilization %, calibration pass rate, claim block rate |
| Pipeline | Accepted units/week, cycle time, long-tail batch % |
| Instruction | FTAR, instruction-related defect rate, clarification volume |

This is a strong general-purpose structure because it covers profitability, labor capacity, operational flow, and data quality at the source.

## Interview Framing

I would track project health across four buckets: financial, workforce, pipeline, and instruction quality.

Financial metrics tell me whether the project is profitable after rework. Workforce metrics tell me whether expert capacity is being used efficiently. Pipeline metrics tell me whether work is flowing through the system or getting stuck. Instruction metrics tell me whether quality problems come from unclear guidelines rather than weak experts.

If I had to keep the dashboard tight, I would use 12 metrics: gross margin %, cost per accepted unit, rework cost %, expert utilization %, calibration pass rate, claim block rate, accepted units/week, cycle time, long-tail batch %, FTAR, instruction-related defect rate, and clarification volume.

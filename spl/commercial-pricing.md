---
title: Commercial Pricing
parent: SPL
nav_order: 9
permalink: /spl/commercial-pricing/
---

# Commercial Pricing

This is a recommended commercial structure for a 1-3 month expert-data project, not a claim about Mercor's actual internal pricing.

The goal is to choose a billing model that aligns incentives around usable, accepted data while protecting the project from excessive rework, scope changes, and unclear acceptance standards.

## Billing Model Options

### 1. Per Accepted Unit Of Data

This is the best default for enterprise trust.

Mercor charges a price per accepted item. An item could be:

- a single-turn prompt and label
- a multi-turn conversation
- a tool-trajectory episode
- a coding solution with tests
- a prompt-rubric evaluation record
- a validated adversarial case

The price should include expert work, QA, program management, and a rework allowance up to a defined cap.

Why this works:

- aligns incentives around quality and usable output
- simplifies procurement
- prevents hours inflation
- makes the customer pay for accepted deliverables, not effort alone

Billable-unit examples:

| Data type | Billable unit |
|---|---|
| Coding | Per problem package: prompt, reference solution, hidden tests, and grader |
| Rubric eval | Per conversation graded or per rubric authored |
| Tool trajectories | Per successful episode meeting success criteria |
| Red-team | Per validated adversarial case plus labels; optionally plus gold safe response |

### 2. Time And Materials For Design, Then Per-Unit For Production

Use hourly or a fixed weekly retainer for the design phase, then switch to per accepted unit once the spec stabilizes.

Design-phase work can include:

- rubric design
- taxonomy creation
- gold set development
- calibration
- workflow design
- adjudication rules

Why this works:

The early phase is inherently iterative. It is hard to price per unit before the task standard is clear. Once the rubric, quality bar, and output format are stable, per-unit pricing becomes cleaner.

### 3. Retainer Plus Usage

Use a monthly retainer for program management, QA infrastructure, and tooling, plus variable per-unit fees for accepted data.

This works when the customer wants a standing team and expects follow-on expansions.

Why this works:

- covers fixed program costs
- supports ongoing client communication and QA capacity
- keeps variable pricing tied to output volume
- fits customers with multiple workstreams over time

### 4. Outcome Or Milestone-Based

Use milestone billing when the customer wants procurement simplicity.

Example:

> Deliver 2,000 accepted evaluation records meeting agreed acceptance criteria.

This can work, but the acceptance standard must be tightly defined. Otherwise, Mercor takes on too much ambiguity and rework risk.

## Commercial Terms To Include

A credible commercial proposal should define:

- acceptance criteria: what counts as accepted, such as customer QA pass, rubric agreement, tests passing, or trajectory success
- rework policy: included rework up to a defined threshold, such as 5-10%, then billed separately or reflected in timeline changes
- SLA: weekly delivery cadence and reporting expectations
- change control: material rubric or spec changes adjust price, scope, or timeline
- minimum commit: protects against stop-start demand and covers fixed PM and QA costs

These terms matter because expert-data projects can fail commercially even when the work is good. The risk often comes from unclear acceptance criteria, uncontrolled scope changes, and hidden rework.

## Target Margin

For human-data projects, margin should usually be discussed as gross margin:

> Revenue minus direct expert payouts and direct QA labor.

A reasonable target range:

| Project type | Gross margin target |
|---|---:|
| Standard expert labeling or grading programs | 30-45% |
| Programs with strong tooling automation, deterministic validation, efficient expert supply, or low churn | 45-60% |
| Niche expert programs with expensive specialists, heavy adjudication, or frequent customer scope changes | 20-30% |

Higher margin is easier when tooling reduces QA cost, deterministic validation exists, and the expert bench is efficient. Lower margin may be necessary when the project needs specialist physicians, senior lawyers, heavy adjudication, or repeated customer-side scope changes.

## Rule Of Thumb For Per-Unit Pricing

Price per accepted unit should cover:

- direct expert pay
- QA and adjudication
- PM and client communication
- platform and tooling overhead
- expected rework
- target margin

The simple formula is:

> Price per accepted unit = total cost per accepted unit / (1 - target gross margin)

## Numeric Example

Suppose Mercor delivers 10,000 accepted rubric-scored conversations.

Per-item cost assumptions:

| Cost component | Cost per item |
|---|---:|
| Expert production cost | $1.60 |
| QA + adjudication | $0.70 |
| PM + overhead | $0.30 |
| Expected rework buffer | $0.20 |
| Total cost | $2.80 |

To hit roughly 40% gross margin:

> Price = $2.80 / (1 - 0.40) = $2.80 / 0.60 = $4.67 per accepted item

In practice, I would round to $4.75-$5.00 depending on complexity, risk, and customer requirements.

## Tie-Back: Per-Task Versus Hourly

Use per accepted unit for production labeling, grading, episodes, or problem packages where acceptance is measurable.

Use hourly or retainer pricing for rubric design, taxonomy building, gold set creation, calibration, and adjudication-heavy ambiguity.

## Interview Framing

For a 1-3 month expert-data project, I would usually recommend a hybrid structure: hourly or retainer pricing during the design and calibration phase, then per accepted unit during production.

Per accepted unit is the cleanest enterprise default once acceptance criteria are stable because it aligns incentives around usable output. The customer is not paying for hours; they are paying for accepted data that passes the agreed quality bar.

The pricing should cover expert production, QA, adjudication, PM, tooling overhead, expected rework, and a target gross margin. For standard expert labeling or grading work, I would target roughly 30-45% gross margin. If tooling and deterministic validation reduce QA cost, the target can be higher. If niche experts or heavy adjudication are required, the margin may need to be lower.

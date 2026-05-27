---
title: Data Types By Use Case
parent: SPL
nav_order: 5
permalink: /spl/data-types-by-use-case/
---

# Data Types By Use Case

Different model-improvement goals need different data formats. The right question is not just "do we need more data?" It is:

> What kind of signal does the model need, and how can humans provide that signal reliably?

Some workflows teach the model how to respond. Some measure whether the model is correct. Some create preference signal. Some expose failures. The SPL needs to match the data type to the use case, the domain risk, and the quality bar.

## A. Prompt-Response Pairs

Use prompt-response pairs for SFT or instruction tuning when the goal is to teach the model a behavior from demonstrations.

This is useful when the desired output can be shown directly: tone, format, task execution, escalation behavior, or domain-specific response patterns.

Best for:

- high-volume coverage
- broad behavior learning
- teaching the model how to respond
- standardizing tone, format, and workflow execution

Common industries:

- customer support
- sales enablement
- HR
- IT helpdesk
- consumer apps

Example: give the model a customer-support ticket and an ideal answer that is concise, empathetic, policy-compliant, and formatted correctly.

## B. Pairwise Preference Or Rankings

Use pairwise preference data when the model can generate multiple candidate outputs and humans need to choose which one is better.

This is useful for RLHF-style workflows where quality is comparative rather than purely right or wrong.

Best for:

- improving chat quality
- style alignment
- policy adherence
- summaries
- writing quality
- helpfulness and safety tradeoffs

Example: show a reviewer two model responses and ask which one is more helpful, safer, more accurate, or better aligned with the requested style.

## C. Prompt-Rubric Pairs

Use prompt-rubric pairs for rubric-based grading and eval data when the goal is fine-grained, auditable scoring.

This is useful when correctness can be decomposed into criteria, such as "must include X," "must not say Y," "must cite a source," or "must escalate this case."

Best for:

- stable measurement across model versions
- auditable scoring
- regulated domains
- training signals where the model needs to understand specific quality criteria

Common industries:

- healthcare, for clinical quality
- legal, for issue spotting, citations, and disclaimers
- finance, for compliance and correctness
- safety and trust

Example: score a healthcare answer against a rubric for clinical completeness, unsafe advice, required disclaimers, and whether the answer recommends appropriate escalation.

### When Rubrics Work Best

Rubrics work best when "good answer" can be broken into checkable criteria.

Good rubric domains:

- high-stakes correctness: healthcare, legal, finance, and compliance
- structured tasks: extraction, classification, and summarization with required fields
- policy and safety: explicit do and don't constraints
- answers with verifiable anchors: citations, calculations, steps, required disclaimers, and refusal behavior
- domain reasoning with measurable elements, such as differential diagnosis with required red flags or contract clause analysis with required risks

Rubrics are less ideal for:

- purely subjective creative writing, unless the rubric focuses on format constraints
- tasks where "correct" depends heavily on hidden context the rater cannot access

## D. Test-Case Or Unit-Test-Graded Solutions

Use test-case or unit-test-graded solutions when outputs can be validated deterministically.

This is strongest when there is a clear pass/fail signal, such as whether code runs, tests pass, or a query returns the expected result.

Common industries:

- software engineering
- data engineering
- analytics

Example: ask the model to fix a bug in a repository, then grade the solution against visible and hidden tests.

## E. Tool-Use Trajectories

Use tool-use trajectories when training agents to operate tools correctly.

The data should show not just the final answer, but the sequence of actions, tool calls, observations, state changes, and decisions that led to the result.

Best for:

- correct sequencing
- state handling
- search and retrieval workflows
- CRM or ticketing workflows
- IDE and coding-agent workflows
- spreadsheet and back-office automation

Common industries:

- IT ops
- sales ops
- support ops
- back office automation

Example: show an agent how to inspect a support ticket, search the knowledge base, update the CRM, draft a response, and mark the correct resolution code.

## F. Red-Team Prompts And Labeled Failure Modes

Use red-team or adversarial prompts when the goal is to expose model weaknesses and harden the system.

This data should include the adversarial prompt, the model behavior, the failure label, and ideally the expected safe behavior.

Best for:

- jailbreak detection
- hallucination discovery
- unsafe advice prevention
- policy boundary testing
- high-risk deployment review

Common industries:

- regulated deployments
- healthcare
- legal
- finance
- safety-critical customer support
- any model surface with brand, compliance, or user-harm risk

Example: test whether the model gives unsafe medical advice, fabricates citations, bypasses policy, leaks sensitive information, or follows malicious instructions.

## Interview Framing

I would evaluate data types by asking what kind of model improvement signal we need.

If we want to teach a behavior, I would use prompt-response demonstrations. If we need alignment or style preferences, I would use pairwise rankings. If we need auditable quality measurement, especially in regulated domains, I would use prompt-rubric pairs. If the task has deterministic correctness, like coding, I would use test-case-graded solutions. If the model is acting as an agent, I would collect tool-use trajectories. If the goal is safety or robustness, I would use adversarial prompts with labeled failure modes.

The SPL's job is to match the data format to the model weakness, domain risk, and client goal. More data is not automatically better. The right data type gives the lab the signal it actually needs.

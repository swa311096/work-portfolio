---
title: SPL Skill Stack
parent: SPL
nav_order: 3
permalink: /spl/skill-stack/
---

# SPL Skill Stack

If the SPL job is to turn model weaknesses into high-quality expert-data workflows, then the skill stack is easiest to understand through one example.

Running example:

> A frontier AI lab wants to improve its coding model. The model performs well on simple coding questions, but it fails when asked to debug multi-file backend issues in realistic codebases.

The SPL's job is to turn that model weakness into a data project that experts can execute and the lab can actually use.

The one-line version:

> SPLs turn ambiguous model-improvement goals into reliable expert-data systems that produce high-quality signal at speed.

---

## 1. Problem Framing

The first skill is turning a vague goal into a clear target.

If the lab says, "we want to improve coding performance," that is not specific enough. Coding performance could mean algorithm questions, frontend bugs, backend architecture, SQL optimization, test writing, security, or code explanation.

For this case, a better framing would be:

> Improve the model's ability to debug multi-file backend code, especially when failures involve edge cases, dependency interactions, or production constraints.

That framing is useful because it tells the SPL what the project is really about. The goal is not "better coding" in general. The goal is better debugging in realistic backend systems.

The SPL should clarify:

- What exact capability is the lab trying to improve?
- What does a good model answer look like?
- Is the data for training, evaluation, or both?
- Which failure matters most: wrong fix, shallow explanation, missed edge case, or unsafe architecture?
- What output does the lab need from experts?

Core skill: **structured problem definition.**

## 2. AI Model Improvement Literacy

The SPL does not need to be a researcher, but they need to understand how the data will be used.

In this coding case, the expert workflow could serve different purposes:

- If the lab wants to **test** the model, experts may create difficult backend debugging evals.
- If the lab wants to **teach** the model, experts may write ideal answers and explanations.
- If the lab wants to **rank outputs**, experts may compare two model answers and choose the better one.
- If the lab wants to **understand failures**, experts may label the specific mistake the model made.

These are different workflows. The SPL needs enough AI literacy to know the difference between eval data, supervised fine-tuning data, preference data, rubrics, and human feedback.

Core skill: **knowing how expert judgment becomes model-improvement signal.**

## 3. Failure Diagnosis

"The model is bad at backend debugging" is still too broad. The SPL needs to help break that into specific failure patterns.

For this case, the model may fail in several different ways:

- It changes the wrong file because it misunderstands the dependency between modules.
- It fixes the happy path but misses null inputs, retries, timeouts, or concurrency issues.
- It writes code that passes the visible test but would fail in production.
- It ignores logging, monitoring, security, or rollback concerns.
- It gives a confident explanation even when the root cause is uncertain.

Each failure pattern points to a different data need. If the model misses edge cases, experts should create tasks with hidden edge-case tests. If it misunderstands module dependencies, experts should create multi-file tasks where the bug requires tracing behavior across files. If it gives shallow explanations, the rubric should score reasoning quality, not just final code.

Core skill: **root-cause analysis of model behavior.**

## 4. Workflow Design

Once the failure pattern is clear, the SPL has to design the actual workflow.

For the backend debugging case, the SPL might choose a workflow like this:

1. Senior backend engineers create realistic multi-file bug tasks.
2. Each task includes a repo snippet, bug report, expected behavior, and hidden edge cases.
3. The model generates a fix and explanation.
4. Experts review the model output using a rubric.
5. A second reviewer checks a sample of outputs for consistency.
6. Disagreements are escalated and used to improve instructions.

The SPL also has to decide the output format. For example, should the expert provide a patch, a written explanation, a failure label, a preference ranking, or all of these? That choice depends on what the lab needs.

Core skill: **turning a messy problem into a repeatable workflow.**

## 5. Expert Profile Judgment

The SPL has to know what kind of expert is needed.

For this case, competitive programmers may not be the right fit. They may be excellent at algorithms but less familiar with production backend systems. The better expert profile is likely:

- senior backend engineers
- experience with production services
- ability to read multi-file codebases
- strong debugging and code review judgment
- familiarity with tests, deployment risk, latency, reliability, and security
- ability to explain why one solution is better than another

The expert profile has to match the failure pattern. If the model is failing at production-style debugging, the project needs experts who understand production-style debugging.

Core skill: **matching the task type to the expert profile.**

## 6. Rubric And Quality-Standard Design

The SPL has to define what "good" means.

Weak rubric:

> The answer should be correct.

Better rubric for this backend debugging case:

> The answer should identify the root cause, modify the right files, handle edge cases, avoid regressions, include or update tests, explain tradeoffs, and avoid security or reliability risks.

A useful rubric may score:

- correctness of the fix
- root-cause explanation
- edge-case handling
- test quality
- production readiness
- security and reliability awareness
- clarity of explanation

This matters because experts need a shared standard. Without a rubric, one reviewer may reward a minimal fix while another rewards a production-ready solution. The lab needs consistent signal, not random reviewer preference.

Core skill: **converting subjective judgment into structured criteria.**

## 7. Quality Control And Calibration

It is not enough to have good experts. The expert signal has to be consistent.

In this case, two senior engineers may disagree. One may think a small patch is best because it minimizes risk. Another may prefer a larger refactor because the root cause suggests deeper design debt. The SPL has to make sure reviewers are applying the same standard.

That may require:

- calibration rounds before full production
- examples of good and bad reviews
- sample audits by senior reviewers
- disagreement tracking
- escalation rules for ambiguous cases
- instruction updates when reviewers interpret the task differently

The goal is not just "expert quality." The goal is **consistent expert signal** that the lab can trust.

Core skill: **managing reliability in human judgment systems.**

## 8. Analytical Operations

The SPL also has to manage delivery.

For this backend debugging project, the SPL should track:

- tasks created
- model outputs reviewed
- QA pass rate
- rejection rate
- revision rate
- reviewer disagreement rate
- average turnaround time
- expert utilization
- delivery risk

If the project is behind schedule, the SPL should not jump straight to "hire more experts." The bottleneck might be unclear task instructions, slow QA, too many expert disagreements, overly complex tasks, or a rubric that reviewers interpret differently.

Core skill: **operational problem-solving with metrics.**

## 9. Tradeoff Thinking

The SPL has to balance speed, cost, volume, and quality.

For example, suppose the lab needs 10,000 coding examples quickly. Reviewing every example twice with senior engineers may produce high quality, but it may be too slow and expensive. The SPL could propose a more practical system:

- full QA for new experts
- lighter sampling for proven experts
- deeper review for high-risk or ambiguous tasks
- escalation only when reviewers disagree
- faster review for low-risk examples

The point is not to maximize quality in isolation. The point is to deliver useful data at the quality bar the lab needs, within the time and cost constraints.

Core skill: **making practical tradeoffs without losing the core quality bar.**

## 10. Stakeholder Communication

The SPL has to keep the lab, experts, reviewers, and internal teams aligned.

For this project, a useful update to the lab might sound like:

> We are seeing strong expert agreement on simple API bugs, but lower agreement on concurrency-related tasks. The current rubric does not clearly distinguish acceptable minimal fixes from production-ready fixes. We are adding two rubric criteria: regression risk and production readiness. This may slow throughput slightly this week, but should improve data consistency.

That kind of communication is specific. It explains what is happening, why it matters, what decision was made, and what tradeoff is involved.

Core skill: **clear communication under ambiguity.**

## 11. Iteration Mindset

The first workflow may not work perfectly.

For example, the first batch of backend tasks may be too easy, so the model performs well and the data does not expose useful failures. Or the tasks may be too ambiguous, causing expert disagreement. Or the lab may realize it cares more about explanations than code patches.

The SPL has to adjust the system quickly:

- make tasks harder
- clarify instructions
- revise the rubric
- change the expert profile
- add review layers
- change the output format
- create better examples for calibration

This is how the workflow improves after seeing real outputs.

Core skill: **learning from workflow failure and improving the loop.**

---

## Full Skill Map

| Job To Be Done | What The SPL Must Be Good At | In The Backend Debugging Case |
|---|---|---|
| Clarify the lab goal | Problem framing, AI literacy | Narrow "better coding" to multi-file backend debugging |
| Understand failure patterns | Root-cause analysis, model behavior diagnosis | Identify missed edge cases, wrong-file fixes, shallow reasoning, or production risks |
| Translate failures into workflow | Workflow design, task design | Decide whether experts create tasks, review model outputs, compare answers, or label errors |
| Identify experts | Expert profile judgment | Select senior backend engineers, not generic coders |
| Build the quality system | Rubric design, QA design, calibration | Define quality across correctness, tests, edge cases, reliability, and explanation |
| Manage delivery | Analytical operations, throughput management | Track volume, QA pass rate, reviewer disagreement, turnaround time, and delivery risk |
| Keep the lab aligned | Stakeholder communication, client feedback loops | Explain quality issues, tradeoffs, and workflow changes clearly |
| Iterate the workflow | Systems thinking, fast learning | Adjust tasks, rubrics, experts, and QA after seeing real outputs |

## The Short Version

To be good at SPL, you need to be strong at seven things:

1. **AI literacy:** know how data, evals, RLHF, and benchmarks fit into model improvement.
2. **Problem diagnosis:** identify exactly where the model is failing.
3. **Workflow design:** turn failure modes into expert tasks.
4. **Expert judgment:** know what kind of experts are needed.
5. **Quality systems:** build rubrics, QA, calibration, and escalation.
6. **Operational execution:** manage speed, volume, bottlenecks, and delivery.
7. **Stakeholder alignment:** keep labs, experts, reviewers, and internal teams aligned.

One-line summary:

> SPLs turn ambiguous model-improvement goals into reliable expert-data systems that produce high-quality signal at speed.

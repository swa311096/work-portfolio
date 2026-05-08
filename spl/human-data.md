---
title: Human Data
parent: SPL
nav_order: 1
permalink: /spl/human-data/
---

# Human Data

Human data matters because model improvement is not a vague process of "making the model better." It is a loop: define the capability, evaluate the model, identify weaknesses, create expert data, train or improve the model, and evaluate again.

The simple version is:

> Evals find the weakness. Expert data helps fix the weakness. Training updates the model. Evals check whether it worked.

This is where expert human judgment becomes valuable. A model may produce an answer that sounds fluent but misses the actual domain logic. An expert can see the gap, explain why the answer fails, and show what a better answer should look like. That judgment becomes useful training or evaluation signal.

---

## The Model Improvement Loop

A frontier AI lab first defines what "better" means. That target has to be specific. "Improve the model" is too vague; "make the model better at complex coding tasks," "medical reasoning," or "long multi-step instruction following" is more actionable. Once the target is clear, the lab evaluates the current model through benchmarks, internal evals, or expert review.

The evaluation tells the lab where the model is strong and where it fails. For a coding model, the lab may find that the model can answer simple questions but struggles with debugging existing code, handling edge cases, reasoning about architecture, or explaining tradeoffs. For a healthcare model, the lab may find that the model sounds confident but misunderstands plan benefits, payer behavior, or claim history.

Once the weakness is understood, the lab needs expert data. Experts might create difficult tasks, write reference answers, review model outputs, compare two answers, explain why one is better, build rubrics, or flag subtle mistakes. This is not generic annotation work. It is expert data because the quality depends on real domain judgment.

That data then becomes signal. In RLHF, for example, humans compare model responses and indicate which one is better. If a senior engineer says Answer B is stronger because it handles edge cases, avoids a security risk, and explains the architecture tradeoff, that preference can help train the model toward better engineering judgment.

After training or fine-tuning, the lab evaluates again. If the model performs better on the original weakness, the loop worked. If not, the lab may need better evals, better experts, clearer rubrics, or a different data workflow.

## Key Terms

An **evaluation**, or eval, is the process of testing a model. It asks how good the model is at a task. Evaluation is mostly measurement, not training.

A **benchmark** is the test used inside an evaluation. SWE-bench, for example, tests coding agents on real software engineering tasks. Evaluation is the act of taking the exam; the benchmark is the exam paper.

An **internal eval** is a private test created by the AI lab. Public benchmarks can become saturated or too generic, so labs create custom evals for specific weaknesses. A lab working on reimbursement reasoning, for example, may need a private eval for complex insurance cases because no public benchmark captures that exact workflow.

**Expert data** is high-quality human input from people with domain expertise: doctors, lawyers, software engineers, finance professionals, math experts, or other specialists. It helps the model improve in areas where correctness depends on judgment, not just surface-level fluency.

**Human feedback** is the judgment humans give on model outputs. A reviewer may say an answer is correct, wrong, misleading, incomplete, or better than another answer. That feedback can be used for evaluation, training, or both.

**RLHF** stands for Reinforcement Learning from Human Feedback. The simple meaning is that humans tell the system which responses are better, and the model is trained to produce more responses like the preferred ones.

A **rubric** is the quality standard used to judge outputs. For a coding task, a good rubric might consider correctness, edge-case handling, runtime efficiency, security, readability, and explanation quality. Rubrics matter because without them, different reviewers may judge the same answer inconsistently.

**Quality review** checks whether the expert data itself is good enough. If one expert writes a coding solution, another expert may review it and catch a missed concurrency issue. This is critical because bad data is not neutral. It can make the model worse or reduce the lab's trust in the workflow.

---

## Coding Example

Suppose an AI lab wants to improve a coding model. The target is not toy programming questions; the lab wants the model to become better at real-world backend engineering tasks.

The lab might evaluate the model with a task like:

> Here is a broken API endpoint. Find the bug, fix it, and explain the tradeoffs.

The model may produce code that looks plausible but misses important system behavior. It may forget rate limiting, fail on null values, ignore database latency, create security risks, or give a shallow explanation. The eval has exposed the weakness: the model can write code, but it does not yet reason like a strong backend engineer.

Now the lab needs senior software engineers to create better tasks, write correct solutions, add edge-case tests, review model outputs, and compare competing answers. One model answer may solve the basic problem but ignore edge cases. Another may handle empty input, database timeouts, tests, and security tradeoffs. A senior engineer can label the second answer as better and explain why.

That explanation is the valuable part. It teaches the system what strong engineering judgment looks like:

> Do not just write code. Consider edge cases, tests, performance, security, and tradeoffs.

After training on many examples like this, the lab evaluates again. The question is not just whether the model writes more code. The question is whether it handles harder engineering situations more reliably.

## Healthcare Example

The same loop applies to healthcare reimbursement reasoning.

Imagine a model needs to estimate likely reimbursement for an out-of-network behavioral health claim. The input may include insurance plan details, claim history, CPT codes, provider information, deductible status, coinsurance, out-of-pocket max, and historical payer behavior.

The model may fail in subtle ways. It might confuse allowed amount with paid amount, ignore deductible status, misunderstand plan-level benefits, or give a confident estimate that does not match how the payer actually behaves. A generic reviewer may not catch those mistakes. A healthcare billing expert can.

Expert data in this workflow might include a correct reimbursement estimate, an explanation of payer rules, appeal or rebilling logic, and examples of edge cases where the model is likely to fail. The expert may compare two model answers and prefer the one that accounts for deductible, coinsurance, plan limits, and payer history.

The model then learns a domain-specific lesson:

> In reimbursement workflows, do not estimate from CPT code alone. Check plan-level benefits, patient responsibility, payer history, and actual paid amount.

After improvement, the lab evaluates whether the model makes fewer reimbursement mistakes. If it still fails on payer-specific behavior or edge cases, the next data loop can be adjusted.

---

## Why Human Data Is Needed

Human data is needed because many important model failures are not obvious from the final answer alone. The model may sound fluent while applying the wrong rule, missing context, overstating confidence, or choosing the wrong next action.

Benchmarks can show that the model failed. Human experts explain why it failed and what better performance looks like.

The core value of human data is that it:

- defines quality
- exposes failure modes
- creates better examples
- turns expert judgment into training signal
- helps the lab measure whether the model actually improved

In simple terms:

> Models need expert human data when the difference between a decent answer and a great answer depends on judgment, context, tradeoffs, and domain expertise.

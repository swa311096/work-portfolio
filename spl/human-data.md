---
title: Human Data
parent: SPL
nav_order: 1
permalink: /spl/human-data/
---

# Human Data

Human data matters because model improvement is not a vague process of "making the model better." It is a loop:

**Define the target capability -> evaluate the model -> identify weaknesses -> create expert data -> train or improve the model -> evaluate again.**

Evals find the weakness. Expert data helps fix the weakness. Training updates the model. Evals check whether the fix worked.

---

## The Model Improvement Lifecycle

Think of human data as part of a stage-wise model improvement lifecycle.

### Stage 1: Define What "Better" Means

A frontier AI lab first decides what capability it wants to improve.

Examples:

- Make the model better at complex coding tasks.
- Make the model better at medical reasoning.
- Make the model better at following long, multi-step instructions.

This matters because "make the model better" is too vague. The lab needs a clear target before it can measure progress or create useful training data.

### Stage 2: Evaluate the Current Model

The lab then tests the current model to understand how good it is today.

This is where evaluations and benchmarks come in.

Example:

> The lab gives the model 1,000 coding problems and checks how many it solves correctly.

The goal is to identify:

- Where is the model strong?
- Where does it fail?
- What types of tasks expose the weakness?

### Stage 3: Identify Failure Patterns

After testing, the lab studies the model's mistakes.

Example:

The model may be good at simple coding questions but weak at:

- debugging existing code
- handling edge cases
- writing production-quality architecture
- explaining tradeoffs
- understanding ambiguous user requirements

This stage is important because the lab now knows what kind of human expertise is needed.

### Stage 4: Create Expert Data

Now the lab needs high-quality human input to fix those weaknesses.

This is where companies like Mercor become important. They may help find experts who can:

- write correct answers
- create difficult tasks
- review model outputs
- compare two answers
- explain why one answer is better
- create rubrics for quality
- flag model mistakes

This is called **expert data** because it comes from people with real domain expertise.

### Stage 5: Convert Human Feedback Into Training Signal

The expert data is then used to improve the model.

One common method is RLHF, where humans compare model outputs and say which one is better.

Example:

> The model gives two answers to the same coding problem. A senior engineer says Answer B is better because it handles edge cases, has cleaner architecture, and avoids a security risk.

That human preference becomes a signal to train the model.

The model gradually learns:

> This type of response is better than that type of response.

### Stage 6: Train or Fine-Tune the Model

The lab uses the expert data and feedback to update the model.

The model may be trained to:

- produce more accurate answers
- reason more carefully
- follow instructions better
- avoid unsafe responses
- perform better in specific domains
- choose responses humans prefer

This is where the human input starts changing model behavior.

### Stage 7: Evaluate Again

After the model is improved, the lab tests it again.

This answers:

- Did the model actually get better?
- Did benchmark scores improve?
- Did expert reviewers rate the new model higher?
- Did it fail less often on the earlier weak areas?

If yes, the improvement worked. If no, the lab goes back and creates better data, better evals, or better feedback loops.

### Simple Loop

The whole process is:

1. Define capability.
2. Evaluate model.
3. Identify weaknesses.
4. Create expert data.
5. Train or improve model.
6. Evaluate again.

Or even simpler:

> Evals find the weakness. Expert data helps fix the weakness. Training updates the model. Evals check if it worked.

---

## Key Terms

### Evaluation

An evaluation, or eval, is the process of testing a model.

It asks:

> How good is the model at this task?

Example:

> Give the model 500 legal reasoning questions and check whether lawyers agree with the answer.

Evaluation is not always training. It is mostly measurement.

### Benchmark

A benchmark is a standardized test used in evaluation.

Example:

> SWE-bench is used to test coding agents on real software engineering tasks.

So:

- Evaluation = the act of testing.
- Benchmark = the test you use.

Simple analogy:

> Evaluation is like taking an exam. The benchmark is the exam paper.

### Internal Eval

An internal eval is a private test created by the AI lab.

Public benchmarks can become saturated or too generic. Labs create private tests for specific weaknesses.

Example:

> A lab may create an internal eval for whether a model can correctly analyze complex insurance reimbursement cases.

That may not exist as a public benchmark, so experts create a custom eval set.

### Expert Data

Expert data is high-quality human input from domain experts.

Examples:

- a doctor writing correct medical reasoning
- a lawyer reviewing legal analysis
- a software engineer debugging code
- a finance expert grading investment memos
- a math expert creating hard reasoning problems

This data helps models improve in specialized areas.

### Human Feedback

Human feedback is when people review model outputs and give judgment.

Examples:

- This answer is correct.
- This answer is wrong.
- This answer is better than that answer.
- This explanation is misleading.
- This response misses an important edge case.

Human feedback can be used for evaluation, training, or both.

### RLHF

RLHF stands for Reinforcement Learning from Human Feedback.

Simple meaning:

> Humans tell the model which responses are better, and the model is trained to produce more of those better responses.

Example:

Prompt:

> Explain how to design a payment fraud detection system.

The model gives two answers. A senior engineer says:

> Answer B is better because it considers latency, false positives, data privacy, and monitoring.

That preference can be used to improve the model.

### Rubric

A rubric is the quality standard used to judge outputs.

Example rubric for a coding answer:

- correctness
- edge-case handling
- runtime efficiency
- security
- readability
- explanation quality

Rubrics matter because without them, human reviewers may judge inconsistently.

### Quality Review

Quality review means checking whether the expert data itself is good enough.

Example:

> If one expert writes a coding solution, another expert may review it and say: this solution works, but it misses a concurrency issue.

This is especially relevant to companies that supply expert data. It is not enough to produce lots of data. The data has to be accurate, consistent, and useful.

---

## Coding Example

Say an AI lab wants to improve its coding model.

### Stage 1: Define Target

The lab says:

> We want the model to become better at real-world backend engineering tasks.

Not toy coding problems. Real engineering tasks.

### Stage 2: Evaluate Current Model

The lab tests the model on coding benchmarks and internal tasks.

Example task:

> Here is a broken API endpoint. Find the bug, fix it, and explain the tradeoffs.

The model attempts the task.

### Stage 3: Identify Weakness

The lab notices:

> The model can write code that looks right, but it misses edge cases and does not reason well about system behavior.

For example:

- it forgets rate limiting
- it does not handle null values
- it ignores database latency
- it creates security risks
- it gives shallow explanations

### Stage 4: Bring in Experts

Now the lab needs senior software engineers.

The experts may create:

- better coding tasks
- correct solutions
- edge-case test cases
- code reviews
- comparisons between model outputs

This is expert data.

### Stage 5: Create Human Feedback

The model gives two answers.

Answer A solves the basic problem but ignores edge cases.

Answer B handles edge cases, explains tradeoffs, and includes tests.

A senior engineer labels:

> Answer B is better.

Then explains:

> Answer A fails when the input is empty and does not consider database timeout. Answer B handles both.

That feedback teaches the model what strong engineering judgment looks like.

### Stage 6: Train the Model

The lab uses many examples like this to improve the model.

The model starts learning patterns like:

> Do not just write code. Consider edge cases, tests, performance, security, and tradeoffs.

### Stage 7: Evaluate Again

The lab runs the improved model through the same or harder evals.

Now they check:

- Does it pass more test cases?
- Does it handle edge cases better?
- Do senior engineers rate its answers higher?
- Did its benchmark score improve?

If yes, the model improved.

---

## Healthcare Example

This example maps to healthcare reimbursement and out-of-network behavioral health workflows.

### Stage 1: Define Target

A lab or AI company wants a model to get better at healthcare reimbursement reasoning.

Example:

> Given insurance plan details, claim history, and provider information, estimate likely reimbursement and explain the reasoning.

### Stage 2: Evaluate Current Model

The model is tested on real or synthetic reimbursement cases.

The lab checks whether the model correctly interprets:

- deductible
- coinsurance
- out-of-pocket max
- CPT codes
- payer behavior
- claim history
- provider context

### Stage 3: Identify Weakness

The model may fail because:

- it misunderstands plan-level benefits
- it confuses allowed amount with paid amount
- it does not know how different payers behave
- it gives a confident but wrong estimate

### Stage 4: Create Expert Data

Healthcare billing experts create or review cases.

They may provide:

- correct reimbursement estimate
- explanation of payer rules
- reason why a claim was underpaid
- appeal or rebilling logic
- edge cases where the model would likely fail

### Stage 5: Create Human Feedback

An expert compares two model answers.

Answer A predicts reimbursement but ignores deductible status.

Answer B accounts for deductible, coinsurance, plan limits, and historical payer behavior.

The expert says:

> Answer B is better.

That becomes training or evaluation signal.

### Stage 6: Improve the Model

The model learns:

> In reimbursement workflows, do not just estimate from CPT code. Check plan-level benefits, patient responsibility, payer history, and actual paid amount.

### Stage 7: Evaluate Again

The lab tests whether the model now makes fewer mistakes on reimbursement cases.

That is how the loop works.

---

## Why Human Data Is Needed

Human data is needed because many important model failures are not obvious from the final answer alone.

A model may produce an answer that sounds fluent but:

- misses a domain-specific edge case
- applies the wrong rule
- ignores context
- overstates confidence
- fails to explain tradeoffs
- chooses the wrong next action

Benchmarks can show that the model failed. Human experts explain **why** it failed and what a better answer should look like.

That is the core value of human data:

- It defines quality.
- It exposes failure modes.
- It creates better examples.
- It turns expert judgment into training signal.
- It helps the lab measure whether the model actually improved.

In simple terms:

> Models need expert human data when the difference between a decent answer and a great answer depends on judgment, context, tradeoffs, and domain expertise.

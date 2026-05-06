---
title: Product Case Depth
parent: PM Interview Prep
nav_order: 3
permalink: /pm-interview-prep/product-case-depth/
---

# Product Case Depth

This page exists because the feedback is consistent: **the casing structure is there, but the answer does not go deep enough.**

The goal is not to memorize more frameworks. The goal is to build the habit of pushing every case one level deeper: sharper assumptions, richer user insight, clearer product judgment, and more grounded tradeoffs.

---

## What "not deep enough" usually means

An answer feels shallow when it stays at the category level:

- "Users want convenience."
- "We should improve onboarding."
- "This will increase engagement."
- "We can measure retention."
- "The risk is adoption."

A deeper answer makes those claims specific:

- Which users?
- In what situation?
- What are they trying to do?
- What breaks today?
- Why does that break matter?
- What behavior would change if we solved it?
- What would the company gain?
- What would we deliberately not solve?

The interviewer is usually not asking for more ideas. They are testing whether the idea is backed by real product thinking.

## The depth ladder

Use this ladder during practice. If an answer sounds generic, move one rung down.

| Level | Weak answer | Stronger answer |
|---|---|---|
| Category | "Improve onboarding" | "Reduce drop-off for first-time creators before they publish their first post" |
| User | "New users" | "Motivated new users who understand the product promise but fail before the first successful action" |
| Context | "They are confused" | "They arrive with intent, but hit setup choices before they understand what a good first outcome looks like" |
| Pain | "Too much friction" | "The product asks them to configure before they have confidence, so they postpone or abandon" |
| Product move | "Add recommendations" | "Start with a guided default path that produces one useful output before asking for customization" |
| Tradeoff | "Might not work for everyone" | "Power users may dislike defaults, so we keep an escape hatch while optimizing the first-session path" |
| Metric | "Activation" | "Percent of new users who complete the first meaningful action within the first session" |

## Case answer spine

For product design and strategy cases, keep the visible structure simple:

1. Clarify the company goal and constraints.
2. Segment users in a way that changes product decisions.
3. Pick one segment and defend the choice.
4. Describe the user's job, context, and current failure mode.
5. Translate the failure mode into product requirements.
6. Generate solutions that map directly to the requirements.
7. Prioritize one solution and explain the tradeoffs.
8. Define success metrics, risks, and next steps.

Depth comes mostly from steps 2-5. If those are thin, the rest of the answer will sound like product theater.

## The 5-depth pass

After choosing a user segment, force yourself through these five passes before proposing solutions.

### 1. Situation

What is happening around the user when the problem appears?

Weak:

> Busy professionals do not have time to work out.

Stronger:

> Professionals with unpredictable schedules often intend to work out, but the decision happens at the end of a draining day. The problem is not only time; it is that the next step has to feel obvious and low-risk when motivation is already low.

### 2. Motivation

What progress is the user trying to make?

Weak:

> They want to be healthier.

Stronger:

> They want to feel in control of their health without turning fitness into another planning burden. The product should help them convert intent into a small completed action.

### 3. Current workaround

What do they do today instead?

Weak:

> They skip the gym.

Stronger:

> They postpone with the belief that they will go tomorrow, or they do a low-effort substitute like walking, scrolling workout content, or saving routines. That means the product is competing with avoidance, not just other fitness apps.

### 4. Root failure

What is the actual product problem?

Weak:

> The product needs better reminders.

Stronger:

> The product needs to reduce the planning cost at the exact moment the user is deciding whether to act. A reminder alone creates guilt; a useful intervention gives them a specific next action.

### 5. Product requirement

What must the solution do to win?

Weak:

> Make workouts easier.

Stronger:

> It must recommend a workout that is short, context-aware, equipment-aware, and psychologically easy to start. The first screen should answer: "What should I do right now?"

## Segment harder

Most shallow cases come from weak segmentation. Segment by behavior and context, not only demographics.

| Prompt | Shallow segmentation | Better segmentation |
|---|---|---|
| Improve Spotify | Age, geography, income | Passive listeners, playlist builders, social sharers, discovery seekers, podcast-first users |
| Improve Uber | Riders vs drivers | Airport riders, late-night riders, commuters, price-sensitive riders, drivers optimizing idle time |
| Design for students | High school vs college | Students cramming before exams, students building habits, students choosing majors, students working part-time |
| Improve Amazon | Prime vs non-Prime | Mission shoppers, browsing shoppers, deal hunters, repeat buyers, high-consideration buyers |
| Improve TikTok ads | SMBs vs enterprises | Creative-constrained SMBs, performance marketers with creative fatigue, brands seeking awareness, agencies managing many clients |

Good segmentation should change the answer. If every segment would get the same solution, the segmentation is not useful.

## The "why this segment" test

When you pick a segment, justify it using at least two of these:

- **Pain intensity:** the problem is frequent, costly, emotional, or blocking.
- **Business value:** solving it improves revenue, retention, acquisition, trust, or strategic position.
- **Right to win:** the company has data, distribution, product surface, brand, or ecosystem advantage.
- **Learning value:** this segment teaches us something reusable for adjacent segments.
- **Feasibility:** the company can actually ship a credible solution.

Example:

> I will focus on creative-constrained SMB advertisers on TikTok. They have high pain because TikTok performance depends heavily on native-feeling video, but they often lack creative resources. They are strategically valuable because SMB spend is blocked by creation friction, not only targeting or budget. TikTok also has a right to win because it owns trend signals, ad performance data, and creative tooling inside Symphony.

## Make pain points causal

Do not list pain points as independent bullets. Connect them into a causal chain.

Weak:

- Users are busy.
- They forget.
- They do not know what to do.

Stronger:

> Because users are busy, they only have short decision windows. Because they do not know what workout fits that window, the decision becomes effortful. Because the decision is effortful, they postpone. So the root product problem is not memory; it is converting vague intent into a low-effort next action.

## Push solutions below the feature name

Feature names are not enough. For each solution, explain the product mechanism.

| Feature-level answer | Mechanism-level answer |
|---|---|
| Add AI recommendations | Use the user's time, goal, past completion, and available equipment to suggest one default next action |
| Add social features | Pair users with similar schedules and goals so accountability appears before the drop-off moment |
| Improve notifications | Trigger only when the user has a realistic action window, and include a concrete one-tap plan |
| Add gamification | Reward consistency of completed small actions, not vanity streaks that punish missed days |

If you cannot explain the mechanism, the feature is probably filler.

## Tradeoff bank

Use tradeoffs to show judgment. Do not say "there are privacy risks" and move on.

| Tradeoff | Depth prompt |
|---|---|
| Personalization vs control | When should the product choose for the user, and when should it ask? |
| Growth vs trust | Could this increase usage while degrading user trust or long-term retention? |
| Simplicity vs power | Which users are hurt by simplifying the flow? |
| Automation vs quality | What happens when the system is wrong? Is there a review or correction path? |
| Speed vs learning | Are we optimizing for quick completion or long-term user capability? |
| Marketplace liquidity vs quality | Does adding supply reduce reliability, relevance, or trust? |
| Monetization vs experience | Where does revenue pressure make the product worse? |

## Metrics that show depth

Use a metric stack instead of one success metric.

| Layer | Question | Example |
|---|---|---|
| North star | Did we create the intended user/company value? | Weekly users completing a meaningful workout |
| Input metric | Is the product mechanism working? | % of users accepting the recommended workout |
| Funnel metric | Where does the flow break? | Viewed recommendation -> started workout -> completed workout |
| Quality metric | Was the action good? | Completion satisfaction, repeat usage, saved routine rate |
| Guardrail | What could we harm? | Notification opt-outs, churn, injury reports, refund/support tickets |

For interviews, explain why each metric exists. The goal is to show that you understand the behavior you are trying to change.

## 30-minute practice drill

Use this drill three times a week.

| Time | Activity |
|---|---|
| 0-3 min | Clarify prompt, company goal, and assumptions |
| 3-8 min | Segment users and pick one |
| 8-14 min | Build the 5-depth pass: situation, motivation, workaround, root failure, requirement |
| 14-20 min | Brainstorm 3 solutions tied to the requirement |
| 20-24 min | Prioritize one and explain tradeoffs |
| 24-28 min | Define metric stack and risks |
| 28-30 min | Recap the logic in 5 sentences |

Record the answer. Then grade only depth, not polish.

## Depth scorecard

Score each practice answer from 1-5.

| Dimension | 1 | 3 | 5 |
|---|---|---|---|
| Segmentation | Generic user groups | Behavior-based segments | Segment choice changes the product direction |
| User insight | Surface-level wants | Clear jobs and pains | Specific context, workaround, and emotional/economic driver |
| Causality | Lists problems | Some prioritization | Clear chain from context to root failure |
| Solution depth | Feature names | Basic user flow | Mechanism, edge cases, and why it should work |
| Tradeoffs | Generic risks | Some pros/cons | Real product judgment with explicit sacrifices |
| Metrics | One metric | Funnel + success metric | Input, output, quality, and guardrails |

Target: average **4+** before optimizing for polish.

## Practice prompts

Start with familiar products, then move into less familiar domains.

- Improve YouTube for people learning technical skills.
- Design a better grocery shopping experience for working parents.
- Improve TikTok Symphony for small advertisers.
- Design a product for first-time managers.
- Improve Amazon search for high-consideration purchases.
- Design a better job search product for international MBA students.
- Improve Spotify discovery for users stuck in repetitive listening.
- Design an AI assistant for startup founders doing customer discovery.
- Improve Uber for airport pickups.
- Design a tool for students preparing for technical interviews.

## Personal case library

Use your own work stories as depth examples:

| Story | Depth angle to practice |
|---|---|
| [AWS networking growth research]({{ '/work/aws/networking-growth-research/' | relative_url }}) | Problem validation, customer segmentation, business case |
| [AWS agentic AI private network]({{ '/work/aws/agentic-ai-private-network/' | relative_url }}) | Abstracting complexity, technical product requirements, tradeoffs |
| [Inshorts user-generated ads platform]({{ '/work/inshorts/user-generated-ads-platform/' | relative_url }}) | 0-to-1 product design, marketplace expansion, monetization |
| [Interview Kickstart SE courses launch]({{ '/work/interview-kickstart/se-courses-launch/' | relative_url }}) | Segment selection, curriculum-product fit, GTM/product loop |
| [Dunzo checkout optimization]({{ '/work/dunzo/checkout-optimization/' | relative_url }}) | Funnel diagnosis, user friction, execution metrics |

After each case practice, map one part of the answer back to a real story. This makes the answer less abstract and gives you proof that you have actually made similar product decisions.

## Five-sentence recap template

Use this to close cases tightly:

1. The company goal is `X`, and I focused on `segment` because `reason`.
2. The core user problem is not just `surface pain`; it is `root failure`.
3. The product requirement is therefore `requirement`.
4. I would build `solution`, which works by `mechanism`.
5. I would measure `success metric`, monitor `guardrail`, and watch the tradeoff around `tradeoff`.

Example:

> The goal is to increase meaningful workout completion, and I focused on motivated but inconsistent gym members because they have clear intent but frequent drop-off. The core problem is not lack of health motivation; it is that they face a high planning cost when motivation is low. The product requirement is to convert vague intent into one low-risk next action. I would build a context-aware workout recommender that suggests a short default plan based on time, goal, past completion, and equipment availability. I would measure first-session workout starts and completions, monitor notification opt-outs and satisfaction, and watch the tradeoff between helpful defaults and user control.

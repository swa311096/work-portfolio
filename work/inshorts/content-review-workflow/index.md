---
title: "Content Review Workflow"
parent: Inshorts
grand_parent: Work
nav_order: 5
---

# Automating Content Review with Vertex AI — $1M+ in Annual Savings

**Company:** Inshorts ($550M Digital Media Platform)
**Role:** Product Manager, Public App
**Timeline:** Apr 2023 – Jun 2024

---

## The Problem

As part of a broader cost-efficiency initiative at Inshorts, I was responsible for automating our content review process.

At the time, content review was almost entirely manual. We had a **300-member operations team** reviewing **12,000 content cards per day** — every piece of content a creator submitted had to be read, watched, and approved by a human before it went live.

The challenge wasn't just cost. It was scale. As content volume grew, the ops team would need to grow with it — a model that wasn't sustainable.

My goals were threefold:
1. Identify which parts of the review workflow could be automated
2. Maintain a high bar for content accuracy and safety — errors could create legal and reputational risk
3. Reduce the overall volume of content requiring review and the number of steps in the cycle

---

## The Diagnosis

I started by mapping the review workflow end to end, shadowing reviewers and timing where effort was concentrated.

The finding: reviewers were spending the majority of their time on two things — validating the **written summary** attached to each video, and determining whether the **video itself** contained offensive or misleading content.

The written summary was particularly time-consuming because creators were writing it manually, with inconsistent quality. Reviewers spent as much time fixing bad summaries as they did evaluating content safety.

This pointed to two distinct automation opportunities: generate the summary automatically, and use AI to do a first pass on video content quality.

---

## What I Did

### 1. AI-generated summaries with Vertex AI

I proposed shifting the primary review artifact from a full manual review to a **60-word content summary** — a distilled version of the video that reviewers could evaluate quickly without watching the entire clip.

I led the initiative to integrate **Google Vertex AI** for multilingual video-to-text summarization. The model watched each video and generated a structured summary in the creator's language — Hindi, Tamil, Telugu, Bengali, and others — which then became the primary artifact for the review queue.

This had two effects: creators no longer had to write summaries manually (improving their experience), and reviewers could evaluate content faster and more consistently.

### 2. Creator quality scoring — risk-based prioritization

In parallel, I worked with engineering to redesign the review funnel itself using a creator quality scoring system.

Each creator was scored based on their **historical approval rates** — how often their past content had passed review without modification.

- **Top 50% of creators** (high approval history) → reduced review requirements, fast-tracked through the queue
- **Bottom 50% of creators** → full manual review

This meant human reviewers spent their time on the content and creators that actually warranted scrutiny — not wasting cycles on proven creators with clean track records.

The scoring system updated dynamically, so creators could improve their standing over time by consistently submitting high-quality content.

---

## Impact

- Reduced manual review volume by **~70%**
- Enabled **80% reduction in operations headcount**
- Saved **$1M+ annually** in ops costs
- System scaled with content growth — no need to add headcount as volume increased
- Improved creator experience by eliminating manual summary writing

---

## Skills & Tools
AI/ML Integration, Google Vertex AI, Multilingual NLP, Content Moderation, Risk-Based Prioritization, Workflow Automation, Ops Cost Reduction, Data Analysis, Cross-functional Leadership, Python

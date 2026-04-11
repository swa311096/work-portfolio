---
title: "Auction and Ranking"
parent: "Ads & Monetization"
nav_order: 2
nav_exclude: true
---

# Auction and Ranking

The most important question in an ads system is not "can an advertiser create an ad?"

It is:

**When a real impression opportunity appears, which ad wins, and why?**

That is the job of the auction and ranking system.

## The Basic Problem

At any moment, a platform may have many eligible ads for the same user and context:

- different advertisers
- different bids
- different objectives
- different predicted outcomes
- different levels of creative quality

But the platform only has a limited number of ad slots, and sometimes only one.

So it needs a way to decide:

1. which ads are eligible
2. how each eligible ad should be scored
3. which ad wins
4. whether the result is still acceptable for the user experience

## A Practical Mental Model

Most systems look roughly like this:

1. generate eligible candidates
2. filter by policy, budget, pacing, and targeting
3. predict outcomes for each candidate
4. combine bid and prediction into a ranking score
5. apply marketplace and user-experience guardrails
6. choose a winner and serve the ad
7. log outcomes so the system can learn

The exact math differs across platforms, but the product logic is usually similar.

## What Usually Goes Into The Ranking Score

A ranking system rarely uses bid alone.

It usually combines some version of:

- bid or advertiser willingness to pay
- predicted click, conversion, or watch probability
- expected value of the outcome
- user or content quality signals
- penalties from policy, safety, or low-quality experiences

The platform is effectively asking:

**Which ad creates the most marketplace value for this impression opportunity?**

That marketplace value is broader than short-term revenue.

If the platform only optimized for the highest raw bid:

- low-quality ads could dominate
- user trust would degrade
- advertiser ROI would worsen
- long-term spend would become less durable

## Why Ranking Is A Product Decision, Not Just A Modeling Decision

Ranking logic encodes business priorities.

A platform can tilt the system toward:

- short-term revenue
- user satisfaction
- advertiser efficiency
- exploration of new demand
- fairness across advertisers

That means auction design is not just an ML problem. It is a product and marketplace design problem.

For example:

- should new advertisers get some exploration volume?
- should weak creatives be penalized harder?
- should low-quality landing pages reduce auction competitiveness?
- should conversion-optimized campaigns beat engagement campaigns in the same inventory?

Those are product decisions disguised as ranking logic.

## What Pacing Changes

Even if an ad is strong, the platform may not want to spend the budget too fast.

So pacing systems affect ranking by asking:

- has this budget already spent too quickly today?
- should this campaign hold back for later hours?
- is delivery too concentrated in one audience pocket?

This matters because the "best" ad for one impression is not always the best ad for the whole day or the whole budget.

## The Core Tradeoff

Auction systems are usually balancing four things:

- monetization now
- advertiser outcomes
- user experience
- marketplace health over time

If a platform over-optimizes one of them, the system starts degrading elsewhere.

Examples:

- too much monetization pressure hurts user experience
- too much bias toward incumbents hurts new demand
- too much advertiser control reduces automated performance
- too much opacity reduces advertiser trust

## Failure Modes I Would Look For

If an ads marketplace is underperforming, I would usually inspect these possibilities:

- too few high-quality eligible ads
- weak prediction quality
- poor pacing logic
- bad objective setup by advertisers
- auction rules that reward low-quality spend
- insufficient controls around repetitive or intrusive ads
- reporting that makes advertisers optimize toward the wrong thing

## Questions I Would Use In A Company Teardown

When I study a company, these are the ranking questions I care about:

- what is the impression opportunity being allocated?
- how many ads are typically eligible?
- what outcomes is the platform trying to predict?
- what role does bid play versus predicted action rate?
- how does the platform protect user experience?
- where do pacing and budget constraints enter the system?
- how much control does the advertiser really have?
- what feedback loops improve the model over time?

That is usually where the real monetization strategy becomes visible.

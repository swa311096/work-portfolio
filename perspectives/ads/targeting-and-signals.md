---
title: "Targeting and Signals"
parent: "Ads & Monetization"
nav_order: 4
nav_exclude: true
---

# Targeting and Signals

Targeting is often described as "choose the audience."

That is true, but incomplete.

In practice, targeting is the interface between advertiser intent and platform understanding. The real system runs on signals.

## What Counts As A Signal

An ads platform can learn from many kinds of information:

- advertiser-selected audience inputs
- user profile information
- behavioral history
- contextual information
- device and session context
- past engagement with similar ads
- conversion feedback

Some of these are explicit. Some are inferred. Some are weak on their own but useful in combination.

## Why Signals Matter

Signals affect every important step in delivery:

- eligibility
- prediction quality
- ranking confidence
- optimization speed
- reporting usefulness

Better signals usually mean the system can make better guesses about:

- who is likely to click
- who is likely to convert
- which creative will resonate
- how aggressively the system should bid or pace

## The Shift From Manual Targeting To Model-Led Delivery

Older ads systems gave advertisers lots of manual levers:

- age
- gender
- interests
- keywords
- lookalikes
- placements

Modern systems still expose some of these, but many platforms increasingly push advertisers toward broader inputs and more automation.

Why?

Because the platform often has more signal and more modeling power than the advertiser does.

The pitch becomes:

**Tell us your goal and give us enough conversion feedback. We will find the right users.**

That works well when:

- the platform has dense user data
- conversion feedback is reliable
- enough volume exists for the model to learn

It works poorly when:

- conversion events are sparse
- the business is new
- privacy constraints reduce observability
- the platform has weak first-party understanding

## Signal Quality Is Uneven

Not all signals are equally useful.

Three questions matter:

1. how predictive is the signal?
2. how fresh is the signal?
3. how reliably can the platform observe it?

For example:

- recent intent usually matters more than stale affinity
- first-party actions are often stronger than broad demographic guesses
- post-click conversion signals are powerful but can be delayed or noisy

## The Core Product Tradeoff

Advertisers want control. Platforms want performance. Those two goals do not always align.

More manual targeting can:

- improve advertiser comfort
- make campaigns easier to reason about
- help in niche use cases

But it can also:

- reduce model flexibility
- shrink reach too early
- make learning slower
- create fragile performance

Broader targeting can improve optimization, but it also creates anxiety because the system becomes harder to inspect.

So one core ads product question is:

**How much control should the advertiser keep, and how much should the system abstract away?**

## Failure Modes I Would Watch For

- targeting is too narrow, so the model cannot learn
- feedback events are too sparse
- expansion is too aggressive and hurts quality
- privacy changes break attribution or signal coverage
- the platform overstates precision it does not actually have
- advertiser tools expose controls that the ranking system mostly ignores

## Questions I Would Use In A Company Teardown

- what are the strongest first-party signals available to the platform?
- how much of delivery is driven by explicit targeting versus model inference?
- how quickly does the system learn from new conversion feedback?
- how much explainability does the advertiser get?
- where do privacy constraints most damage performance?
- what kinds of advertisers benefit most from automation, and who struggles?

This is where the real sophistication of an ads platform often shows up. Good targeting is not about exposing more filters. It is about turning noisy signals into reliable delivery decisions.

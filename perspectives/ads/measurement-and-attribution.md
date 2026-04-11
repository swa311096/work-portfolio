---
title: "Measurement and Attribution"
parent: "Ads & Monetization"
nav_order: 4
nav_exclude: true
---

# Measurement and Attribution

Measurement is what closes the ads loop.

Without it, advertisers do not know whether spend worked, platforms cannot optimize well, and reporting becomes a source of confusion instead of trust.

## The Core Question

After an ad is shown, clicked, or watched:

**What outcome should the platform claim credit for, and how confident should anyone be in that claim?**

That is the attribution problem.

## What A Measurement System Usually Needs

At a minimum, a platform needs:

- impression logging
- click or engagement logging
- conversion event capture
- some way to connect user actions back to ad exposure
- reporting layers for advertisers

In stronger systems, measurement also includes:

- configurable attribution windows
- deduplication across surfaces
- modeled conversions
- experiments and lift studies
- diagnostics that explain where performance changed

## Why Attribution Is Hard

A user may:

- see multiple ads
- click one ad but convert later
- convert on another device
- be influenced by the ad without clicking it
- have their activity partially hidden by privacy rules

So attribution is never just "count purchases after clicks."

It is a set of assumptions about causality, visibility, and reporting rules.

## The Product Importance Of Attribution Windows

A seven-day click window and a one-day click window can produce very different reported performance.

That matters because attribution settings shape:

- how efficient the campaign appears
- what campaigns advertisers keep funding
- what the optimization system learns from
- how comparable one platform is to another

So attribution policy is not a reporting detail. It changes marketplace behavior.

## Last-Click Is Useful, But Incomplete

Simple attribution models are attractive because they are easy to explain.

But they often miss reality:

- upper-funnel campaigns get under-credited
- assist effects disappear
- cross-channel journeys get flattened
- platforms compete to claim the same conversion

That is why more mature advertisers eventually care about:

- incrementality
- holdouts
- media mix context
- platform bias in self-reported numbers

## What Good Measurement Should Do

A strong measurement system should help an advertiser answer:

- what happened?
- why did it happen?
- how much confidence should I have?
- what should I change next?

That means reporting needs both performance visibility and interpretability.

It is not enough to show:

- spend
- clicks
- conversions
- CPA

The platform also needs to help diagnose:

- learning instability
- signal loss
- audience saturation
- creative fatigue
- delayed conversion behavior

## Failure Modes I Would Look For

- conversion logging is incomplete
- attribution rules are opaque
- reporting overstates certainty
- optimization is trained on noisy labels
- advertisers cannot reconcile platform numbers with their own data
- privacy changes silently reduce signal quality

## Questions I Would Use In A Company Teardown

- what conversion events can the platform observe directly?
- how does it handle delayed or cross-device conversion behavior?
- what attribution defaults shape advertiser decision-making?
- how much of reporting is deterministic versus modeled?
- what diagnostics exist beyond topline metrics?
- does the platform offer incrementality or lift tooling?

Measurement is where advertiser trust is either built or destroyed. If reporting feels inflated, inconsistent, or impossible to interpret, marketplace quality eventually weakens even if short-term revenue looks healthy.

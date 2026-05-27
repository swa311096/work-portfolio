---
title: Referral Quality
parent: SPL
nav_order: 4
permalink: /spl/referral-quality/
---

# Referral Quality

Referrals should be treated as a managed expert-supply channel, not an open invite system.

The goal is not to maximize the number of referred experts. The goal is to maximize the quality of referred experts after onboarding: who passes screening, completes accepted work, maintains quality, and becomes useful for real client projects.

## 1. Limit Referral Volume Unless Quality Is Proven

A new referrer should not be able to submit unlimited candidates.

Example:

| Referrer type | Active referral cap |
|---|---:|
| New referrer | 3 active referrals |
| Strong referrer | 10-20 active referrals |
| Trusted referrer | Higher cap for urgent projects |

This forces referrers to be selective. If they know they only have a small number of active slots, they are less likely to send weak candidates casually.

## 2. Require Role-Specific Referral Context

Mercor should not allow low-signal referrals like "my friend is smart."

Referrers should submit structured context:

- what domain the expert is strong in
- why they are qualified
- where they have worked or studied
- what tasks they are likely good at
- whether the referrer has directly worked with them
- confidence score

This creates accountability and gives Mercor better routing data. A strong referral is not just a name; it is a hypothesis about where that expert can create high-quality data.

## 3. Penalize Bad Referrals Softly But Clearly

If a referrer repeatedly sends poor candidates, Mercor should respond with graduated limits:

- reduce their payout eligibility
- lower referral caps
- deprioritize their referrals
- require stronger justification
- pause referral access if abuse continues

The goal is not to punish one bad referral. The goal is to stop repeated low-quality volume before it wastes screening time, client capacity, or project QA bandwidth.

## 4. Use Project-Specific Referral Requests

Instead of saying "refer experts," Mercor should make the request specific:

> We need senior backend engineers with distributed systems experience who can evaluate Kubernetes debugging tasks.

This improves match quality because referrers know exactly who to look for. It also helps Mercor attract candidates who map to live demand, rather than building a broad but weak expert pool.

## 5. Add Anti-Collusion Checks

Because money is involved, Mercor should watch for gaming.

Red flags include:

- one referrer sends many weak profiles quickly
- referred experts share similar writing or test patterns
- experts refer each other in a closed loop
- referrals pass screening but underperform immediately
- referrer and expert submit overlapping work artifacts

These patterns should trigger review before more payouts are released. The system should assume most referrals are legitimate, but it should still have controls for repeated abuse, closed-loop referrals, and payout farming.

## Interview Answer

Mercor should treat referrals like a performance-managed acquisition channel. I would not optimize for number of referred experts. I would optimize for referred-expert quality after onboarding.

The system should have staged payouts, referrer quality scores, referral caps, and tiered privileges. A referrer only earns the full bonus if the expert passes screening, completes accepted work, and maintains quality over a defined period. Over time, high-quality referrers get higher caps and better incentives, while low-quality referrers are limited or paused.

This aligns incentives correctly: referrers make money only when they bring people who can actually deliver high-quality data.

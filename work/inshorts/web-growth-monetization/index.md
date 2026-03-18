---
title: "Web Growth & Monetization"
parent: Inshorts
grand_parent: Work
nav_order: 4
---

# Driving 6x DAU Growth on Inshorts Web

**Company:** Inshorts ($550M Digital Media Platform)
**Role:** Product Manager, Public App
**Timeline:** Apr 2023 – Jun 2024

---

## The Problem

When I joined Inshorts, my first project was to grow traffic and engagement on our web platform.

To give context: our short-video mobile app had around **8 million daily active users**. The web platform had **200,000** — roughly 2.5% of the mobile base. For a news platform where organic search should be a natural distribution channel, that gap was a significant missed opportunity.

My goals were threefold:
1. Identify why web traffic was so low
2. Fix core traffic and performance issues
3. Redesign the web experience to drive meaningful engagement and retention

---

## The Diagnosis

I started by digging into Google Search Console and analytics data. Three major issues surfaced immediately:

**1. Only 30% of pages were being indexed**
Google was crawling the desktop versions of pages, but our content was rendered on mobile. Since Google uses mobile-first indexing, most of our pages simply weren't showing up in search results.

**2. URL structure was a mess**
URLs were unstructured and non-descriptive — no location context, no content hierarchy. For a platform whose entire value proposition was *local* news, this was a direct hit to our SEO relevance for location-based queries.

**3. Video delivery was killing performance**
We were serving MP4 files directly, which meant the entire video had to load before playback. On slower mobile connections — exactly the network conditions of our tier 2/3 audience — this created multi-second delays that drove users away before they saw any content.

---

## What I Did

### Fixing indexing and URL structure

I partnered with the front-end engineering team to fix mobile page indexing — ensuring the mobile-rendered versions of pages were the ones Google was crawling and indexing.

We also restructured URLs to be location-based, organizing content by city and state. For a news platform, this was a significant SEO unlock — queries like "Patna news today" or "Chhattisgarh local news" now had a proper URL hierarchy to land on.

**Result: indexing improved from 30% to 70%+**

### Improving video performance

We converted video delivery from MP4 to **HLS (HTTP Live Streaming)**, which streams video in small chunks rather than loading the full file upfront. This dramatically reduced time-to-first-frame, especially on the slower connections common in tier 2 and tier 3 cities.

### Redesigning the web experience

In parallel, I worked with the UX design team to simplify the web experience from the ground up.

The existing page had too many engagement elements competing for attention — it was unclear what a user was supposed to do. We stripped it back to focus on two core actions: **sharing content** and **installing the app**.

We also added **location filters** so users could navigate to their city or state's content directly, reinforcing the local-first positioning.

Finally, I ran A/B tests comparing two content layout approaches:
- **Scroll-based** — continuous scrolling through a feed
- **Stacked view** — discrete content cards, one at a time

The stacked view won on engagement and retention metrics. We rolled it out as the default.

---

## Impact

- Grew website DAU **6x — from 200,000 to 1.2M** within two months
- Improved **D7 retention from 8% to 23%**
- Improved site indexing from **30% to 70%+**
- Unlocked **Google Ads on web** as a new revenue channel for the company

---

## Skills & Tools
SEO, Google Search Console, Web Performance, HLS Streaming, UX Design, A/B Testing, Growth, Retention, Google Analytics, Mixpanel, Google Ads, Front-end Engineering Collaboration

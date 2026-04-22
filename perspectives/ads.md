---
title: "Ads & Monetization"
parent: Operating Notes
nav_order: 1
nav_exclude: true
has_children: true
---

# Ads & Monetization

I think about ads systems as marketplaces, but that is only half the story.

The more useful lens is:

**Ads platforms are intent interpretation systems.**

Every platform is trying to answer some version of the same question:

**What does this user seem to want right now, and what kind of commercial message can fit that moment without breaking the experience?**

That is why ads products look so different across platforms. The main difference is not just format or auction design. It is where user intent comes from, how clearly it is expressed, and how confidently the platform can act on it.

## The Core Tension

Every ads system still has to balance three things:

- advertiser outcomes
- audience experience
- platform revenue

But those outcomes are downstream of a more fundamental problem:

- what intent exists on the platform?
- how observable is that intent?
- what advertiser use cases does that support?
- how does the platform turn that into targeting, ranking, and measurement?

This section is where I want to build a working operator's understanding of ads platforms through that lens.

## Platforms We Care About For Now

Different platforms support different ad use cases because user intent appears in different forms.

| Platform | What intent looks like | What ads are strongest | Why |
|---|---|---|---|
| Google | Explicit query intent | Demand capture, direct response | The user is already stating what they want |
| Meta | Identity, behavior, and latent interest | Discovery, demand generation, retargeting | Intent is inferred rather than directly stated |
| TikTok | Entertainment and content-affinity feedback | Creative-led discovery, impulse conversion | Creative quality shapes commercial opportunity |
| Snap | Visual communication and camera-native behavior | Brand storytelling, AR, youth-oriented discovery | The format itself shapes receptivity and engagement |
| Reddit | Topic and discussion intent | Contextual and interest-based ads | Relevance comes from conversation and community context |
| Pinterest | Planning and visual intent | Discovery with commercial adjacency | Users are often already collecting ideas with purchase potential |

This is why the same advertiser behaves differently on different platforms.

The platform is not just offering inventory. It is offering a specific kind of intent access.

## What Strong Ads Fluency Should Look Like

If this section gets stronger over time, it should let me do five things well:

1. explain what kind of intent a platform has access to
2. map that intent to the advertiser use cases the platform supports best
3. diagnose how that intent flows into targeting, ranking, and measurement
4. compare why one platform is structurally stronger than another for a given job
5. reason about monetization tradeoffs without losing sight of user experience

## The Core Actors

- advertisers or businesses
- audiences or users
- platform or publisher

Every meaningful ads decision is some version of this balancing act:

- advertisers want efficient outcomes
- users want relevance and a product experience that does not feel degraded
- platforms want monetization that remains durable over time

## A Simple Ecosystem Model

The basic loop looks like this:

1. advertisers create ads
2. advertisers define how they want those ads distributed
3. the platform distributes ads to relevant audiences
4. audiences interact with those ads
5. those interactions feed back into delivery, optimization, and reporting

Even this simple loop breaks into multiple product systems:

- ad creation
- audience selection
- auction and ranking
- delivery and pacing
- measurement and attribution
- reporting and optimization

That loop is useful because it makes clear that an ads platform is not one product. It is a bundle of connected products:

- advertiser tooling
- ranking and serving systems
- measurement systems
- marketplace health controls

## A Better Way To Compare Ads Platforms

When I study an ads business, these are the first questions I care about:

1. where does user intent come from on this platform?
2. is that intent explicit, inferred, or created by the product itself?
3. what advertiser jobs does that make the platform good at?
4. how strong are the platform's first-party signals?
5. how much does creative matter relative to targeting or bid?
6. what does the ranking system optimize for?
7. how much trust should advertisers place in the measurement?

That usually gets to the heart of the business faster than jumping straight into campaign setup screens.

## What An Ads Platform Is Really Trying To Do

The platform wants to maximize monetizable demand without breaking the user experience.

In practice, that means balancing:

- advertiser outcomes
- audience experience
- platform revenue
- marketplace quality over time

If ad load rises too aggressively:

- user experience degrades
- ad quality usually falls
- advertiser ROI gets weaker
- long-term demand becomes less durable

So the better mental model is:

**Show the highest-value ads in the right context, at the right time, without degrading the product experience or breaking advertiser outcomes.**

But "right context" is the key phrase. Context is where intent becomes monetizable.

On some platforms, context is explicit:

- a search query
- a product page
- a shopping session

On others, it is inferred:

- who the user is
- what they have engaged with before
- what the current content session suggests

And on entertainment platforms, the system is often trying to create commercial intent inside a non-commercial session.

The phrase "highest-value" matters because value is not just bid price. In most modern systems, value is some combination of:

- advertiser willingness to pay
- predicted action probability
- user or context quality
- platform constraints
- policy and safety filters

## The Five Core Systems

These are the downstream systems that convert intent into monetization.

| System | What it does | Why it matters | Current note |
|---|---|---|---|
| Ad structure and setup | Organizes objectives, budgets, audiences, and creatives | This is how advertiser intent gets translated into campaign inputs | [Ads Structure](structure/) |
| Objectives and optimization | Translates business goals into delivery goals | This determines what the system is trying to maximize | [Ad Objectives](ad-objectives/) |
| Auction and ranking | Decides which ad wins a given opportunity | This is where monetization, relevance, and user experience collide | [Auction and Ranking](auction-ranking/) |
| Targeting and signals | Determines who is eligible and what the system knows | This is how the platform operationalizes intent and prediction | [Targeting and Signals](targeting-and-signals/) |
| Measurement and attribution | Connects spend to outcomes | This is how the platform explains whether its interpretation of intent was useful | [Measurement and Attribution](measurement-and-attribution/) |

### 1. Ad Creation And Setup

This usually includes:

- ad formats
- ad structure
- creative tooling
- creative optimization
- publishing and review workflows

| Topic | About |
|---|---|
| [Ads Structure](structure/) | How most ads managers organize campaigns, ad groups, and creatives |

### 2. Objectives And Optimization

The same ad can perform very differently depending on what the advertiser is asking the platform to optimize for.

Common objectives include:

- reach
- traffic
- app installs
- video views
- leads
- conversions
- purchases

The objective matters because it shapes:

- what delivery system tries to maximize
- what feedback matters most
- how performance gets evaluated
- what tradeoffs the advertiser is implicitly making

| Topic | About |
|---|---|
| [Ad Objectives](ad-objectives/) | How advertiser goals shape optimization, delivery, and what "good performance" means |

### 3. Auction And Ranking

An ad platform cannot show every eligible ad, so it needs a ranking layer that decides:

- which ads are eligible
- how those ads are scored
- whether revenue or user experience is being over-weighted
- how pacing, budget limits, and policy constraints affect the outcome

This is usually the most important monetization system in the stack.

| Topic | About |
|---|---|
| [Auction and Ranking](auction-ranking/) | How platforms decide which ad wins and what tradeoffs shape the result |

### 4. Targeting And Signals

Depending on the platform, the main targeting inputs may include:

- explicit advertiser inputs
- platform-side user understanding
- contextual information
- historical engagement signals
- conversion feedback

Signals matter because they influence:

- who becomes eligible
- what the model can predict
- how quickly the system learns
- how resilient performance is under privacy constraints
- how much control the advertiser really has

| Topic | About |
|---|---|
| [Targeting and Signals](targeting-and-signals/) | The signal layer behind delivery, relevance, and optimization |

### 5. Measurement And Attribution

This usually includes:

- event tracking
- attribution
- conversion reporting
- lift or incrementality concepts
- dashboards and diagnostics

Measurement is what closes the loop between:

- spend
- delivery
- outcomes
- future optimization

| Topic | About |
|---|---|
| [Measurement and Attribution](measurement-and-attribution/) | How platforms decide what counts as success and what advertisers get to see |

## Platform Cases

This is where I want to apply the framework to specific companies.

| Platform | Core intent lens | Why it matters | Current note |
|---|---|---|---|
| Google | Explicit query intent | Cleanest example of demand capture | [Google: Explicit Intent](google/) |
| Meta | Inferred identity and behavioral intent | Strong benchmark for model-led social advertising | [Meta: Inferred Intent](meta/) |
| Snap | Camera-native communication intent | Useful contrast on format, audience, and creative surface area | Planned |
| Reddit | Topic and discussion intent | Good case for contextual relevance and community trust | Planned |
| Pinterest | Planning and visual discovery intent | Distinct because commercial intent is often adjacent to inspiration | Planned |
| TikTok | Entertainment intent and inferred content affinity | The platform often creates demand through creative rather than capturing explicit demand | [TikTok: Creative-Led Intent](tiktok/) |

## What I Want To Build Next

This section should eventually produce a small library of high-signal artifacts:

- platform-by-platform intent maps
- end-to-end system maps of major ads platforms
- auction and ranking explainers
- targeting and signal frameworks
- measurement and attribution breakdowns
- company-specific teardown notes
- PM tradeoff memos on monetization decisions

That is the actual goal. Not just "write about ads," but build evidence that I can reason about ads products as systems for interpreting and monetizing user intent.

Across companies, I usually look at the same core questions:

- where does user intent come from?
- where do ads fit in the product experience?
- what is the advertiser trying to achieve?
- is the platform capturing demand or creating demand?
- what are the key ranking and delivery decisions?
- what does measurement likely look like?
- what constraints come from privacy, policy, or supply?
- what tradeoffs define the business?

---
title: "Agentic AI Private Network"
parent: Amazon Web Services
grand_parent: Work
nav_order: 1
---

# Designing an Agentic AI Solution for AWS Networking

**Company:** Amazon Web Services
**Role:** Senior PM Technical Intern, EC2 VPC
**Timeline:** Jun 2025 – Aug 2025

---

## The Problem

Once the business case was established — startups were dropping AWS at the top of the funnel because networking was too complex — the next question was: **what does the solution actually look like?**

The existing experience required developers to manually configure 20+ networking services, manage IP address blocks, set up routing, and ensure best practices for every service combination. For a startup developer without an infrastructure background, this was weeks of work before a single line of product code could run.

The goal: design a solution that removes this friction entirely.

---

## The Insight

The key observation from the research phase was that developers don't think in terms of networking primitives — they think in terms of the services they're using. A startup building a web app doesn't think *"I need a VPC, subnets, route tables, and security groups"* — they think *"I have an EC2 instance, an RDS database, and an S3 bucket, and I need them to talk to each other."*

The solution had to meet developers at that level of abstraction.

---

## What I Did

### 1. Mapped startup application patterns

I analyzed the types of applications startups build on AWS and catalogued the most common service connectivity scenarios — which services get used together, how they need to be connected, and what the failure modes look like at each stage.

This gave us a finite set of patterns that covered the vast majority of startup use cases — the foundation for a templated solution.

### 2. Designed the agentic networking solution

The solution I designed flipped the interaction model entirely.

Instead of asking developers to configure the network, we ask them one question: **which services does your application use, and which ones need to connect?**

From those inputs — EC2, RDS, S3, and a simple connectivity map — the system automatically:
- Provisions all underlying networking services
- Manages IP address allocation and routing
- Applies AWS best practices for the specific service combination selected
- Handles scaling configurations that would otherwise require manual refactoring later

This is the agentic layer: the developer describes *what* they want, and AWS builds *how* to get there.

### 3. Defined APIs and built the UX

I worked with the engineering team to define the APIs that would power this experience — what inputs the system takes, how it reasons over service combinations, and what it provisions in response.

I also designed the console UX workflows, mapping out how a developer would actually interact with this in the AWS console — from initial setup through monitoring and modification.

### 4. Documented and secured cross-functional buy-in

I wrote the full product documentation — covering the technical architecture, the user flows, and the business rationale — and presented it to the broader EC2 networking team to align engineering and product leadership on the path forward.

---

## Impact

- Reduced infrastructure configuration steps by **80%+**
- Cut total time to deploy applications from **weeks to days**
- Secured cross-functional buy-in from engineering and product leadership for implementation

---

## Skills & Tools
Product Strategy, API Design, Agentic AI, UX Workflows, Technical Documentation, System Design, AWS EC2, VPC Networking, Cross-functional Leadership

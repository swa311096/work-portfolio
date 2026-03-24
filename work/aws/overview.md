---
title: "AWS Networking — Overview"
parent: Amazon Web Services
grand_parent: Work
nav_order: 0
---

# AWS Networking — Overview

#### TL;DR

AWS offers 20+ networking services — Lattice, PrivateLink, Peering, Transit Gateway, NAT Gateway, and more — built on top of core networking primitives: VPCs, subnets, route tables, NACLs.

Together, these services handle virtually every connectivity scenario a company needs to build, launch, and scale applications on AWS. But they come with a steep learning curve — which makes them particularly difficult for early-stage and growth-stage startups that don't have dedicated cloud infrastructure teams.

**My project: simplify how startups build, manage, and scale network infrastructure on AWS.**

---

#### What AWS Networking Actually Does

Applications running on AWS use a combination of services to function — compute (EC2, ECS, Lambda), storage (RDS, S3), AI/ML capabilities (Bedrock, SageMaker). For these resources to work — to serve customers over the internet and communicate securely with each other — they need a private network in the cloud.

That's what the networking team builds. I was part of the EC2 networking team at AWS, which owned VPC and all network connectivity services: Peering, Cloud WAN, Transit Gateway, NAT Gateway, PrivateLink, and Lattice.

---

#### A Brief History: From EC2-Classic to VPC

**EC2-Classic — The Original Architecture**

AWS's original network model was a flat network. You'd pick any service, launch an instance, and it would land on a shared flat network alongside every other customer's instances. Connectivity between services was straightforward — everything was on the same network.

But EC2-Classic had a fundamental problem: **no isolation, no advanced controls.**

![EC2-Classic vs VPC](../assets/ec2-classic-vs-vpc.png)

| | EC2-Classic | EC2-VPC |
|---|---|---|
| **Network isolation** | Shared with all AWS customers | Logically isolated, private to your account |
| **IP addressing** | Private IPs reset on every restart | Static private IPs that persist across stops/starts |
| **Security Groups** | Inbound rules only | Full inbound + outbound (egress filtering) |

**VPC — Your Private Data Center in the Cloud**

AWS VPC (Virtual Private Cloud) gives you a logically isolated section of the AWS Cloud where you launch resources in a network you define — complete control over IP address ranges, subnets, routing, and gateways.

Think of it as your own private data center, but in the cloud.

![AWS VPC Components](../assets/vpc-components.png)

More control and isolation was a massive improvement — but it also created a new problem.

---

#### The Complexity Explosion

VPC meant more control, but more control meant more connectivity scenarios to handle:

- VPC → Internet
- Internet → VPC
- VPC ↔ VPC (same region, different regions, different accounts, different organizations)
- VPC → Private network (GCP, Azure)
- VPC → On-premises data center
- VPC → AWS services outside the VPC (S3, DynamoDB)

To address each of these scenarios, AWS built dedicated services:

| Connectivity Scenario | Service |
|---|---|
| VPC ↔ VPC (same account/region) | VPC Peering |
| VPC ↔ VPC (multi-account/region) | Transit Gateway |
| VPC ↔ On-premises | Site-to-Site VPN, Direct Connect |
| Private access to AWS services | PrivateLink |
| Service-to-service within VPC | Lattice |
| Outbound internet from private subnet | NAT Gateway |
| Multi-region WAN | Cloud WAN |

The result: **20+ networking services**, each solving a specific scenario, each with its own configuration model, on top of VPC-level building blocks — subnets, IP address management, route tables, NACLs, security groups.

---

#### The Problem This Creates for Startups

AWS's approach ensures that no matter the scale or use case, there's a service for it. But the cost of that completeness is a steep learning curve.

For enterprises with dedicated cloud infrastructure teams, this is manageable. For **early-stage to growth-stage startups** — which typically don't have a cloud infra specialist — navigating 20+ services with overlapping use cases and AWS-specific networking primitives is genuinely difficult.

Misconfiguring an IP address block can cause complete connectivity loss across services. Fixing it means refactoring the entire network setup — a multi-week detour for a founding team trying to ship product.

**This is where my project came in: simplify how startups build, manage, and scale network infrastructure for their applications on AWS.**

*(Note: Observability and security were out of scope — the focus was entirely on the building and scaling experience.)*

---

*Continue reading:*
- [Networking Growth Research](../networking-growth-research/) — How we built the business case and scoped a $200M opportunity
- [Agentic AI Private Network](../agentic-ai-private-network/) — The solution we designed

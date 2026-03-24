---
title: "Agentic AI Private Network"
parent: Amazon Web Services
grand_parent: Work
nav_order: 1
---

# Agentic AI Private Network

**Company:** Amazon Web Services  
**Role:** Senior PM Technical Intern, EC2 VPC  
**Timeline:** Jun 2025 – Aug 2025

After [problem validation](../networking-growth-research/) aligned the team on the business case, the next step was to define what we would build.

---

#### TL;DR

**Pain points**

- **Getting started:** Developers often skip learning core networking building blocks like subnets and IP addressing, which leads to inefficient and costly architecture later.
- **Scaling:** As they grow, they struggle to choose the right networking services when connectivity needs get complex.

**Approach**

Abstract networking out of the user flow. Instead of asking users to work with networking primitives, the product takes inputs at the **application-resource** level: which resources they are using, which are public vs. private, and which resources need to connect—including the internet, on-prem systems, and other cloud providers.

**Outcome**

Based on those inputs, AWS automatically creates the underlying network infrastructure using best practices, reducing configuration steps by roughly **80%** and cutting time to launch from **weeks to days**.

---

#### What we heard (70+ interviews)

I interviewed 70+ early-stage AWS customers to understand where networking was breaking down for them. Two pain points came up repeatedly.

**First: scaling**

Teams struggled when their architecture started scaling across VPCs, regions, geographies, or external environments. At that point, issues like **overlapping IP ranges** started surfacing, which blocked connectivity between services that now needed to communicate. They also found it hard to decide which AWS networking service to use for a given topology. For example, the same connectivity problem could potentially be solved with VPC Peering, Transit Gateway, or Cloud WAN—but most teams did not have the expertise to choose the right one confidently.

**Second: day one (root cause)**

The root cause often started much earlier, at the initial setup stage. Many developers were not familiar with AWS networking building blocks such as VPCs, subnets, route tables, and IP planning. Instead of learning those concepts upfront, they defaulted to whatever was fastest. That helped them get started quickly, but it often led to inefficient architectures that became difficult or expensive to fix later. A common example was creating multiple VPCs with overlapping CIDR ranges using default configurations, which later prevented those environments from being connected.

**Theme**

Across both stages, the same pattern showed up: developers were trying to skip the AWS networking learning curve, and as a result they were landing on architectures that limited scalability later.

---

#### Solution direction

To solve this, I proposed abstracting networking away from the developer workflow. Instead of asking users to configure networking primitives like VPCs, subnets, and IP ranges, I designed the experience around **application-level** inputs that developers already understand.

The user flow asked:

1. Which application resources are being used, such as compute, storage, or databases  
2. Which of those resources need to be public versus private  
3. Which resources need to connect to each other, including internet, on-premises environments, and other cloud providers  
4. Whether the architecture needs to support global scale  

Based on these inputs, AWS would automatically generate the underlying network infrastructure using recommended best practices. This reduced configuration steps by roughly **80%** and compressed time-to-launch from **weeks to days**. The design also preserved flexibility: customers who wanted more control could still inspect and modify the generated setup as their needs evolved.

---

#### What I shipped in the internship

I translated this into a concrete product proposal by designing the core console flow, defining API inputs and outputs, outlining the SDK requirements, documenting the concept in a PRFAQ, and driving cross-functional buy-in across partner teams.

---

#### Impact

- **80%+** reduction in configuration steps vs. manual VPC-style setup  
- Time from intent to runnable network moved from **weeks to days**  
- Cross-functional alignment to implement  

---

#### Skills & tools

Product definition, API design, console UX, PR/FAQ, AWS VPC and connectivity (peering, TGW, Cloud WAN), IP addressing, agentic workflows, cross-functional alignment

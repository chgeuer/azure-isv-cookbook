# The technical envisioning / technical discovery session

The engineering part of an engagement usually starts with a 'technical envisioning session', during which we try to understand your system better. This session is usually time-boxed to 60 minutes, so we won't have time to go super-deep in each aspect. 

Some of our customers migrate their workloads from a different environment like AWS or on-premises datacenters to Azure, while others already have a system running on the Azure cloud, which they want to optimize. 

## Goals of the envisioning session

One goal of the 'technical envisioning session' is to convey a technical overview to us, so that your lead engineer understands the overall picture. The second goal is to break down the project down into an agreed set of discrete 'engagements'. Your lead engineer might then pull in additional engineers into these engagement.  

## Types of engagements

Each customer comes with their own sets of needs and challenges. However, there are a few typical engagement types which are common across projects and customers:

- architecture design sessions (ADS)
- architecture design review sessions (ADR)
- technology-specific deep-dives, into areas like
  - networking topology, such as VNET integration of PaaS services
  - cloud deployment, infrastructure as code (IaC), deployment mechanisms (ARM templates / Bicep, Terraform,  Pulumi, imperative scripts)
  - data warehouse design
  - DevOps
  - PowerBI
  - ...
- security reviews

## How to prepare for the initial technical envisioning

Prior to the technical envisioning session, you should prepare an architectural overview of your system. Some customers already have various representations of their system, so there's no need to generate additional documentation, others don't have any graphical representation. While there are many different ways to represent an architecture, we mainly care about a deployment diagram, which highlights interactions between the various components. 

Finding the right level of detail is the biggest challenge. Typical 'marchitecture' slides do not convey enough detail, diagrams which list IP addresses and firewall rules for all subnets certainly are too deep for an initial session.

## Architecture samples

This section provides some sample architecture diagrams we see in our customer engagements. These might help you to get a better understanding on what sort of information we try to surface during a technical envisioning session, and potentially later during architecture review sessions.

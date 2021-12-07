

## What we need from you

1. Your **current architecture diagrams** and target architecture. Ideally, please share these with me at least 2-3 days prior to the call. If you don't have diagrams, you find some examples [here](https://cookbook.azureisv.com/other-samples). Alternatively we can cover this during the technical discovery meeting. 
2. Capture, prioritize and share Azure topics / services you need our advice with. 

## Goals of the technical discovery phase

The **goals** of the technical discovery phase are the following: 

1. We gain deeper technical understanding about your solution's architecture. 
2. Mutual understanding about your current tech challenges and goals. 
3. Identification of joint engagements / areas where you need advisory from Azure Engineering, and conditions of satisfaction.  

Our work will be structured in sprints (we call them 'engagements'). Each sprint usually lasts 2-4 weeks and will be focused on a single theme.  

The **main outcome** of the initial tech discovery phase is a mutually agreed project plan, listing the sprints/engagements, with clearly identified advisory areas and conditions of success. For the concrete engagements, I will pull in subject matter experts, as needed.

### Provisional Agenda (60-90 minutes overall)

- Introduction / Who is who
- Short overview of your solution, potentially a (quick) demo
- Overview to your solution architecture diagrams
  - Application-level components
  - Physical architecture on Azure (or the current hosting environment, in case of a migration project)
    - Network topology
    - Compute tier
    - Databases and storage and what is your data classification? 
    - Requirements re: security, availability, geo-distribution, governance/regulation/compliance, service levels
- ISV business: How do you sell your solution? Via software licenses, are you offering a SaaS solution, are you allowing customers to run their solution in their own subscription, are you managing customer deployments, are you selling your solution through cloud marketplaces already?  
- In which Azure areas specifically do you need advisory from us?
- Agreeing on a discrete set of engagements where you need our help, their priority, and jointly agreed definition / condition of success. Examples could be
  - An architecture design session (in case you do not yet have an Azure architecture), and you want us to advise while you develop your architecture
  - Iterative architecture reviews (of your architecture's evolution)
  - Architecture reviews with specific focus areas, such as 'security' or 'resilience and reliability'
  - In-depth sessions for areas, such as networking, security, data migration, deployment automation, DevOps, Kubernetes
- Scheduling the next meeting(s)

### Potential topics during the session

To give your team an understanding around the level of detail we try to touch, please consider the topics below. Keep in mind that not all of them might be applicable to your unique situation: 

- Your team's cloud readiness: Does your technical team already have
  - experience on Azure, or 
  - another cloud environment (AWS, GCP), or 
  - is this your first cloud project?
- Your application's cloud readiness: Are you ...
  - building a new 'greenfield' application,
  - migrate your app from another cloud environment, or
  - migrate from an on-premises data center?
- Pain points, challenges, and issues you're currently facing during your cloud journey
- Expectations for our project
- Project's schedule and important milestones, if any
- Your functional and non-functional requirements:
  - High Availability and Resiliency: 
    - Is your application designed to run distributed across multiple availability zones?
    - Do you need to run your application across multiple Azure regions?
  - Disaster Recovery and Business Continuity
  - Cross-cloud platform portability
    - Are you following a multi-cloud strategy in which you want your application to run without major modifications across multiple environments?
    - Or are you trying to leverage (environment-specific) best-of-breed PaaS services, in order to achieve maximum development velocity?
  - Performance numbers, such as throughput, latency, or transactions/sec
  - Migration Plans (zero-downtime requirements, data migration, volume and shape of data, replication options)
  - Security (authentication and authorization, networking, ...)
  - Governance, Compliance
  - Usage pattern of the solution, e.g. are your users office workers (working nine-to-five) in a certain geography, or are consumers using your solution 24x7?
- Technology stack overview
  - Azure Services already in use
  - Programming Languages and Frameworks (C#/Java/Node/Python/Go/...)
  - Compute (IaaS/VMs, PaaS/Web, FaaS, Kubernetes)
  - Identity, Authentication and Sign-In (Azure AD B2C, Octa/Auth0, social sign-in, self-implemented, ...)
  - Operations
    - Infrastructure-as-Code (ARM/bicep templates, Terraform, imperative scripting, Chef/Puppet/Packer/...)
    - CI/CD (Azure DevOps, GitHub Actions, Jenkins, etc.)
    - Kubernetes and CNCF (NGINX, Service Mesh, Linkerd, Helm, GitOps, ...)
    - Monitoring (Log Analytics, Prometheus, etc.)
    - Application Performance Management (Application Insights, New Relic, Datadog, etc.)
  - Data
    - Relational (MSSQL/PostgreSQL/MySQL/...)
    - NoSQL (MongoDB/CassandraDB/Redis/...)
    - Big Data (data lake, DWH, ETL)
    - Messaging and eventing (Azure Service Bus, RabbitMQ, ...)
    - Event Streaming (Event Hubs, Kafka, etc.)



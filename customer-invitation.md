
# Invitation to our technical discovery session

Hi all, 

I'm happy to also welcome you to the "Azure FastTrack for ISV" program. 
You already had the initial conversation with our program management team. 
The next step to kick-off the technical workstream is the "technical discovery" session with our engineering team. 
In our joint project, I will serve as 'lead engineer', i.e. I will be your primarily entry point for technical questions, and will pull additional engineers in, if needed. 

The goal of the technical discovery session is to help me to get a deeper technical understanding of your solution's architecture, and to jointly identify the different engagements / areas where you need advisory from Azure Engineering. 

### Agenda (60-90 minutes overall)

- Introduction / Who is who
- Short overview of your solution from your customer's perspective, potentially a (quick) demo
- Overview to your solution architecture diagrams
  - Application-level components
  - Physical architecture on Azure (or the current hosting environment, in case of a migration project), incl.
    - Network topology
    - Compute tier
    - Databases and storage
    - Requirements like availability, geo-distribution, governance/regulation/compliance, service levels
- Agreeing on a discrete set of engagements where you need our help, and their priority, such as
  - An architecture design session (in case you do not yet have an Azure architecture)
  - Iterative architecture reviews (of your architecture's evolution)
  - In-depth sessions for areas like
    - networking
    - security
    - data migration
    - deployment automation, DevOpst
- Scheduling next meeting(s)

### Preparing for the session

**Solution Architecture Diagram**: Please have your solution's architecture ready to present it during tech discovery. Ideally, please share it with us in e-mail 2-3 days prior to the session. If you need more information or inspiration regarding the right level of detail, please head over to https://cookbook.azureisv.com/technical-envisioning-session for samples. 

You might also look into the following questions:

- In which technical area do you specifically need advisory from Azure Engineering?
- Your team's cloud readiness: Does your technical team already have
  - experience on Azure, or 
  - another cloud environment (AWS, GCP), or 
  - is this your first cloud project?
- Your application's cloud readiness: Are you 
  - building a new 'greenfield' application,
  - migrate your app from another cloud environment, or
  - migrate from an on-premises data center?
- Pain points, challenges, and issues you're facing during your cloud journey
- Your expectations for our project
- Your project's schedule and important milestones, if any
- Your functional and non-functional requirements:
  - High Availability and Resiliency: 
    - Can your application be deployed across multiple availability zones?
    - Do you need to run your application across multiple Azure regions?
  - Disaster Recovery and Business Continuity
  - Cross-cloud platform portability
  - Performance numbers, such as minimum throughput, maximum latency, transactions/sec, response time, etc.)
  - Security (authentication and authorization, networking, ...) 
  - Governance, Compliance
- Technology stack
  - Azure Services already in use
  - Programming Languages and Frameworks (C#/Java/Node/Python/Go/...)
  - Infrastructure-as-Code (ARM templates, Terraform, imperative scripting)
  - CI/CD (Azure DevOps, GitHub Actions, Jenkins, etc.)
  - Compute approach (IaaS/VMs, PaaS/Web, FaaS, Kubernetes)
  - Kubernetes and CNCF (NGINX, Istio, Linkerd, Helm, GitOps, ...)
  - Operating systems (Linux distro, Windows)
  - Data
    - Relational DB (SQL/PostgreSQL/MySQL/...)
    - NoSQL DB (MongoDB/CassandraDB/Redis/...)
    - Messaging and eventing (Azure Service Bus, RabbitMQ, ...)
    - Event Streaming (Event Hubs, Kafka, etc.)
    - Big Data (data lake, DWH, ETL)
  - Monitoring (Log Analytics, Prometheus, etc.)
  - Application Performance Management (Application Insights, New Relic, Datadog, etc.)

Not all of them might be applicable to your unique situation, but it would be very helpful for us if you could share these with us as well. 


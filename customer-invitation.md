
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
  - Physical architecture on Azure (or the current hosting environment, in case of a migration project)
    - Network topology
    - Compute tier
    - Databases and storage
    - Requirements re: security, availability, geo-distribution, governance/regulation/compliance, service levels
- Agreeing on a discrete set of engagements where you need our help, their priority, and jointly agreed definition / condition of success. Examples could be
  - An architecture design session (in case you do not yet have an Azure architecture), and you want us to advise while you develop your architecture
  - Iterative architecture reviews (of your architecture's evolution)
  - Architecture reviews with specific focus areas, such as 'security' or 'resilience and reliability'
  - In-depth sessions for areas, such as
    - networking
    - security
    - data migration
    - deployment automation, DevOps,
    - Kubernetes
    - ...
- Scheduling the next meeting(s)

### Preparing for the session

Please have your solution's architecture diagram ready to present it during tech discovery. Ideally, please share it with us in e-mail 2-3 days prior to the session. If you need more information or inspiration regarding the right level of detail, please head over to https://cookbook.azureisv.com/technical-envisioning-session for samples. 

You might also look into the following questions:

- In which Azure areas do you specifically need advisory from us?
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
    - Are you followint a multi-cloud strategy in which you want your application to run without major modifications across multiple environments?
    - Or are you trying to leverage (environment-specific) best-of-breed PaaS services, in order to achieve maximum development velocity?
  - Performance numbers, such as 
    - minimum throughput,
    - maximum latency,
    - transactions/sec
  - Migration Plan
    - Zero-downtime requirements? 
    - Data Migration, volume and shape of data, replication options
  - Security (authentication and authorization, networking, ...)
  - Governance, Compliance
  - Usage pattern of the solution, e.g. are your users office workers (working nine-to-five) in a certain geography, or are consumers using your solution 24x7?
- Technology stack overview
  - Azure Services already in use
  - Programming Languages and Frameworks (C#/Java/Node/Python/Go/...)
  - Compute
    - Compute approach (IaaS/VMs, PaaS/Web, FaaS, Kubernetes)
    - Operating systems (Linux distributions, Windows)
  - Operations
    - Infrastructure-as-Code
      - ARM templates, Terraform, imperative scripting
      - Chef/Puppet/Packer/...
    - CI/CD (Azure DevOps, GitHub Actions, Jenkins, etc.)
    - Kubernetes and CNCF (NGINX, Service Mesh, Linkerd, Helm, GitOps, ...)
    - Monitoring (Log Analytics, Prometheus, etc.)
    - Application Performance Management (Application Insights, New Relic, Datadog, etc.)
  - Data
    - Relational DB (SQL/PostgreSQL/MySQL/...)
    - NoSQL DB (MongoDB/CassandraDB/Redis/...)
    - Big Data (data lake, DWH, ETL)
    - Messaging and eventing (Azure Service Bus, RabbitMQ, ...)
    - Event Streaming (Event Hubs, Kafka, etc.)
  - Authentication and Sign-In (Azure AD B2C, Octa/Auth0, social sign-in, self-implemented, ...)

Not all of them might be applicable to your unique situation, but it would be very helpful for us if you could share these with us as well. 

All the very best, looking forward working with you,

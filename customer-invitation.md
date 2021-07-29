
# Invitation to our technical discovery session

Hi all, 

we're happy to welcome you to the "Azure FastTrack for ISV" program. 
You already had the initial conversation with our program management team. 
The next step to kick-off the technical workstream is the "technical discovery" session with our engineering team. 
In our joint project, I will serve as 'lead engineer', i.e. I will be your primarily entry point for technical questions, and will pull additional engineers in, if needed. 

The goal of the technical discovery session is to help me to get a deeper technical understanding of your solution's architecture, and to jointly identify the different engagements / areas where you need advisory from Azure Engineering. 

### Agenda (60-90 minutes overall)

- Introduction / Who is who
- Short overview of your solution from your customer's perspective, potentially a (quick) demo
- Overview to your solution architecture
  - Application-level components
  - Physical architecture on Azure (or the current hosting environment, in case of a migration project), incl.
    - Network topology
    - Compute tier
    - Databases and storage
    - Requirements like availability, geo-distribution, regulation and compliance, service levels
- Agreeing on a discrete set of engagements where you need our help, and their priority, such as
  - An architecture design session (in case you do not yet have an Azure architecture)
  - Iterative architecture reviews (of your architecture's evolution)
  - In-depth sessions for areas like
    - networking
    - security
    - data migration
    - deployment automation, DevOps
- Scheduling next meeting(s)

### Preparing for the session

- **Solution Architecture**: Please have your solution's architecture ready to present it during tech discovery. Ideally, please share it with us in e-mail 2-3 days prior to the session. If you need more information or inspiration regarding the right level of detail, please head over to https://cookbook.azureisv.com/technical-envisioning-session for samples. 
- **Technology Questionaire**: Please take a few minutes to fill our technology questionaire [here **Put Paolo's link in]()


- Please send your technical documentation and/or architecture diagram(s)
- Is your cloud solution
  - A new greenfield application
  - A migration from on-premises
  - A migration from another cloud platform (AWS, GCP)
- Please provide a list of your:
  - Pain points
  - Challenges
  - Issues
  - Technical goals 
  - Deadlines
  - Expectation for the engagement
  - Deadlines or time plans, if any
- Please provided your functional and non-functional requirements in terms of:
  - High Availability and intra-region resiliency across multiple availability zones
  - Disaster Recovery, Business Continuity, multiple regions 
  - Cross-cloud platform portability 
  - Speeds and feeds (e.g. transactions/sec, response time, etc.)
  - Performance SLAs in terms of throughput and latency, if any
  - Security
    - User authentication
    - Network security
    - RBAC
    - Others
  - Governance
  - Compliance

### - Technology stack used by the solution.

| Technology Area                                                                      | Technology Components |
| ------------------------------------------------------------------------------------ | --------------- |
| Azure Services used by your solution                                                 |                 |
| Programming Languages and Frameworks (C#, Python, Golang, PHP, Rust, Java, etc.)     |                 |
| Scripting Languages (Bash, PowerShell, etc.)                                         |                 |
| Infrastructure as Code (Terraform, ARM templates, etc.)                              |                 |
| CI/CD (Azure DevOps, GitHub Actions, Jenkins, etc.)                                  |                 |
| Messaging and eventing (Azure Service Bus, RabbitMQ, etc.)                           |                 |
| Kubernetes and CNCF (NGINX, Istio, Linkerd, Helm, GitOps, etc.)                      |                 |
| Event Streaming (Event Hubs, Kafka, etc.)                                            |                 |
| Relational Databases (Azure DB for PostgreSQL, etc.)                                 |                 |
| NoSQL Databases (MongoDB, CassandraDB, ArangoDB, etc.)                               |                 |
| Operating System (Linux distro, Windows)                                             |                 |
| Monitoring and Dashboarding (Log Analytics, Prometheus, etc.)                        |                 |
| Application Performance Management (Application Insights, New Relic, Datadog, etc.)  |                 |

All the very best, looking forward working with you, 

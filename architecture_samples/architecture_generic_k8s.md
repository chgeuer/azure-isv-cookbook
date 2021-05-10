### Too generic / Too little detail

The following architecture illustration conveys a few ideas, but also lacks lots of details:

![A kubernetes-based microservices architecture with databases](../img/architecture_generic_k8s.svg)

Details we get from the picture: 

- The partner plans to run services on top of Kubernetes as an orchestrator
- There will be multiple services on the Kubernetes cluster
- Some services talk to each other
- Some services store data in databases
- The databases seem to be hosted on Kubernetes as well
- Some services call out to services outside of the Kubernetes cluster

Details we miss in the picture:

- What 'application' is calling the deployment, i.e. how do users interact with the system? 
  - Is it a web-based application, where users use their browser? Is it a 'single-page application'? Server-rendered HTML?
  - Is it a 'fat client', like a Windows-application, running on the user's computer, which interacts with the system?
  - Is it a B2B-application, where your application exposes an API which is called from, and integrated, with your customed's business systems?
- How does traffic come into the application? 
  - Does the application only expose a single endpoint, or IP address? Do you need multiple IP addresses?
  - Which protocols are used, is is web-based (HTTPs) traffic, IoT (AMQP/MQTT), which transports (TCP, UDP)
  - Do you have session-affinity requirements, a.k.a. sticky sessions, where subsequent requests need to be sent to the same compute node?
- Connectivity to external systems
  - The picture just says that the application talks to 3rd party services. Which services are that?
  - When talking to 3rd party services, do you have requirements for controlling the outbound IP address? For example, some 3rd party services have to lock-down incoming traffic using IP addresses (allow-listing), so you might have to be able to control outbound IP addresses.
- High-availability
  - Do you need to run your application in multiple cloud regions, or is it sufficient to run in a single one? 
- Databases
  - Which types of databases are needed for the application? 
    - Relational databases (MS SQL, MySQL/Maria, PostgreSQL)
    - Key-value stores (Redis, Memcache)
    - Document- and other NoSQL databases (MongoDB, Cassandra, ScyllaDB)
    - Message-centric brokers (RabbitMQ, Kafka, )
    - Extensions, such as TimescaleDB
  - The picture seems to say that the database system a
- Multi-tenancy
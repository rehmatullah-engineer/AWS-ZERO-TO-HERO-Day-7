Day 1 — AWS Fundamentals
Date: 24 September 2025
Topic: Introduction to Cloud Computing on AWS
Learning focus: Cloud computing basics, deployment models, cloud types, AWS benefits, networking, pay-as-you-go pricing, and AWS global infrastructure.

Table of Contents
- 1. Why Do DevOps and Developers Need the Cloud?
- 2. Cloud Deployment Models
- 3. Cloud Types
- 4. How Does the AWS Public Cloud Work?
- 5. Key Benefits of Cloud Computing
- 6. Data and Networking in the Cloud
- 7. On-Demand and Pay-As-You-Go
- 8. AWS Global Infrastructure
- 9. Quick Revision
- 10. Summary
1. Why Do DevOps and Developers Need the Cloud?
Cloud computing helps developers and DevOps teams build, deploy, and operate applications without purchasing and maintaining all the underlying physical infrastructure themselves.
- Speed: Provision resources in minutes.
- Scalability: Scale resources up or down as demand changes.
- Reliability: Design for high availability, backups, and disaster recovery.
- Cost efficiency: Pay for resources according to the service's pricing model rather than purchasing all hardware upfront.
- Innovation: Access managed services and technologies such as AI/ML, analytics, and databases.
Example: A developer can launch a virtual server on AWS to host a web application instead of buying a physical server.
2. Cloud Deployment Models
Deployment models describe where infrastructure runs and who manages it.
Model	Description	Key point
On-premises	An organization owns or manages infrastructure in its own data center.	The organization manages hardware and maintenance.
Cloud	Resources are provided by a cloud provider over a network.	Examples include AWS services such as Amazon EC2 and Amazon S3.
Hybrid cloud	Combines on-premises infrastructure with cloud resources.	Some systems remain local while others run in the cloud.


Remember: Hybrid cloud combines on-premises and cloud environments.
3. Cloud Types
Type	Description	Typical use
Public cloud	Infrastructure is operated by a provider and services are offered to customers over a network.	AWS, Microsoft Azure, Google Cloud.
Private cloud	A cloud environment dedicated to one organization.	Organizations requiring dedicated environments or greater control.
Hybrid cloud	Connects a private or on-premises environment with public cloud services.	Workloads or data that need to operate across both environments.


Note: “Deployment models” and “cloud types” overlap in introductory material. Public, private, and hybrid are commonly used to describe cloud deployment approaches.

4. How Does the AWS Public Cloud Work?
Users connect to AWS over the internet or through a private network connection. They request resources, and AWS makes those resources available through its infrastructure.
Users
  |
  v
Internet or private connection
  |
  v
AWS Global Infrastructure
  |
  +--> Compute
  +--> Storage
  +--> Databases
  +--> Other services
Main service categories
- Compute: Runs applications and code. Example: Amazon EC2.
- Storage: Stores files, objects, backups, and other data. Example: Amazon S3.
- Databases: Stores and retrieves application data. Example: Amazon RDS.
- Other services: Networking, monitoring, analytics, security, and AI/ML.
Key idea: You request the resources your application needs, configure them, and manage them according to the chosen service and AWS responsibility model.
5. Key Benefits of Cloud Computing
- No large upfront hardware purchase: Start without first buying physical servers.
- High availability and fault tolerance: Design systems to continue operating when individual components fail.
- Global reach: Deploy applications closer to users in different geographic areas.
- Security and compliance capabilities: Use AWS security features to support requirements. You remain responsible for the security tasks assigned to you under the AWS shared responsibility model.
- Elasticity: Adjust capacity as demand changes.
- Focus on innovation: Spend less time maintaining physical infrastructure and more time developing products.
Important: Cloud services do not automatically make an application highly available or secure. These outcomes depend on architecture, configuration, monitoring, and operational practices.

6. Data and Networking in the Cloud
- Data storage: AWS services store data in infrastructure located in AWS data centers around the world.
- Networking: AWS provides services to connect users, applications, and resources.
- Access: Resources can be reached over the public internet or through private connectivity, depending on the architecture.
- Secure communication: HTTPS/TLS, VPNs, and other controls can help protect data in transit.
Examples of relevant AWS services
Service	Purpose
Amazon VPC	Creates a logically isolated virtual network for AWS resources.
Amazon Route 53	Provides DNS and domain-routing capabilities.
Elastic Load Balancing	Distributes incoming traffic across targets.
AWS Direct Connect	Provides dedicated network connectivity between an organization and AWS.
AWS Site-to-Site VPN	Establishes encrypted VPN connectivity between networks.


7. On-Demand and Pay-As-You-Go
- On-demand: Request resources when needed, subject to service availability and limits.
- Pay-as-you-go: Charges are based on usage measured under the service's pricing model.
- Flexible capacity: Scale resources to match workload requirements.
- Commitment options: Many services offer on-demand pricing; other options may require commitments and have different terms.
Example
If you run a virtual server for a short task and stop or terminate it when finished, you can reduce compute charges compared with leaving it running. Associated resources such as storage, snapshots, public IPv4 addresses, or data transfer may still incur charges.

Cost reminder: Review service pricing, configure AWS Budgets or billing alerts where appropriate, and remove resources you no longer need.
8. AWS Global Infrastructure
AWS infrastructure is organized into geographic areas and locations designed to support different workload needs.
8.1 AWS Regions
A Region is a separate geographic area where AWS operates infrastructure. Examples of Region codes include us-east-1 and ap-south-1.
- Choose a Region based on latency, service availability, cost, data residency, and business requirements.
- Not every AWS service is available in every Region.
8.2 Availability Zones (AZs)
An Availability Zone is an isolated location within an AWS Region. Regions contain multiple Availability Zones designed with independent infrastructure and failure boundaries.
- Each AZ consists of one or more data centers.
- Deploying across multiple AZs can improve resilience.
- Multi-AZ architecture must be deliberately configured; it is not automatic for every resource.
8.3 AWS Local Zones
AWS Local Zones extend selected AWS services closer to major population, industry, or technology centers.
- They can reduce latency for applications that need computing resources closer to end users.
- They are associated with a parent AWS Region.
- Available services and capabilities vary by location.
Conceptual diagram
AWS Region (for example, ap-south-1)
|
+-- Availability Zone A
|   +-- One or more data centers
|
+-- Availability Zone B
|   +-- One or more data centers
|
+-- Local Zone (where available)
    +-- Selected AWS services closer to users
Memory tip:
- Region = a geographic area.
- Availability Zone = an isolated location within a Region.
- Local Zone = selected AWS infrastructure closer to users in a metropolitan area.
9. Quick Revision
Key terms
Term	Remember
Cloud computing	Computing resources delivered as services over a network.
On-premises	Infrastructure owned or managed in an organization's own facilities.
Public cloud	Cloud services operated by a provider and offered to customers.
Private cloud	A cloud environment dedicated to one organization.
Hybrid cloud	Combination of on-premises/private infrastructure and public cloud.
Scalability	Ability to increase or decrease capacity to meet demand.
Elasticity	Ability to adjust capacity as demand changes, often dynamically.
High availability	Designing a system to minimize service interruption.
Region	Geographic AWS infrastructure area.
Availability Zone	Isolated location within an AWS Region.
Local Zone	Selected AWS infrastructure located closer to users.
Pay-as-you-go	Paying according to the applicable service usage and pricing model.


Self-check questions
1. Why might a developer choose AWS rather than purchase a physical server?
2. What is the difference between on-premises, cloud, and hybrid deployment?
3. What distinguishes a public cloud from a private cloud?
4. Name four benefits of cloud computing.
5. What are the roles of compute, storage, and database services?
6. Explain the difference between an AWS Region and an Availability Zone.
7. Why might an application use multiple Availability Zones?
8. What does pay-as-you-go mean, and why should you check related resource charges?
9. What is the purpose of an AWS Local Zone?
10. Name two ways to help secure network communication.
10. Summary
Cloud computing helps developers and DevOps teams deliver applications more quickly and flexibly by providing access to compute, storage, networking, and other services without requiring them to own all physical infrastructure. AWS offers cloud services with usage-based pricing options and global infrastructure made up of Regions, Availability Zones, and, in selected locations, Local Zones.

Main takeaway: Choose appropriate services and locations, design for security and resilience, monitor usage, and manage costs carefully.
Suggested GitHub Repository Details
- File name: README.md
- Repository title: AWS Fundamentals — Day 1 Notes
- Description: Beginner-friendly notes covering cloud computing fundamentals, deployment models, cloud types, AWS benefits, pay-as-you-go pricing, networking, and AWS global infrastructure.
- Topics: aws cloud-computing devops aws-fundamentals regions availability-zones cloud-networking cloud-learning

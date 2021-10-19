# AWS_Cloud_Practitioner_Essentials

This is a brief post of the key concepts and services from the course https://www.aws.training/Details/eLearning?id=60697 that AWS offers for free in its learning platform, that help me the most to get certified. Baisically I took these notes from the course and studied them to take the certification. 

## Module 1 - Introduction to AWS
- Cloud Computing: The on-demand delivery of IT resources over the internet with pay-as-you-go pricing.
- Cloud Computing Deployment Models:
  1. Cloud-Based
     - Run all parts of the application in the cloud.
     - Migrate existing applications to the cloud.
     - Design and build new applications in the cloud. 
  2. On-Premise (Also known as private cloud deployment)
     - Deploy resources by using virtualization and resource managment tools.
     - Increase resources utilization by using application managment and virtualization technologies.
  3. Hybrid
     - Connect cloud-based resources to on-premises infrastructures.
     - Integrate cloud-based resources with legacy IT applications
- Benefits of Cloud Computing
  1. Trade upfront expense for variable expense.
  2. Stop spending money to run and maintain data centers.
  3. Stop gessing capacity.
  4. Benefit from masive economies of scale.
  5. Increase speed and agility.
  6. Go global in minutes. 
  
  How does the scale of cloud computing help you to save costs? **R:** The aggregated cloud usage from a large number of customers results in lower pay-as-you-go prices.
  
## Module 2 - Compute in the Cloud
- Multitenacy: Sharing underlying hardware between virtual machines.
- Vertical Scaling: Increase memory and CPU.
- CaaS: Compute as a Service.

1. EC2 (Elastic Cloud Computing): Provides secure, resizable compute capacity in the cloud as Amazon EC2 instances. Instance types are optimal for different tasks.
   1. General Purpose: Provide a balance of compute, memory and networking resources. You can use them for variety of workloads, such as:
      - Application Servers.
      - Gaming Servers.
      - Backend Servers for enterprise applications.
      - Small and medium databases.
   2. Compute Optimized: 
      - High-performance web servers. 
      - Compute-intensive applications servers.
      - Dedicated gaming servers. 
      - Batch processing workloads.
   3. Memory Optmized: Are designed to deliver fast performance for workloads that process large datasets in memory.
   4. Accelerated Computing: use hardware accelerators, or coprocessors to perform some functions more efficienttly that is possible in software running on CPU's.
      - Floating-point number calculations.
      - Graphics precessing.
      - Data pattern matching.
   5. Storage Optimized: Are designed for workloads that require high, sequential read and write access to large datasets on local storage.
      - Distributed file systems.
      - Data warehousing.
      - High frequency online transaction processing.

   **IOPS:** (Input/Output operations per second) is a metric that mesures the performance of a storage device.

   - EC2 Pricing
     - On-Demand: Are ideal for short-term, irregular workloads that cannot be interrupted. The instance run continuosly until you stop them, and you pay for only the compute time you use.
     - Saving plans: Enable you to reduce your compute costs by committing to a consistent amount of compute usage for 1-year or 3-year term. This term commitment results in savings of up to 72% over On-Demand costs. Any usage up to the commitment is charged at the discounted Saving Plan rate. Any usage beyond the commitment is charged at regular On-Demand rates.
     - Reserved Instances: Are a billed discount applied to the use of On-Demand instances in your account. You can purchase Standard Reserved and Convertible Reserved Instances for 1-year or 3-year term, and schedule reserved instances for 1-year term. At the end of the reserved instance term, you can continue using the Amazon EC2 instance without interruption. However, you are charged On-Demand rates until you do one of the following:
       - Terminate the instance
       - Purchase a new reserved instance that matches the instance attributes (type, region, platform)
     - Spot Instances: Are ideal for workloads with flexible start and end times, or that can withstand interruptions. Spot instances use unused Amazon EC2 computing capacityand offer you cost savings at up to 90% off of On-Demand prices.
     - Dedicated Hosts: Are physical servers with Amazon EC2 instances capacity that is fulled dedicated to your use. You can use your existing oer-socket, per-core, or per-VM software licenses to help maintain license compliance. Dedicated Hosts are the most expensive.
    
   - Scaling Amazon EC2: Auto scaling enables you to automatically add or remove Amazon EC2 instances in response to changing application demand. You can use two approches:
     - Dynamic Scaling: Responds to changing demand.
     - Predictive Scaling: Automatically schedules the right number of EC2 instances based on predicted demand.

2. Elastic Load Balancing (ELB): Is the service that automatically distributes incoming application traffic across multiple resources, such as EC2 instances.
3. Messaging and Queuing: To help mantain application availability when a single component fails, you can design your application through a microservice approach. Two different services that facilitate application integration: Amazon Simple Notification Service (SNS) and Amazon Simple Queue Service (SQS).
   - Amazon Simple Notification Service (SNS): Is a publish/subscribe service. Using Amazon SNS topics, a publisher publishes messages to subscribers. In SNS subscribers can be web servers, email addresses, AWS lambda functions, or several other options.
   - Amazon Simple Queu Service (SQS): Is a message queuing service. You can send, store and receive messages between software components, without losing messages or requiring other services to be available. A user or service retrives a message from the queu, process it, and deletes it from the queu.
4. AWS Lambda: Is a service that lets you run code without needing to provision or manage servers. You pay only for the compute time that you consume.
   - Auto-scalable
   - Runs up to 14 min 59 secs.
5. Amazon Elastic Container Service (ECS): Is a highly scalable, high-performance container managment system that enables you to run and scale containerized applications on AWS.
6. Amazon Elastic Kubernetes Service (EKS): Is a full managed service that you can use to run kubernetes on AWS.
7. AWS Fargate: Is a serverlees compute engine for containers. It works with both Amazon ECS and Amazon EKS. Fargate manages your servers infrastructure for you.
8. Amazon Lightsail: Designed to be the easiest way to launch and manage a virtual private server. Lightsail include everything you need to jumpstart your project - a virtual machine, SDD-based storage, data transfer, DNS managment, and static IP address - for a low, predictable price.
9. AWS Batch: Dynamically provisions the optimal quantity and type of compute resources based on the volume and specific resource requirements of the batch jobs submitted. AWS Batch plans, schedules, and executes your batch computing workloads across the full range of AWS compute services and features, such as Amazon EC2 and Spot instances.
10. AWS Elastic Beanstalk: An easy-to-use service for deploying and scaling web applications and services developed with java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Ngnix, Passanger, and AWS Elastic Beanstalk automatically handles the deployment, from campacity provisioning, load balancing, and auto scaling to application heath monitoring.
11. AWS Serverless Application Repository: Enables you to quick deploy code samples components, and complete applications for common use cases such as web and mobile back-ends, event and data processing, logging, monitoring, IoT and also to publish your own applications and share them within your team, across your organization, or with the community. There is no additional charge to use the serverless Application repo, you only pay for the AWS resources used in the app you deploy.
12. ASW Outposts: Bring native AWS services, infrastructure, and operating models to virtually and data-centers, co-location space, or on-premises facility. You can use the same API's, the same tools, the same hardware, and the same functionality acress-on-premises and the cloud to deliver a truly consistent hybrid experience.
13. WMWare Cloud on AWS.

**Thitly couple architecture:** When application communicate directly.

**Loosly couple architecture:** Single Failure won't cause cascading failures.


## Module 3 - Global Infrasctructure and Reliability
- Global Infrastructure: When determining the right region for your service, data, and applications, considere the following four business factores:
  1. Compliance with data governance and legal requirements.
  2. Proximity to your customers.
  3. Available services within a Region.
  4. Pricing.
  - Availability Zones: is a single data center or a group of datacenters within a region.
- Edge Locations: is a site that Amazon-CloudFront uses to store cached copies of your content to your customer for faster delivery.

- How to Provision AWS Resources
1. AWS Managment Console
2. AWS Command Line Interface (CLI)
3. Software Development Kits (SDK's)
4. AWS Elastic Beanstalk: you provide code and configuration settings, and Elastic Beanstalk deploys the resources necessary to perform the following tasks:
   - Adjust Capacity
   - Load Balancing
   - Automatic Scaling
   - Application Health Monitoring
5. AWS Cloud Formation: you can treat your infrastructure as code, AWS Cloud Formation provisions you resources in a safe, repeatable manner, enabling you to frequently build your infrastructure and applications without having to perform manual actions or write custom scripts, it determines the rigth operations to perform when managing your stack and rolls back changes automatically if it detects errors.


## Module 4 - Networking
- Connectivity to AWS
1. Amazon Virtual Private Network (VPC): enables you to provision an isolated section of the AWS Cloud within a VPC, you can organize your resources into subnets. A subnet is a section of a VPC that can contain resources such as Amazon EC2 instances. 
2. Internet Gateway: is a connection between a VPC and th internet.
3. Virtual Private Gateway: to access private resources in a VPC, you can use a virtual private gateway. Enables you to establish a virtual private network (VPN) connection between your VPC and a private network.
4. AWS Direct Connection: enables you to establish a dedicated private connection between your datacenter and a VPC. This connection helps you to reduce network costs and increase the amount of bandwidth.
- Subnets and Network Access Control Lists
  - Network Traffic in a VPC: the VPC component that checks packet permissions for subnets is a network access control list (ACL).
  - Network Access Control Lists (ACLs): vistual firewall that controls inbound and outbound traffic at the subnet level.
    - Each AWS account includes a default network ACL.
    - By default, your account's default network ACL allows all inbound and outbound traffic.
    - All ACL's have an explicit deny rule. This rule ensures that if a packet dosen't match any of the other rules in the list, the packet is denied.
  - Stateless Packet Filtering: Network ACL's perfomr stateless packet filtering. They remember nothing and checks packets that cross the subnet boarder each way: inbound and outbound.
    - The VPC component that checks packet permissions for an Amazon EC2 instance is a security group.
  - Security Groups: is a virtual firewall that controls inbound and outbound traffic for an Amazon EC2 instance. By default a security group denies all inbound traffic and allows all outbound traffic. You can add cutom rules to configure which traffic to allow or deny.
    - If you have multiple Amazon EC2 instances within a subnet, you can associate the same security group or use different security groups for each instance.
  - Stateful Packet Filtering: security groups perform stateful packet filtering. They remember previous decisions made for incoming packets.
- Global Networking
  - Domain Name Systems (DNS): DNS resolution is the process of translating a domain name to IP address.
  - Amazon Route 53: is a DNS web service, connects users requests to infrastructure running in AWS. It can route users to infrastrucutre outside of AWS.
  
  **You can register new domain names directly in Rout53**
  
## Module 5 - Storage and Databases
- Instance Stores and Amazon Elastic Block Storage (EBS)

1. An instance store provides temporary block-level storage for an EC2 instance. Is a disk storage that is physically attached to the host computer with the following characteristics:
    1. HDD options
    2. Solid state
    3. Size up to 16 TiB

2. Amazon Elastic Block Storage (EBS): provides block-level storage volumes that you can use with EC2 instances. Because EBS volumes are for data that needs to persist, it's importatnt to backup the data (snapshots).

    **EBS snapshot is an incremental backup**

3. Amazon Simple Storage Service (S3)
  
   **When you modify a file in block storage, only the pieces that are changed are updated. When a file in object storage is modified, the entire onject is updated**
  
   **Nine 9's of durability**
 
   S3 provides object-level storage, offers unlimited storage space, the maximum file size for an object is 5TB.
   - You can set permissions to control visibility and access to it.
   - You can also use versioning feature to track changes to your objects over time.
   - S3 storage classes:
    
     With S3 you only pay for what you use, you can choose from a range of storage classes to select a fit, you will considere two factors:
     - How often you plan to retrieve your data.
     - How available you need your data to be.
     
       1. S3 standard: provides high availability for objects, it has a higher cost.
          - Designed for frequently accessed data.
          - Store data in a minimum of three availability Zones.
       2. S3 Zone-Infrequent Access (Zone-IA): ideal for infrequently accessed but requires high availability when needed. Same level of availability as S3 standard but with lower storage price.
          - Ideal for infrequently accessed data.
          - Similar to S3 standard but lower storage price and higher retrieval price.
       3. S3 One Zone-Infrequent Access (One Zone-IA)
          - Store data in a single availability zone.
          - Lower storage price than S3 Standard-IA.
       4. S3 Intelligent-Tiering:
          - Ideal for data with unknown or changing access patterns.
          - Requires a small monthly monitoring and automation fee per object.
       5. S3 Glacier:
          - Low-cost storage designed for data-archiving.
          - Able to retrieve objects within a few minutes to hours.
       6. S3 Glacier Deep Archive:
          - Lowest-cost object storage class, ideal for archiving.
          - Able to retrieve objects within 12 hours.
          
4. Amazon Elastic File System (EFS)
   - File Storage, multiple clients can access data thta is stored in shared file folders. In this approach, a storage server uses **block sotrage** with a local file system to organize files.
     Compared to block storage and objects storage, file storage is ideal for use cases in which a large number of services and resources need to access the same data at the same time.

   - Amazon EFS is a scalable file system used with AWS Cloud Services and On-premise resources.
**[REFERENCE 1]**
5. Amazon Relational Database Service (RDS)
   - RDS enables you to run relational databases in the AWS Cloud Managed services that automates tasks such as: 
     - Hardware provisioning
     - Database setup
     - Patching
     - Backups
  
   - Database Engines:
     - Postgre SQL
     - MySQL
     - Maria DB
     - Oracle
     - Microsft SQL Server
     - Amazon Aurora:
       - Compatible with MySQL and PostgreSQL. 
       - Five times faster that MySQL and three times faster than PostgreSQL. 
       - Reduce unnecesary I/O operations. 
       - Replicates six copies of your data across three availability zones. 
       - Continuosly backs up your data.
6. Amazon Dynamo DB
   - Nonrelational databases: One type of structural approach for nonrelational databases is key-value pairs. With key-value pairs, data is organized into items (keys), and items have attributes (values). You can add or remove attributes from items in the table at any time. Not every item has to have the same attributes.
   - Dynamo DB is a key-value database. It delivers single-digit millisecond performance at any scale.
     - Is serverless, which means that you do not have to provision, patch or manage servers.
     - You also do not have to install, mantain or operate software.
     - Automatically scales and mantain performance.
     - Suitable choice for use cases that require high performance while scaling.
7. Amazon Redshift
   - Datawarehousing that you can use for big data analytics. It offers the ability to collect data from many sources and helps you to understand relationships, and trends across your data.
8. AWS Database Migration Service
   - Enables you to migrate relational databases, nonrelational databases, and others types of data store.
     - The source and target database can be of the same type or different types.
     - During the migration, your source database remains operational.
     - Other uses cases:
       - Development and test database migration.
       - Database consolidation.
       - Continuos replication.
9. Additional database services
   - Amazon DocumentDB: a document database that support MongoDB workloads.
   - Amazon Neptune: a graph database service. you can use it to build and run applications that work with highly connected datasets, such as recommendations engines, fraud detection, and knowledge graphs.
   - Amazon Quantum Ledger Database (QLDB): you can use it to review a complete history of all the changes that have been made to your application data.
   - Amazon Managed Blockchain: you can use it to create and manage blockchain networks woth open-source frameworks.
   - Amazon Elastic Cache: add caching layers on top of your databases to help improve the read times of common requests. Supports Redis and MemCached.
   - Aamzon DynamoDB Accelerator (DAX): is an in-memory cache for DynamoDB, it helps to improve response times from single-digit millisecond to microseconds.

## Module 6 - Security
- Shared Responsability Model.
**[REFERENCE 2]**
- User permissions and access.
1. AWS Identity and Access Management (IAM): Gives you the flexibility to configure access based on you company's specific operational and security needs.
   - IAM user, groups, and roles.
   - IAM policies.
   - Multi-factor authentication.
2. Root user: when you create an AWS account, you begin with an identity known as the root user, it has access to all the AWS services and resources in the account.
3. IAM users: is an identity that you create in AWS, it represents the person or application that interacts with AWS services and resources. It consists of a name and credentials.
   
   **By default when you create a new IAM user, it has no permissions associated with it.**
   
4. IAM policies: is a document that allows or denies permissions to AWS services ans resources.
5. IAM group: is a collection of IAM users. When you assign an IAM policy to a group, all users in the group are granted permissions specified by the policy.
6. IAM roles: ia an identity that you can assume to gain temporary access to permissions.
   
   **Before an IAM user, application, or service can assume an IAM role, they must be granted permissions to switch to the role.**
   
- AWS Organizations
  - You can use it to consolidate multiple AWS accounts and manage within a central location.
  - You can centrally control permissions for the accounts in your organization by using service control policies (SCPs).
  - Organizations Units (OUs)
    - You can group accounts into organizations units to make it easier to manage accounts with similar business or security requirements.
  
  **Note 1: You can apply service control policies (SCPs) to the organization root, an individual member account, or an OU. An SCP affects all IAM users, groups, and roles within account, including the root user.**
  
  **Note 2: You can apply IAM policies to IAM users, groups, or roles. You cannot apply an IAM policy to the AWS account root user.**
  
- Compliance
  - AWS Artifacts: Provides on-demand access to AWS-security and comppliance reports and select online agreements.
    - AWS Artifacts Agreement: you can review, accept, and manage agreements for an individual account and for all your accounts in AWS Organizations.
    - AWS Artifacts Reports: provide compliance reports from third.party auditors.
  - Customer Compliance Center
    - Contains resources to help you learn more about AWS compliance.
- Denial-of-service attacks
  Deliberate attemp to make a website or application unavailable to users.
  
  - AWS Shield: a service that protects applications against DDoS attacks.
    - Standard: automatically protects all AWS customers at no cost, protects your AWS resources from the most common, frequently occurring types of DDoS atacks.
    - Advanced: a paid service that provides detailed attacks diagnostics and the ability to detect and mitigate sophisticated DDoS attacks-
- Additonal Security Services
1. AWS Key Managment Service (KMS)
   - Enables you to perform encryption operations through the use of cryptographic keys. 
   - You can use KMS to create, manage and use cryptographic keys.
   - You can also control the use of keys across wide range of services and in your applications.
2. AWS WAF
   - A web application firewall that let's you monitor network requests that come into your web applications
3. Amazon Inspector
   - Helps to improve security and compliance of applications by running automated security assessments. 
   - It checks applications for security vulnerabilities and deviations from security best practices.
   - Provides you with a list of security findings prioritized by severity level, including a detailed description of each security issue and a recommendation for how to fix it.   
4. Amazon Guard Duty
   - A service that provides intelligent threat detection for your AWS infrastructure and resources. Identifies threats by continuosly monitoring the network activity and account behavior within your AWS environment.

**Note 1: Identity federation allows your users to use one login (corporate & AWS).**
  
## Module 7 - Monitoring and Analytics
- Amazon CloudWatch
  A web service that enables you to monitore and manage various metrics and configure alarm actions based on data from those metrics.
  
  - CloudWatch Alarms: you can create thatautomatically perform actions if the value of your metric has gone above or below a predifined threshold.
  - CloudWatch Dashboard: enables you to access all the metrics for your resources from a single location.
  
- AWS CloudTrail
  - Records API calls for your account. The record information includes the indentity of the API caller, the time, source IP address, and more.
  
  **Events are tiplically updated in CloudTrail within 15 minutes after an API call.**
  
  - CloudTrail Insights: this optional feature allows CloudTrail to automatically detect unusual API activities.
  
  **You can filter logs to assist with operational analysis and troubleshooting.**

- AWS Trusted Advisor
  
  A web service that inspects your AWS environment and provides real-time recommendations in accordance with AWS best practices: 
  - Cost optimization
  - Performance
  - Security
  - Fault tolerance
  - Service limits
  1. Green check indicates the number of items for which it detected no problems.
  2. Orange triangle represents the number of recommended investigations.
  3. Red circle represents the number of recommended actions.

## Module 8 - Pricing and Support
- AWS Free Tier
  - Always free
  - 12 months free
  - Trials
  
  **Lambda allows 1 million free invocations per month**
  
  **S3 is free for 12 months for up to 5 GB of standard storage.**
  
  **Lightsail offers 1 month trial of up to 750 hours of usage.**
  
- AWS Pricing Concepts
  - Pay for what you use
  - Pay less when you reserve
  - Pay less with volume-based discounts when you use more
  - AWS Pricing Calculator: lets you explore AWS services and create and estimate for the cost of your use case.
  **Lambda allows 1 million free requests and up to 3.2 million seconds of compute time per month.**
  
- AWS Billing Dashboard
  - Compare current month-to-date balance with previous month, and get a forcast of the next month based on current cost.
  - View month-to-date expense by service.
  - View free tier usage by servcice.
  - View free tier usage by service.
  - Access cost explorer and create budgets.
  - Purchase and manage saving plans.

- Consolidate Billing
  - Simplifies billing process.
  - Share savings accross accounts.
  - Free feature.
  
  **Default maximum number of accounts allowed for an organization is 4.**
  
  **Ability to share bulk discount pricing, saving plans and reserved instances.**
  
- AWS Budgets
  - You can create budgets to plan your service usage, service cost, and instance reservation.
  - Updates three times a day.
  - You can also set custom alerts when your usage exceeds.

- AWS Cost Explorer
  - A tool that enables you to visualize, understand, and manage you AWS cost and usage over time.
  - Default report for your top five cost-accruing AWS services.

- AWS Support Plans
  1. Basic: 
     - Free.
     - Includes access to whitepapers.
     - Documentation.
     - Support communities.
     - Limit selection of AWS trusted Advisor checks.
     - AWS personal health dashboard.
  2. Developer: 
     - Best practices guidance.
     - Client-side diagnostic-tools.
     - Bulding-block architecture support.
  4. Business:
     - USe case guidance to identify AWS offerings, features and services.
     - All AWS trusted advisor checks.
     - Limited support for third-party software.
  6. Enterprise:
     - Application architecture guidance.
     - Infrastructure event managment.
     - Technical account manager (TAM).

  **TAM: your primary point of contact of AWS. Provide guidance, architectureal reviews, and ongoing communication with your company as you plan, deploy, and optimize your applications.**
  
  **These plans have pay-by-the-month pricing and require no long-term contracts.**

- AWS Marketplace
  - A digital catalog that includes thousands of software listings from independent software vendors. You can find, test, and buy software that runs on AWS.
  - categories:
    - Business applications.
    - IoT
    - Data & Analytics
    - ML
    - DevOps
    - Migration
    - Infrastrucutre Software
    - Security
  
## Module 9 - Migration and Innovation
- AWS Cloud Adoption Framework (CAF)
  Organize guidance into six areas of focus, called perspectives.
  - Business:
    1. Business: ensures that IT aligns with business needs.
    2. People: supports development of an organizations-wide change managment strategy for successful cloud adoption.
    3. Governance: focuses on the skills and processes to align IT strategy with business strategy.

  - Technical:
    1. Platform
    2. Security
    3. Operations

- Migration strategies
  1. Rehosting: also know as 'lift-and-shift' involves moving applications without changes.
  2. Replatforming: also know as 'lift, tinker, and shift', involves making a few cloud optimizations to realize a tangible benefit. Optimization is achived without changing the core architecture of the application.
  3. Refactoring/Re-architecting: involves reimagining how an application is architected and developed by using cloud-native features.
  4. Repurchasing: involves moving from a traditional license to a Software-as-a-Service model.
  5. Retaining: consist of keeping applications that are critical for the business in the source environment.
  6. Retiring: removing applications that are no longer needed.

- AWS Snow Family
  A collection of physical devices that help to physically transport up to exabytes of data into and out of AWS.
  - Snowcone: small, rugger, and secure edge computing and data transfer device. 2 CPUs, 4 GB of memory and 8 TB of usable storage.
  - Snowball: 
    - Edge Storage optimized: suited for large-sacle data migrations. 80 TB of hard disk drive, 40 vCPUs, 80 GiB of memory.
    - Edge Compute optimized: pwerfull computing resources. Storage 42 TB, 52 vCPUs, 208 GiB of memory.
  - Snowmobile: an exabyte-scale data transfer service used to move large amounts of data to AWS up to 100 PB.

## Module 10 - The Cloud Journey
- AWS Well-Architected Framework
  Helps you to understand how to design and operate reliable, secure, efficient, and cost-effective systems in the AWS Cloud. It provides you a way for you to consistently measure your architecture against best practices and design principles and identity areas of improvement.
  - Operational excellence
  - Security
  - Reliability
  - Performance efficiency
  - Cost optimization

- Benefits od the AWS Clud
  1. Trade upfront expense for variable expense.
  2. Benefit from massive economics of scale.
  3. Stop guessing capacity.
  4. Incrase speed and agility.
  5. Stop spending money running and maintaining data centers.
  6. Go global in minutes.

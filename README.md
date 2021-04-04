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
## Module 4 - Networking
## Module 5 - Storage and Databases
## Module 6 - Security
## Module 7 - Monitoring and Analytics
## Module 8 - Pricing and Support
## Module 9 - Migration and Innovation
## Module 10 - The Cloud Journey
## Module 11 - AWS Certified Cloud Practitioner Basics

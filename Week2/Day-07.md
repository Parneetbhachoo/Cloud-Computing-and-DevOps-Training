
# Day 07 — AWS Cloud Infrastructure and Global Architecture

**Training Date:** 08 July 2026

## 1. Overview

The seventh day of the Master Class Program on Cloud Computing and DevOps focused on cloud infrastructure, AWS pricing, global infrastructure, and essential AWS services.

The session covered how cloud providers deliver computing resources over the internet, how AWS charges for resource usage, and how its global infrastructure supports availability and scalability. The session also introduced Microsoft Project Natick, included practice questions on AWS concepts, and provided hands-on exposure to creating an AWS account and exploring the AWS Management Console.

## 2. Topics Covered

### 2.1 Cloud Infrastructure

Learned about cloud infrastructure and the fundamental components required to deliver cloud services.

The major components include:

- **Servers:** Provide computing power for running applications, processing requests, and hosting services.
- **Storage:** Stores application files, databases, backups, and other digital information.
- **Networking:** Connects computing resources and enables communication between users, applications, and services.
- **Data Centers:** Physical facilities containing servers, storage systems, networking equipment, and supporting infrastructure.

Cloud providers use these components to deliver computing resources and services over the internet.

### 2.2 AWS Pricing and the Pay-as-You-Go Model

Studied how Amazon Web Services generates revenue by charging customers for the cloud resources and services they use.

Important areas discussed included:

- **Compute:** Services such as Amazon EC2 provide virtual computing capacity, with charges depending on the selected pricing model and resource usage.
- **Storage:** Amazon S3 provides cloud object storage, with costs depending on factors such as storage class, data stored, requests, and data transfer.
- **Data Transfer:** Charges may apply to data transferred between AWS services, regions, and external networks, depending on the service and transfer path.

#### Pay-as-You-Go Pricing

The Pay-as-You-Go model allows customers to pay for cloud resources according to their usage rather than purchasing all the physical infrastructure in advance.

This model offers flexibility and can reduce upfront infrastructure costs. However, resources must be monitored carefully to avoid unnecessary expenses.

### 2.3 AWS Global Infrastructure

Learned about the components of AWS Global Infrastructure and how they support the deployment of cloud applications across different geographical locations.

#### AWS Regions

A **Region** is a geographical area where AWS operates a collection of cloud infrastructure.

Region selection can affect latency, service availability, compliance requirements, and cost.

#### Availability Zones (AZs)

An **Availability Zone** is an isolated location within an AWS Region, consisting of one or more data centers with independent infrastructure.

Deploying applications across multiple Availability Zones can improve availability and resilience if one zone experiences a failure.

#### Data Centers

Data centers are physical facilities that house servers, storage, networking equipment, and supporting systems used to operate cloud services.

#### AWS Regions in India

Studied the AWS Regions available in India:

- **Asia Pacific (Mumbai):** `ap-south-1`
- **Asia Pacific (Hyderabad):** `ap-south-2`

These Regions provide options for deploying resources closer to users in India and can help organizations meet geographical and operational requirements.

### 2.4 Important AWS Services

Explored the basic purposes of three important AWS services.

#### A. Amazon EC2 — Virtual Servers

Amazon Elastic Compute Cloud (EC2) provides virtual servers called instances.

Common uses include:

- Hosting websites and web applications.
- Running application workloads.
- Performing computing tasks.
- Deploying development and testing environments.

EC2 instances can be configured with different operating systems, instance types, storage options, and networking settings.

#### B. Amazon S3 — Cloud Storage

Amazon Simple Storage Service (S3) is an object storage service used to store and retrieve data.

Common uses include:

- Storing images and documents.
- Hosting static website files in supported configurations.
- Keeping backups and application assets.
- Storing logs and other data.

S3 organizes data into buckets containing objects. Access to stored objects can be controlled using permissions and security policies.

#### C. AWS Lambda — Serverless Computing

AWS Lambda is a serverless compute service that runs code in response to supported events or requests.

Key features include:

- Executing code without directly managing servers.
- Supporting event-driven application workflows.
- Scaling execution according to demand within service limits.
- Charging based on factors such as requests and execution duration, subject to the applicable pricing model.

Lambda allows developers to focus on application logic rather than directly managing the underlying server infrastructure.

### 2.5 Microsoft Project Natick

Discussed Microsoft Project Natick, an experimental project that investigated deploying data-center infrastructure underwater.

The project explored whether underwater data centers could provide benefits such as improved cooling, reliable operation, and proximity to coastal population centers.

It offered an example of how organizations investigate alternative approaches to data-center design and energy efficiency.

### 2.6 AWS Conceptual Questions

Practiced questions covering several AWS concepts to reinforce theoretical understanding.

Topics included:

- **Amazon CloudFront:** A content delivery network (CDN) that helps deliver content to users with reduced latency.
- **AWS Outposts:** A service that brings AWS infrastructure and services to supported on-premises environments.
- **Scaling:** Adjusting computing capacity according to workload requirements.
- **Region Selection:** Choosing a geographical AWS Region based on factors such as latency, service availability, compliance, and cost.
- **Elastic Processing:** Adapting computing resources to changing processing demands.
- **EC2 Pricing:** Understanding that instance costs depend on the selected instance, purchasing option, usage, and other applicable charges.

These questions helped reinforce the relationship between AWS services, infrastructure decisions, and cloud cost management.

## 3. Practical Implementation

### 3.1 Creating an AWS Account

Created an AWS account to begin exploring Amazon Web Services and its cloud environment.

This provided an entry point for accessing AWS services and learning how cloud resources are managed through the provider's interface.

### 3.2 Exploring the AWS Management Console

Accessed and explored the AWS Management Console, the web-based interface used to interact with AWS services.

The session introduced the console as a central place for discovering services, navigating AWS resources, and accessing service-specific configuration options.

This initial exploration provided familiarity with the AWS environment before proceeding to more advanced practical tasks.

## 4. Key Learnings

- Understood the fundamental components of cloud infrastructure, including servers, storage, networking, and data centers.
- Learned how AWS charges for compute, storage, and data transfer.
- Understood the Pay-as-You-Go pricing model.
- Distinguished between AWS Regions, Availability Zones, and data centers.
- Identified the AWS Regions located in Mumbai and Hyderabad.
- Learned the basic uses of EC2, S3, and AWS Lambda.
- Explored Microsoft Project Natick and its underwater data-center concept.
- Practiced AWS-related questions involving CloudFront, Outposts, scaling, Region selection, and EC2 pricing.
- Created an AWS account and explored the AWS Management Console.

## 5. Learning Outcome

Developed a stronger understanding of AWS cloud infrastructure, global architecture, pricing concepts, and essential cloud services. Creating an AWS account and exploring the Management Console provided initial hands-on familiarity with the AWS environment and prepared the foundation for further practical work involving cloud resource deployment and management.


# Day 08 — AWS EC2 Deployment and Nginx Web Server Hosting

**Training Date:** 09 July 2026

## 1. Overview

The eighth day of the Master Class Program on Cloud Computing and DevOps focused on deploying and managing a Linux-based virtual server using Amazon Web Services (AWS).

The session involved creating an AWS account, launching an Ubuntu EC2 instance, understanding secure SSH access, exploring AWS billing and cost management, and connecting to the cloud server using different methods. Practical work also included transferring files using SCP, installing and configuring Nginx, and hosting a sample webpage accessible through the instance's public IP address.

## 2. Topics Covered

### 2.1 AWS Account Setup

Created and configured an AWS account to access cloud computing services.

Explored the AWS environment and its role in providing computing infrastructure, storage, networking, and other cloud services.

### 2.2 Introduction to Amazon EC2

Learned about Amazon Elastic Compute Cloud (EC2), an AWS service that provides virtual servers called instances.

EC2 instances can be used to:
- Host websites and web applications.
- Run Linux or Windows workloads.
- Perform computing tasks.
- Create development and testing environments.

The configuration of an EC2 instance depends on the selected operating system image, instance type, storage, networking, and security settings.

### 2.3 Launching an Ubuntu EC2 Instance

Successfully created an EC2 instance by following the instance launch process.

The process included:

**Step 1: Selecting an Amazon Machine Image (AMI)**

Selected the Ubuntu AMI, which provides the operating system image used to create the virtual server.

**Step 2: Choosing the Instance Type**

Selected the `t3.micro` instance type to provide the virtual computing resources for the practical.

**Step 3: Creating a Key Pair**

Created and downloaded a key pair file with the `.pem` extension for SSH authentication.

A key pair consists of a public key and a private key. The public key is configured for access to the instance, while the private key is retained by the user and used to authenticate the connection.

The private key must be stored securely and should never be uploaded to a public GitHub repository.

**Step 4: Launching the Instance**

Launched the EC2 instance using the selected configuration.

**Step 5: Understanding Public Addressing**

Learned about the two addresses used to reach the instance:

- **Public IPv4 Address:** A public IP address that can be used to reach the instance when networking and security settings permit.
- **Public DNS:** A DNS hostname that can resolve to the instance's public address when the required conditions are met.

These addresses can be used to connect to the instance or access a hosted website, provided the appropriate network access is configured.

### 2.4 AWS Billing and Cost Management

Explored the AWS Billing and Cost Management dashboard to understand cloud usage and expenditure.

Learned about the importance of:
- Monitoring service usage and associated costs.
- Reviewing billing information.
- Tracking cloud resource consumption.
- Avoiding unnecessary charges by managing resources carefully.

This is important because running cloud resources can incur costs even when they are no longer actively needed.

### 2.5 Methods of Connecting to an EC2 Instance

Learned about different methods of accessing a Linux-based EC2 instance.

**A. AWS EC2 Instance Connect**

A browser-based connection method that provides terminal access to supported EC2 instances through the AWS console.

**B. Windows Command Prompt or PowerShell**

SSH can be used from Windows terminals to establish a remote connection to a Linux instance when an SSH client is available.

**C. Git Bash or Ubuntu Terminal through WSL**

Git Bash and Windows Subsystem for Linux (WSL) provide SSH-compatible command-line environments for Windows users.

These methods allow users to administer a remote Linux server without directly accessing the physical machine.

### 2.6 SSH — Secure Shell

Successfully connected to the Ubuntu EC2 instance using SSH.

SSH is a network protocol used to establish an encrypted connection to a remote system. It enables users to execute commands and manage servers remotely.

The general command format is:

```bash
ssh -i /path/to/key.pem ubuntu@<PUBLIC_IP>
```

Here:
- `-i` specifies the private key file.
- `/path/to/key.pem` represents the location of the downloaded key.
- `ubuntu` is the typical default username for Ubuntu EC2 images.
- `<PUBLIC_IP>` represents the instance's actual public IP address.

The connection also depends on the instance's security group, network configuration, and SSH service availability.

### 2.7 SCP — Secure Copy Protocol

Learned how SCP can transfer files between a local computer and a remote server over SSH.

SCP is useful for downloading logs, reports, and other files from a cloud server to a local machine.

A general example of downloading a file is:

```bash
scp -i /path/to/key.pem ubuntu@<PUBLIC_IP>:/path/to/remote-file ./local-file
```

In this command:
- The remote file path identifies the file on the EC2 instance.
- `./local-file` specifies the destination on the local machine.
- The private key is used for authentication.

### 2.8 Nginx Web Server

Learned about Nginx, an open-source web server commonly used to serve websites and static content. It can also act as a reverse proxy and load balancer.

The practical session involved installing Nginx on the Ubuntu EC2 instance, starting the service, and checking its status.

### 2.9 Hosting a Webpage on AWS EC2

Studied how a webpage can be hosted on a cloud-based Linux server by placing its files in the web server's document directory.

The default Nginx web directory used in the practical was:

```text
/var/www/html/
```

The default webpage file was:

```text
/var/www/html/index.html
```

After modifying the webpage, its content could be served by Nginx when the service was running and the required access permissions and network rules were configured.

## 3. Practical Implementation

### 3.1 Creating and Launching the EC2 Instance

- Created and configured an AWS account.
- Opened the Amazon EC2 service.
- Selected an Ubuntu AMI.
- Chose the `t3.micro` instance type.
- Created and downloaded a `.pem` key pair.
- Launched the EC2 instance.
- Identified the instance's public IPv4 address and public DNS.

### 3.2 Connecting to Ubuntu through SSH

- Explored browser-based access using EC2 Instance Connect.
- Learned about SSH access through Windows Command Prompt, PowerShell, Git Bash, and WSL.
- Successfully connected to the Ubuntu EC2 instance using SSH.
- Gained familiarity with remote command execution on a cloud server.

### 3.3 Transferring Files Using SCP

Learned how to download files from a remote cloud server to a local computer using SCP.

This introduced a practical method for transferring files securely between local systems and cloud infrastructure.

### 3.4 Installing and Starting Nginx

Installed Nginx on the Ubuntu EC2 instance using Linux command-line commands.

Started the Nginx service and verified its status to confirm that the web server was running.

### 3.5 Creating and Hosting a Sample Webpage

- Opened the default Nginx web directory.
- Modified `/var/www/html/index.html` to create a sample webpage.
- Used the running Nginx service to serve the webpage.
- Accessed the hosted webpage through the EC2 instance's public IP address in a web browser.

The successful browser access demonstrated how a cloud-hosted web server can deliver webpage content over the internet.

### 3.6 Exploring AWS Billing

Opened the AWS Billing and Cost Management dashboard to become familiar with monitoring usage and expenditure associated with cloud resources.

## 4. Key Learnings

- Understood the purpose and basic workflow of Amazon EC2.
- Learned how an Ubuntu EC2 instance is configured and launched.
- Understood the role of AMIs, instance types, and SSH key pairs.
- Learned about public IPv4 addresses and public DNS.
- Explored AWS Billing and Cost Management.
- Connected successfully to a cloud server using SSH.
- Learned the purpose of SCP for secure file transfers.
- Installed and managed the Nginx web server on Ubuntu.
- Created a sample webpage in the Nginx document root.
- Successfully accessed the hosted webpage through the EC2 instance's public IP address.
- Developed practical experience in cloud server administration and website deployment.

## 5. Learning Outcome

Successfully deployed a basic web server on AWS EC2 and hosted a sample webpage using Nginx. The session strengthened practical understanding of virtual server provisioning, SSH-based remote administration, file transfer, web server management, and cloud cost monitoring.

This experience established a foundation for further work with AWS infrastructure, cloud security, website deployment, and DevOps automation.

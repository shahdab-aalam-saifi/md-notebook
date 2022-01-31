# Introduction

## AWS History

- 2002 - Internally launched
- 2003 - Amazon infrastructure is one of their core strength. Idea to market.
- 2004 - Launched publicly with SQS
- 2006 - Re-launched publicly with SQS, S3 and EC2
- 2007 - Launched in Europe

## AWS Regions and Availability Zones (AZ)

- A *availability zone* is a facility containing multiple servers, switches, load balancing, firewall etc. connected to each other. 
- A *region* is a geographical area consisting of more than 2 availability zones connected through a link.
- *Edge locations* are the endpoints used for caching content. It consists of CloudFront, Amazon's Content Delivery Network (CDN).
- *Regional Edge cache* lies between CloudFront Origin servers and the edge locations. It has cache larger than an individual edge location. When the user requests the data, the data is no longer available at edge location. Therefore, the edge location retrieves the cached data from the regional edge cache instead of the Origin servers that have high latency.

### Region and AZ Mapping (September 2021)

![image-20210917121137377](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20210917121137377.png)

| Continent                     | Region Code      | Region Name    | No. of Availability Zones | No. of Edge Network | Regional Edge Caches |
| ----------------------------- | ---------------- | -------------- | ------------------------- | ------------------- | -------------------- |
| **North America**             |                  |                | **25**                    | **44**              | **3**                |
|                               | North Virginia   | us-east-1      | 6                         |                     | Yes                  |
|                               | Ohio             | us-east-2      | 3                         |                     | Yes                  |
|                               | North California | us-west-1      | 3                         |                     |                      |
|                               | Oregon           | us-west-2      | 4                         |                     | Yes                  |
|                               | US-East          |                | 3                         |                     |                      |
|                               | US-West          |                | 3                         |                     |                      |
|                               | Central          | ca-central-1   | 3                         |                     |                      |
| **South America**             |                  |                | **3**                     | **4**               | **1**                |
|                               | Sao Paulo        | sa-south-1     | 3                         |                     | Yes                  |
| **Europe/Middle East/Africa** |                  |                | **24**                    | **39**              | **2**                |
|                               | Frankfurt        | eu-central-1   | 3                         |                     | Yes                  |
|                               | Ireland          | eu-west-1      | 3                         |                     |                      |
|                               | Landon           | eu-west-2      | 3                         |                     | Yes                  |
|                               | Milan            | eu-south-1     | 3                         |                     |                      |
|                               | Paris            | eu-west-3      | 3                         |                     |                      |
|                               | Stockholm        | eu-north-1     | 3                         |                     |                      |
|                               | Bahrain          | me-south-1     | 3                         |                     |                      |
|                               | Cape Town        | af-south-1     | 3                         |                     |                      |
| **Asia Pacific/China**        |                  |                | **29**                    | **34**              | **5**                |
|                               | Hong Kong SAR    | ap-east-1      | 3                         |                     |                      |
|                               | Mumbai           | ap-south-1     | 3                         |                     | Yes                  |
|                               | Seoul            | ap-northeast-2 | 4                         |                     | Yes                  |
|                               | Singapore        | ap-southeast-1 | 3                         |                     | Yes                  |
|                               | Sydney           | ap-southeast-2 | 3                         |                     | Yes                  |
|                               | Tokyo            | ap-northeast-1 | 4                         |                     | Yes                  |
|                               | Osaka            | ap-northeast-3 | 3                         |                     |                      |
|                               | Beijing          |                | 3                         |                     |                      |
|                               | Ningxia          |                | 3                         |                     |                      |

### AWS Region Infrastructure

<img src="https://jayendrapatil.com/wp-content/uploads/2016/03/AWS-Global-vs-Regional-vs-AZs.png" alt="AWS Global vs Regional vs AZ" style="zoom: 25%;" />

## Features of Amazon EC2

Amazon EC2 provides the following features:

- Virtual computing environments, known as *instances*

  ![ 					Launch multiple instances from an AMI 				](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/architecture_ami_instance.png)

- Preconfigured templates for your instances, known as *Amazon Machine Images (AMIs)*, that package the bits you need for your server (including the operating system and additional software)

  ![ 				The AMI lifecycle (create, register, launch, copy, deregister). 			](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/ami_lifecycle.png)

- Various configurations of CPU, memory, storage, and networking capacity for your instances, known as *instance types*

- Secure login information for your instances using *key pairs* (AWS stores the public key, and you store the private key in a secure place)

- Storage volumes for temporary data that's deleted when you stop, hibernate, or terminate your instance, known as *instance store volumes*

- Persistent storage volumes for your data using Amazon Elastic Block Store (Amazon EBS), known as *Amazon EBS volumes*

- Multiple physical locations for your resources, such as instances and Amazon EBS volumes, known as *Regions* and *Availability Zones*

- A firewall that enables you to specify the protocols, ports, and source IP ranges that can reach your instances using *security groups*

- Static IPv4 addresses for dynamic cloud computing, known as *Elastic IP addresses*

- Metadata, known as *tags*, that you can create and assign to your Amazon EC2 resources

- Virtual networks you can create that are logically isolated from the rest of the AWS Cloud, and that you can optionally connect to your own network, known as *virtual private clouds* (VPCs)

# Identity and Access Management (IAM)

## Users and Groups

## Roles

## Permissions

> **least privilege principle** don’t give more permissions than a user needs

## Policies

## Password Policy

## Multi-Factor Authentication

### Security Tools

### Credentials Report (account-level)

### Access Advisor (user-level)

# AWS Management Console

### AWS CLI

### AWS CloudShell

### AWS SDK

# Elastic Compute Cloud (EC2)

Amazon Elastic Compute Cloud or EC2 is a web service that provides resizable compute capacity in the cloud. EC2 instances can be scaled up or scaled down as per computing requirements.

## EC2 Instance Types

### General Purpose

### Compute Optimized

### Memory Optimized

### Accelerated Computing

### Storage Optimized

## Security Groups

### Ports

| Port | Protocol  | Description                                 |
| ---- | --------- | ------------------------------------------- |
| 21   | FTP       | File Transfer Protocol                      |
| 22   | SSH, SFTP | Secure Shell, Secure File Transfer Protocol |
| 80   | HTTP      | HyperText Protocol                          |
| 443  | HTTPS     | Secure HyperText Protocol                   |
| 3389 | RDP       | Remote Desktop Protocol                     |

# Elastic Bean Stack (EBS)

## EBS Snapshot

# Amazon Machine Image (AMI)


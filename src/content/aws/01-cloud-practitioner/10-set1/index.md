---
title: "Practice Set 1"
---

Test your knowledge for the exam.

{{% question %}}
question: |
    Which components are used by an EC2 instance in a private subnet to access a public API on the internet?
explanation: |
    It requires:
    
    - [NAT Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html)
    - [Internet Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html)    
    
    And also correct Route Table routes.
answers:
    - answer: "NAT Gateway"
      correct: True
    - answer: "Internet Gateway"
      correct: True
    - answer: "Elastic Load Balancer"
    - answer: "VPC Endpoint"
    - answer: "Virtual Private Gateway"
    - answer: "AWS PrivateLink"
{{% /question %}}

{{% question %}}
question: |
    Which components are used by an EC2 instance in a private subnet to access a public API on the internet?
explanation: |
    It requires:
    
    - [NAT Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html)
    - [Internet Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html)    
    
    And also correct Route Table routes.
answers:
    - answer: "NAT Gateway"
      correct: True
    - answer: "Internet Gateway"
      correct: True
    - answer: "Elastic Load Balancer"
    - answer: "VPC Endpoint"
    - answer: "Virtual Private Gateway"
    - answer: "AWS PrivateLink"
{{% /question %}}

{{% question %}}
question: |
    Which AWS Services can run OCI containers without you having to manage any EC2's/hosts?
explanation: |
    EKS Fargate, ECS Fargate and Lambda run serverless containers. ECS Anywhere is a service to run containers outside of AWS on **hardware/VMs** you manage. ECR is storage for container images, not to run containers on.
answers:
    - answer: "EKS Fargate"
      correct: True
    - answer: "ECS Anywhere"
    - answer: "ECS Fargate"
      correct: True
    - answer: "Lambda"
      correct: True
    - answer: "ECR"
{{% /question %}}

{{% question %}}
question: |
    Which service decouples 2 services where a producer of a message sends the message to the service and the consumer of the message needs to pull the message from the service?
explanation: |
    Amazon Simple Queue Service (Amazon SQS) lets you send, store, and receive messages between software components at any volume, without losing messages or requiring other services to be available. [Source](https://aws.amazon.com/sqs/)
answers:
    - answer: "SQS"
      correct: True
    - answer: "SNS"
    - answer: "SES"
    - answer: "SSM"
{{% /question %}}

{{% question %}}
question: |
    What is a correct *name* of an Availability Zone?
explanation: |
    * **eu-west-1a** is the Availability Zone *name* which is random associated per account to AZ ID's
    * **use1-az1** is the Availability Zone *ID*
    * **us-east-1** is a Region *Code* (it misses the a, b, c suffix)
    * **Europe (Ireland)** is a Region *Name*
answers:
    - answer: "eu-west-1a"
      correct: True
    - answer: "use1-az1"
    - answer: "us-east-1"
    - answer: "Europe (Ireland)"
{{% /question %}}

{{% question %}}
question: |
    What do you need to configure on an EC2 to select an operating system?
explanation: |
    An Amazon Machine Image (AMI) is an image provided by AWS that provides the information required to launch an instance. You must specify an AMI when you launch an instance. You can launch multiple instances from a single AMI when you require multiple instances with the same configuration. You can use different AMIs to launch instances when you require instances with different configurations. [Source](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html)
answers:
    - answer: "Amazon Machine Image (AMI)"
      correct: True
    - answer: "Optical Disc Image (ISO or UDF)"
    - answer: "Operating System Version (OSV)"
    - answer: "Virtual Machine Image (VMI)"
    - answer: "Open Container Initiative (OCI)"
{{% /question %}}

{{% question %}}
question: |
    If you need to store a copy of your data in your own country where an AWS Region is not present, which service(s) could you use? (Choose all that apply)
explanation: |
    * Correct: [Outposts](https://aws.amazon.com/outposts/)
    * Correct: [Local Zone](https://aws.amazon.com/about-aws/global-infrastructure/localzones/)
    * Correct: [Snow Family](https://aws.amazon.com/snow/)
    * Incorrect: [Edge Locations](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)
    * Incorrect: [Availability Zones](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/)
answer_validation: False
answers:
    - answer: "Outposts"
      correct: True
    - answer: "Local Zone"
      correct: True
    - answer: "Snow Family"
      correct: True
    - answer: "Edge Locations"
    - answer: "Availability Zones"
{{% /question %}}

{{% question %}}
question: |
    Which of the following storage options stores the data in a single Availability Zone, supports back-up, and can be used to run the Operating System on?
explanation: |
    Amazon Elastic Block Store (Amazon EBS) is an easy-to-use, scalable, high-performance block-storage service designed for Amazon Elastic Compute Cloud (Amazon EC2). [Source](https://aws.amazon.com/ebs/)
answers:
    - answer: "EBS"
      correct: True
    - answer: "EFS"
    - answer: "Instance Storage (Ephemeral)"
    - answer: "FSx"
    - answer: "S3"
{{% /question %}}

{{% question %}}
question: |
    Which storage service stores the data across all Availability Zones in a Region, but requires a mount point in every Availability Zone for instances to connect through NFSv4?
explanation: |
    Amazon Elastic File System (EFS) provides a simple, serverless, set-and-forget elastic file system. With Amazon EFS, you can create a file system, mount the file system on an Amazon EC2 instance, and then read and write data to and from your file system. [Source](https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html)
answers:
    - answer: "EFS"
      correct: True
    - answer: "EBS"
    - answer: "S3"
    - answer: "Instance Storage (Ephemeral)"
{{% /question %}}

{{% question %}}
question: |
    Which service can be used to connect two VPCs with the least amount of steps?
explanation: |
    Correct: VPC Peering, initiate the connection on VPC A and accept the incoming peering request on B and let the VPC Peering propagate route tables.     
    Incorrect: Transit Gateway, would also be possible but requires a lot more steps compared to VPC Peering.     
    Incorrect: NAT Gateway is for public internet connectivity.     
    Services that don't exist: NAT Peering, VPC Gateway, Transit Peering.
answers:
    - answer: "VPC Peering"
      correct: True
    - answer: "NAT Peering"
    - answer: "NAT Gateway"
    - answer: "VPC Gateway"
    - answer: "Transit Gateway"
    - answer: "Transit Peering"
{{% /question %}}

{{% question %}}
question: |
    Which services can be connected to Transit Gateway?
explanation: |
    Transit Gateways connect with other Transit Gateways, VPCs, Site-to-Site VPNs, Direct Connect. The only not supported service is an Elastic IP Address (EIP), which is a public IP address.
answer_validation: False
answers:
    - answer: "Transit Gateway"
      correct: True
    - answer: "VPC"
      correct: True
    - answer: "Site-to-Site VPN"
      correct: True
    - answer: "Direct Connect"
      correct: True
    - answer: "Elastic IP Address"
{{% /question %}}

{{% question %}}
question: |
    Which service enables customers to physically connect to AWS?
explanation: |
    The AWS Direct Connect cloud service is the shortest path to your AWS resources. While in transit, your network traffic remains on the AWS global network and never touches the public internet. [Source](https://aws.amazon.com/directconnect/)
answers:
    - answer: "Direct Connect"
      correct: True
    - answer: "Site-to-Site VPN"
    - answer: "VPC Peering"
    - answer: "Network Load Balancer"
    - answer: "Global Accelerator"
{{% /question %}}

{{% question %}}
question: |
    If you want to move data from EFS to S3, which service could you use?
explanation: |
    [Source](https://repost.aws/knowledge-center/datasync-transfer-efs-s3)
answers:
    - answer: "DataSync"
      correct: True
    - answer: "AWS Backup"
    - answer: "Storage Gateway"
    - answer: "Database Migration Service (DMS)"
{{% /question %}}

{{% question %}}
question: |
    Which service can be used to offload reads from an RDS instance to save costs?
explanation: |
    ElastiCache is designed to store key-value data in memory. The key is the query, and the value the result. Aurora just another RDS instance which is the most expensive service and does not add any value. OpenSearch is also very expensive and not designed for caching queries. MemoryDB is a Redis OSS-compatible, durable, in-memory database service for ultra-fast performance.
answers:
    - answer: "Aurora"
    - answer: "OpenSearch"
    - answer: "ElastiCache"
      correct: True
    - answer: "MemoryDB"
{{% /question %}}

{{% question %}}
question: |
    Which database service is compatible with MongoDB?
explanation: |
    Amazon DocumentDB (with MongoDB compatibility) - Scale enterprise workloads with ease using a fully managed native JSON document database. [Source](https://aws.amazon.com/documentdb/)
answers:
    - answer: "DocumentDB"
      correct: True
    - answer: "DynamoDB"
    - answer: "Aurora"
    - answer: "Redshift"
    - answer: "MemoryDB"
{{% /question %}}

{{% question %}}
question: |
    What are main features of a Landing Zone?
explanation: |
    Control Tower supports creating AWS accounts, implementing security guardrails and managing access to AWS accounts. It does create a deployment pipeline for workloads. 
answers:
    - answer: "Creating AWS Accounts"
      correct: True
    - answer: "Implementing Security Guardrails"
      correct: True
    - answer: "Manage access to AWS Accounts"
      correct: True
    - answer: "Deployment Pipeline for workloads"
{{% /question %}}

{{% question %}}
question: |
    Which service can run OCI (Docker) containers? (Choose all that apply)
explanation: |
    They can all run OCI Docker containers, except for ECR because this service stores OCI images and does not run them for you.
answer_validation: False
answers:
    - answer: "ECR"
    - answer: "ECS"
      correct: True
    - answer: "Fargate"
      correct: True
    - answer: "Lambda"
      correct: True
    - answer: "App Runner"
      correct: True
{{% /question %}}

{{% question %}}
question: |
    You have built a python function that can validate server side if a JWT token is still valid. You would like to access the function on a public URL and return the response. Which service or feature does offer this functionality? (Choose all that apply)
explanation: |
    Route 53 is the only service that cannot trigger a lambda function on a URL. 
answer_validation: False
answers:
    - answer: "Route 53"
    - answer: "CloudFront Edge Functions"
      correct: True
    - answer: "API Gateway"
      correct: True
    - answer: "Lambda Function URL"
      correct: True
{{% /question %}}

{{% question %}}
question: |
    What are features of CloudFront?
explanation: |
    Securely deliver content with low latency and high transfer speeds. CloudFront cannot load balance network traffic and cannot be used as a proxy service for egress network traffic like for example [Squid](https://www.squid-cache.org/). 
answers:
    - answer: "Load Balancing Network Traffic across multiple Regions"
    - answer: "Egress proxy service with caching"
    - answer: "CloudFront can cache data close end-users"
      correct: True
    - answer: "CloudFront optimizes latency without caching"
      correct: True
{{% /question %}}

---
title: "Official Sample Questions"
---

This is a copy of the official [sample questions](https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Sample-Questions.pdf).

{{% question %}}
question: |
  Why is AWS more economical than traditional data centers for applications with varying compute workloads?
explanation: |
  The ability to launch instances on demand when needed allows users to launch and terminate instances in response to a varying workload. This is a more economical practice than purchasing enough on-premises servers to handle the peak load.
answers:
  - answer: "Amazon EC2 costs are billed on a monthly basis."
  - answer: "Users retain full administrative access to their Amazon EC2 instances."
  - answer: "Amazon EC2 instances can be launched on demand when needed."
    correct: True
  - answer: "Users can permanently run enough instances to handle peak workloads."
{{% /question %}}

{{% question %}}
question: |
  Which AWS service would simplify the migration of a database to AWS?
explanation: |
  AWS DMS helps users migrate databases to AWS quickly and securely. The source database remains fully operational during the migration, minimizing downtime to applications that rely on the database. AWS DMS can migrate data to and from most widely used commercial and open-source databases.
answers:
  - answer: "AWS Database Migration Service (AWS DMS)"
    correct: True
  - answer: "AWS Storage Gateway"
  - answer: "Amazon EC2"
  - answer: "Amazon AppStream 2.0"
{{% /question %}}

{{% question %}}
question: |
  Which AWS offering enables users to find, buy, and immediately start using software solutions in their AWS environment?
explanation: |
  AWS Marketplace is a digital catalog with thousands of software listings from independent software vendors that makes it easy to find, test, buy, and deploy software that runs on AWS.
answers:
  - answer: "AWS Marketplace"
    correct: True
  - answer: "AWS Config"
  - answer: "AWS OpsWorks"
  - answer: "AWS SDK"
{{% /question %}}

{{% question %}}
question: |
  Which AWS networking service enables a company to create a virtual network within AWS?
explanation: |
  Amazon VPC lets users provision a logically isolated section of the AWS Cloud where users can launch AWS resources in a virtual network that they define.
answers:
  - answer: "Amazon Virtual Private Cloud (Amazon VPC)"
    correct: True
  - answer: "AWS Direct Connect"
  - answer: "Amazon Route 53"
  - answer: "AWS Config"
{{% /question %}}

{{% question %}}
question: |
  Which of the following is an AWS responsibility under the AWS shared responsibility model?
explanation: |
  Maintaining physical hardware is an AWS responsibility under the AWS shared responsibility model.
answers:
  - answer: "Configuring third-party applications"
  - answer: "Maintaining physical hardware"
    correct: True
  - answer: "Securing application access and data"
  - answer: "Managing guest operating systems"
{{% /question %}}


{{% question %}}
question: |
  Which component of the AWS global infrastructure does Amazon CloudFront use to ensure low-latency delivery?
explanation: |
  To deliver content to users with lower latency, Amazon CloudFront uses a global network of points of presence (edge locations and regional edge caches) worldwide. 
answers:
  - answer: "Edge locations"
    correct: True
  - answer: "AWS Regions"
  - answer: "Availability Zones"
  - answer: "Virtual Private Cloud (VPC)"
{{% /question %}}

{{% question %}}
question: |
  How would a system administrator add an additional layer of login security to a user's AWS Management Console?
explanation: |
  Multi-factor authentication (MFA) is a simple best practice that adds an extra layer of protection on top of a username and password. With MFA enabled, when a user signs in to an AWS Management Console, they will be prompted for their username and password (the first factor: what they know), as well as for an authentication code from their MFA device (the second factor: what they have). Taken together, these multiple factors provide increased security for AWS account settings and resources.
answers:
  - answer: "Use Amazon Cloud Directory"
  - answer: "Audit AWS Identity and Access Management (IAM) roles"
  - answer: "Enable multi-factor authentication"
    correct: True
  - answer: "Enable AWS CloudTrail"
{{% /question %}}

{{% question %}}
question: |
  Which service can identify the user that made the API call when an Amazon EC2 instance is terminated?
explanation: |
  AWS CloudTrail helps users enable governance, compliance, and operational and risk auditing of their AWS accounts. Actions taken by a user, role, or an AWS service are recorded as events in CloudTrail. Events include actions taken in the AWS Management Console, AWS Command Line Interface (CLI), and AWS SDKs and APIs.
answers:
  - answer: "AWS CloudTrail"
    correct: True
  - answer: "AWS Trusted Advisor"
  - answer: "AWS X-Ray"
  - answer: "AWS Identity and Access Management (AWS IAM)"
{{% /question %}}

{{% question %}}
question: |
  Which service would be used to send alerts based on Amazon CloudWatch alarms?
explanation: |
  Amazon SNS and Amazon CloudWatch are integrated so users can collect, view, and analyze metrics for every active SNS. Once users have configured CloudWatch for Amazon SNS, they can gain better insight into the performance of their Amazon SNS topics, push notifications, and SMS deliveries.
answers:
  - answer: "Amazon Simple Notification Service (Amazon SNS)"
    correct: True
  - answer: "AWS CloudTrail"
  - answer: "AWS Trusted Advisor"
  - answer: "Amazon Route 53"
{{% /question %}}

{{% question %}}
question: |
  Where can a user find information about prohibited actions on the AWS infrastructure?
explanation: |
  The AWS Acceptable Use Policy provides information regarding prohibited actions on the AWS infrastructure. 
answers:
  - answer: "AWS Trusted Advisor"
  - answer: "AWS Identity and Access Management (IAM)"
  - answer: "AWS Billing Console"
  - answer: "AWS Acceptable Use Policy"
    correct: True
{{% /question %}}

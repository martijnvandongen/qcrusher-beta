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
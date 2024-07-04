---
title: "Official Sample Questions"
---

[Source](https://d1.awsstatic.com/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Sample-Questions.pdf)

{{% question %}}
question: |
    A company runs a public-facing three-tier web application in a VPC across multiple Availability Zones. Amazon EC2 instances for the application tier running in private subnets need to download software patches from the internet. However, the EC2 instances cannot be directly accessible from the internet. 
    
    Which actions should be taken to allow the EC2 instances to download the needed patches? (Select TWO.)
explanation: |
    A, B – A NAT gateway forwards traffic from the EC2 instances in the private subnet to the internet or other AWS services, and then sends the response back to the instances. After a NAT gateway is created, the route tables for private subnets must be updated to point internet traffic to the NAT gateway.
shuffle_answers: False
answers:
    - answer: "A) Configure a NAT gateway in a public subnet."
      correct: True
    - answer: "B) Define a custom route table with a route to the NAT gateway for internet traffic and associate it with the private subnets for the application tier."
      correct: True
    - answer: "C) Assign Elastic IP addresses to the EC2 instances."
    - answer: "D) Define a custom route table with a route to the internet gateway for internet traffic and associate it with the private subnets for the application tier."
    - answer: "E) Configure a NAT instance in a private subnet."
{{% /question %}}


---
title: "General"
---


{{% question %}}
question: |
    What are these? 

    ```
    AWS_ACCESS_KEY_ID=ASIAIOSFODNN7EXAMPLE      
    AWS_SECRET_ACCESS_KEY=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY     
    AWS_SESSION_TOKEN=AQoDYXdzEJr...     
    ```
explanation: |
    * Temporary Security Credentials can be recognized by the `AWS_SESSION_TOKEN`
    * IAM User Access Keys look similar, but don't have an `AWS_SESSION_TOKEN`
    * EC2 Key Pair [look different](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/create-key-pairs.html)
    * Root User Access Keys look similar, but don't have an `AWS_SESSION_TOKEN` and is [strongly recommended](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user_manage_add-key.html) not to use!
answers:
    - answer: "Temporary Security Credentials"
      correct: True
    - answer: "IAM User Access Keys"
    - answer: "EC2 Key Pair"
    - answer: "Root User Access Keys"
{{% /question %}}

{{% question %}}
question: |
    Which resources can assume IAM Roles? (Choose all applicable)
explanation: |
    * IAM Users, EC2 Instances, S3 Buckets, and ECS Containers can assume roles.
    * The root account [cannot](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-console.html#:~:text=You%20cannot%20switch%20roles%20if%20you%20sign%20in%20as%20the%20AWS%20account%20root%20user.%20You%20can%20switch%20roles%20when%20you%20sign%20in%20as%20an%20IAM%20user%2C%20a%20user%20in%20IAM%20Identity%20Center%2C%20a%20SAML%2Dfederated%20role%2C%20or%20a%20web%2Didentity%20federated%20role.) assume roles
answer_validation: False
answers:
    - answer: "IAM Users"
      correct: True
    - answer: "EC2 Instances"
      correct: True
    - answer: "S3 Buckets"
      correct: True
    - answer: "ECS Containers"
      correct: True
    - answer: "The Root Account"
{{% /question %}}

{{% question %}}
question: |
    Which 3 components are required for an autoscaling group to scale in or out based on load on the cluster?
explanation: |
    * The AutoScaling Group is required, without Scaling Policies it is essentially an AutoHealing Group.
    * Scaling Policies are required to increase or decrease the desired capacity with some logic.
    * CloudWatch Alarms are required to trigger Scaling Policies.
    * An AutoScaling Group is not required, because you could also have a (web) application that should scale without a Load Balancer.
    * CloudWatch Logs and CloudWatch Synthetics are other services not really involved in Auto Scaling situations. At least it not required.
answers:
    - answer: "CloudWatch Alarms"
      correct: True
    - answer: "CloudWatch Synthetics"
    - answer: "CloudWatch Logs"
    - answer: "AutoScaling Scaling Policies"
      correct: True
    - answer: "AutoScaling Group"
      correct: True
    - answer: "Application Load Balancer"
{{% /question %}}

{{% question %}}
question: |
    What are valid CloudWatch Alarm States?
explanation: |
    A metric alarm has the following possible states:     
    OK – The metric or expression is within the defined threshold.    
    ALARM – The metric or expression is outside of the defined threshold.     
    INSUFFICIENT_DATA – The alarm has just started, the metric is not available, or not enough data is available for the metric to determine the alarm state.    
    [Source](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html)
shuffle_answers: False
answers:
    - answer: "OK"
      correct: True
    - answer: "ALARM"
      correct: True
    - answer: "LOW"
    - answer: "INSUFFICIENT_DATA"
      correct: True
    - answer: "HIGH"
    - answer: "ANOMALY_DETECTED"
{{% /question %}}

{{% question %}}
question: |
    Your VPC has an Internet Gateway and has Public, Private and Isolated Subnets. You want to access SNS from an EC2 in the Isolated Subnet. Which option would you use?
explanation: |
    The isolated subnet should not be accessible from/to the internet, neither via the NAT Gateway nor the Internet Gateway. A VPC Endpoint is the solution. There are two types: Gateway Endpoint only for DynamoDB and S3, or Interface Endpoint for hundreds of AWS services. 
answers:
    - answer: "SNS Gateway Endpoint"
    - answer: "SNS Interface Endpoint"
      correct: True
    - answer: "No changes, SNS is directly accessible from VPCs"
    - answer: "No changes, SNS can be reached via the NAT Gateway and Internet Gateway"
{{% /question %}}

{{% question %}}
question: |
    Which modes are available in the AWS Storage Gateway appliance? 
explanation: |
    AWS Storage Gateway Modes are:
    
    1. Tape stores data on Glacier or S3
    2. Volume stores data in S3 which could be migrated to EBS
    3. S3 File stores data as S3 objects    
    
    [Source](https://aws.amazon.com/storagegateway/)
answers:
    - answer: "Memory Gateway"
    - answer: "Tape Gateway"
      correct: True
    - answer: "Volume Gateway"
      correct: True
    - answer: "EBS File Gateway"
    - answer: "S3 File Gateway"
      correct: True
    - answer: "S3 Glacier Gateway"
{{% /question %}}

{{% question %}}
question: |
    Some databases can work best in N groups, where each group is on different hardware, while nodes in the same group should share the same underlaying hardware. Which strategy should you use?
explanation: |
    [Source](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html)
answers:
    - answer: "EC2 Dedicated Hosts"
    - answer: "EC2 Cluster Placement Groups"
    - answer: "EC2 Partition Placement Groups"
      correct: True
    - answer: "EC2 Dedicated Instances"
    - answer: "EC2 Spread Placement Groups"
{{% /question %}}


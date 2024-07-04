---
title: "Practice Set 1"
---

{{% question %}}
question: |
    Which service would you select if you need extreme performance and a static IP address?
explanation: |
    Network Load Balancer operates at the connection level (Layer 4), routing connections to targets (Amazon EC2 instances, microservices, and containers) within Amazon VPC, based on IP protocol data. Ideal for load balancing of both TCP and UDP traffic, Network Load Balancer is capable of handling **millions of requests per second while maintaining ultra-low latencies**. Network Load Balancer is optimized to handle sudden and volatile traffic patterns while **using a single static IP address per Availability Zone**. It is integrated with other popular AWS services such as Auto Scaling, Amazon EC2 Container Service (ECS), Amazon CloudFormation, and AWS Certificate Manager (ACM).
answers:
    - answer: "Application Load Balancer"
    - answer: "Gateway Load Balancer"
    - answer: "Network Load Balancer"
      correct: True
    - answer: "Classic ELB"
    - answer: "3rd party Load Balancer from the Marketplace"
{{% /question %}}

{{% question %}}
question: |
    Your website is under attack, and you have discovered 5 IP addresses originating the attack. How could you quickly mitigate the attack?
explanation: |
    A Security Group does not support blocking ports or IP addresses, a Network ACL does.
answers:
    - answer: "Block all ports from the 5 IP addresses on the Network ACL"
      correct: True
    - answer: "Block all ports from the 5 IP addresses on the Application Load Balancer"
    - answer: "Block all ports from the 5 IP addresses on the EC2 Web Server"
    - answer: "Block all ports from the 5 IP addresses on the Security Group"
{{% /question %}}

{{% question %}}
question: |
    Where can KMS Store Encryption Keys? (Choose all that apply)
explanation: |
    KMS can store secrets in KMS, CloudHSM or an External Key Store (e.g. your own HSM on-premise)
answer_validation: False
answers:
    - answer: "KMS itself"
      correct: True
    - answer: "Secrets Manager"
    - answer: "CloudHSM"
      correct: True
    - answer: "External Key Store"
      correct: True
{{% /question %}}

{{% question %}}
question: |
    What are correct AWS Certificate Manager (ACM) service offerings? (Choose all that apply)
explanation: |
    KMS can store secrets in KMS, CloudHSM or an External Key Store (e.g. your own HSM on-premise)
answer_validation: False
answers:
    - answer: "Free Public Certificate from Amazon"
      correct: True
    - answer: "Import Self-Signed Certificates"
      correct: True
    - answer: "AWS Private Certificate Authority"
      correct: True
    - answer: "AWS Private CA Short-Lived Certificates"
      correct: True
    - answer: "Generate Self-Signed Certificates"
{{% /question %}}

{{% question %}}
question: |
    What are features of Amazon Macie? (Choose all that apply)
explanation: |
    [Source](https://aws.amazon.com/macie/features/)
answer_validation: False
answers:
    - answer: "Automatically build an interactive data map of your sensitive data in S3."
      correct: True
    - answer: "Automatic key rotation for objects stored in S3 buckets."
    - answer: "Generate findings and send to EventBridge and Security Hub for automated remediation and workflow integration."
      correct: True
    - answer: "Analyzes objects in S3 buckets, inspecting them for sensitive data such as personally identifiable information (PII)."
      correct: True
{{% /question %}}

{{% question %}}
question: |
    Which statement about S3 encryption is true?
explanation: |
    [Source](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucket-encryption.html)
answers:
    - answer: "S3 buckets have an encryption configuration which all objects inherit."
    - answer: "S3 buckets have an encryption configuration which is applied to all objects in the bucket."
    - answer: "S3 buckets have a default encryption configuration, but objects in buckets can be encrypted or not."
      correct: True
    - answer: "S3 buckets have a default encryption key, and all objects in the bucket are encrypted with the default key or another specified key."
{{% /question %}}

{{% question %}}
question: |
    Which of the following cases gives public access to an S3 object? (Choose 1 or more)
explanation: |
    Correct answer is: a and d, because all policies are collected (incl policies and ACLs). Note ACLs also do not have Deny statements, which makes c even impossible. [Source](https://aws.amazon.com/blogs/security/iam-policies-and-bucket-policies-and-acls-oh-my-controlling-access-to-s3-resources/)
answer_validation: False
answers:
    - answer: "Both the Object ACL and Bucket Policy have an Allow"
      correct: True
    - answer: "The Object ACL has an Allow, the Bucket Policy a Deny"
    - answer: "The Object ACL has a Deny, the Bucket Policy an Allow"
    - answer: "The Object ACL is not configured, the Bucket Policy has an Allow"
      correct: True
{{% /question %}}

{{% question %}}
question: |
    How does cross-region data encryption work for S3 bucket replication?
explanation: |
    Correct answer is B. C is also possible, but data must be re-encrypted. [Source1](https://docs.aws.amazon.com/AmazonS3/latest/userguide/acl-overview.html) and [Source2](https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication-walkthrough-4.html)
shuffle_answers: False
answer_validation: False
answers:
    - answer: "A) They point to the KMS key in a central region"
    - answer: "B) Both regions have their own KMS keys and data is always encrypted/decrypted with the key in the same region as the bucket"
      correct: True
    - answer: "C) They point to a KMS multi-region key and data can be replicated to any region and decrypted in any region"
    - answer: "D) It requires customer provided keys (SSE-C) and not KMS keys"
{{% /question %}}

{{% question %}}
question: |
    When you discover role session credentials were leaked, what’s the best solution to ensure the temporary credentials cannot be used? (Choose 2)
explanation: |
    [Source](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_revoke-sessions.html )
answers:
    - answer: "Click revoke active sessions in the management console"
      correct: True
    - answer: "Delete the role"
    - answer: "Detach the policies"
    - answer: "Manually add an inline policy which applies a Deny in case aws:TokenIssueTime is less than the current time."
      correct: True
{{% /question %}}

{{% question %}}
question: |
    When you discover role session credentials were leaked, what’s the best solution to ensure the temporary credentials cannot be used? (Choose 2)
explanation: |
    [Source](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_revoke-sessions.html)
answers:
    - answer: "Click revoke active sessions in the management console"
      correct: True
    - answer: "Delete the role"
    - answer: "Detach the policies"
    - answer: "Manually add an inline policy which applies a Deny in case aws:TokenIssueTime is less than the current time."
      correct: True
{{% /question %}}

{{% question %}}
question: |
    What is true about Instance Metadata Service v1 and v2? (Choose 2)
explanation: |
    [Source](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps_examples_ec2.html#example-ec2-2)
answers:
    - answer: "IMDSv2 uses session-oriented requests"
      correct: True
    - answer: "IMDSv1 is accessible from other hosts"
    - answer: "It’s possible to implement an SCP that enforces v2 only"
      correct: True
    - answer: "IMDSv1 is not available for new EC2 instances"
{{% /question %}}

{{% question %}}
question: |
    Which are AWS Control Tower behaviour options? (Choose 3)
explanation: |
    [Source](https://docs.aws.amazon.com/controltower/latest/controlreference/control-behavior.html)
answers:
    - answer: "Preventive"
      correct: True
    - answer: "Detective"
      correct: True
    - answer: "Reactive"
    - answer: "Proactive"
      correct: True
    - answer: "Block"
{{% /question %}}

{{% question %}}
question: |
    Werner created an S3 bucket with a bucket policy that allows s3:GetObject for the same Account. A user in the same account tries to access the resource but gets "Access Denied". How to fix this?
explanation: |
    [Source](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html)
answers:
    - answer: "Change s3:GetObject to all accounts and use a condition to limit access only from the same account."
    - answer: "Remove the explicit Deny statement in any of the identity based policies."
      correct: True
    - answer: "Add an Allow to any of the identity based policies."
    - answer: "Correct the bucket name in the ARN of the bucket policy."
{{% /question %}}











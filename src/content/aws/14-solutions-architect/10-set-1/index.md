---
title: "Practice Set 1"
---

{{% question %}}
question: |
    You have an FSx Windows File Server deployment in Single-AZ setup. To align with company policies, it must be migrated to Multi-AZ. What steps should you take while minimizing downtime?
explanation: |
    [Source](https://aws.amazon.com/blogs/modernizing-with-aws/automate-the-upgrade-of-an-amazon-fsx-for-windows-file-server-to-a-multi-az-deployment/)
answers:
    - answer: "Reconfigure the deployment type to Multi-AZ"
    - answer: "Create a new FSx Windows File Server in Multi-AZ and use AWS DataSync to transfer data to the new file system"
      correct: True
    - answer: "Add an instance to the current FSx Single-AZ deployment to make it Multi-AZ"
    - answer: "Take a backup of the FSx Windows File Server in Single-AZ, create a new FSx Windows File Server in Multi-AZ and restore the backup"
{{% /question %}}
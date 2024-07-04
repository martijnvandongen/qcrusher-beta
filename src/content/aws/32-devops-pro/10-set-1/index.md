---
title: "Practice Set 1"
---

{{% question %}}
question: |
    Our DynamoDB table items are 3KB in size. Your workload requires 10 reads/sec (strongly consistent) and 2 writes/sec. How much RCU and WCU should you configure on your table with pre-provisioned capacity?
explanation: |
    Write: 3 KB / 1 KB = 3 * 2 writes per second = 6 WCU    
    Eventually consistent reads below 4KB: 0.5 * 10 = 5 RCU     
    Strongly consistent reads below 4KB: 1 * 10 = 10 RCU     
    Transactional read of 8KB at 10 reads per second = 8KB / 4KB = 2 * 2 = 4 * 10 = 40 RCU     
    [Source](https://aws.amazon.com/dynamodb/pricing/provisioned/)
shuffle_answers: False
answers:
    - answer: "10 RCU 2 WCU"
    - answer: "10 RCU 6 WCU"
      correct: True
    - answer: "30 RCU 2 WCU"
    - answer: "30 RCU 6 WCU"
{{% /question %}}
+++
title = "Clean up"
date = 2022
weight = 7
chapter = false
pre = "<b>7. </b>"
+++
### Clean up resources
1. You need to go to **API Gateway**
    - Choose **students**
    - Choose **Delete**
    - Enter `confirm   ` to confirm deletion
![clean](/images/8-cleanup/clean-1.png) 
![clean](/images/8-cleanup/clean-2.png)
2. Go to **Lambda**
   - Choose function **demo**
   - Choose **Actions**
   - Choose **Delete**
   - Enter `confirm   ` to confirm deletion
![clean](/images/8-cleanup/clean-3.png)
![clean](/images/8-cleanup/clean-4.png)
3. Go to **DynamoDB table**
    - Choose **Table**
    - Choose **studentData**
    - Choose **Delete** 
![clean](/images/8-cleanup/clean-5.png)
    - Choose **Delete all CloudWatch alarms for studentData.**
    - Enter `confirm   ` to confirm deletion
![clean](/images/8-cleanup/clean-6.png)

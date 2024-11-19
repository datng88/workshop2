---
title : "Create IAM role for Lambda"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.1 </b> "
---

### Create IAM Role

1. In the **AWS Management Console**. Enter and select **IAM** in search bar
![iam-1](/images/2-Prerequiste/2.3-createrolelambda/iam-1.png)
2. In **IAM** interface. Choose **Create role**
![iam-2](/images/2-Prerequiste/2.3-createrolelambda/iam-2.png)
   - **Trusted entity type:** AWS service
   - **Use case:** Lambda
   - Select **Next**
![iam-3](/images/2-Prerequiste/2.3-createrolelambda/iam-3.png)
3. Searching *dynamodb* in the search bar > Find and select permission **AmazonDynamoDBFullAccess**
![iam-4](/images/2-Prerequiste/2.3-createrolelambda/iam-4.png)
4. In the **Name, review, and create** section:
   - **Role name:** `LambdaAccessDynamoDB`
   - Select **Create role**
![iam-4](/images/2-Prerequiste/2.3-createrolelambda/iam-5.png)
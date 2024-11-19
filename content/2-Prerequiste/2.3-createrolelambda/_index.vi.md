---
title : "Tạo IAM role cho Lambda"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.1 </b> "
---

### Tạo IAM Role

1. Trong **AWS Management Console**. Nhập và chọn **IAM** trong thanh tìm kiếm
![iam-1](/images/2-Prerequiste/2.3-createrolelambda/iam-1.png)
2. Trong giao diện **IAM**. Chọn **Create role**
![iam-2](/images/2-Prerequiste/2.3-createrolelambda/iam-2.png)
   - **Trusted entity type:** AWS service
   - **Use case:** Lambda
   - Chọn **Next**
![iam-3](/images/2-Prerequiste/2.3-createrolelambda/iam-3.png)
3. Tìm kiếm *dynamodb* trong thanh tìm kiếm > Tìm và chọn quyền **AmazonDynamoDBFullAccess**
![iam-4](/images/2-Prerequiste/2.3-createrolelambda/iam-4.png)
4. Trong phần **Name, review, and create**:
   - **Role name:** `LambdaAccessDynamoDB`
   - Chọn **Create role**
![iam-4](/images/2-Prerequiste/2.3-createrolelambda/iam-5.png)


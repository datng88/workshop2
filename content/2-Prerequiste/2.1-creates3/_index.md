---
title : "Create S3 bucket"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---
### Create S3 bucket ###
1. Firstly, you need go to **AWS Management Console** > Find **S3**
![findS3](/images/findS3.png)
2. In the **S3 interface**, select **Create bucket**
![create-S3-but](/images/create-S3-but.png)
3. In the **S3 bucket interface**, enter the following fields:
   - Bucket name: enter `demo-fdf98   `
   - Object Ownership: select **ACLs disabled (recommended)**
   - **Note**: **Bucket name** is globally unique. You need to add *-fdf98* after it that your **Bucket name** matches [the bucket naming rules.](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html?icmpid=docs_amazons3_console)
![bucket-name](/images/bucket-name.png)
4. For **Block Public Access settings for this bucket**, leave the default.
![default-access](/images/block-access.png)
5. For **Bucket Versioning**, select **Disable**.
![versionning](/images/versionning.png)
6. For **Bucket Key**, select **Disable**. Then, select **Create Bucket**
![bucket-key](/images/bucket-key.png)
---
title : "Clean up"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b>7 . </b> "
---
1. Go to **S3 interface**. 
   - Select **demo-fdf98** bucket
   - Choose **Empty**
   - Enter `permanently delete   ` to delete bucket
   - Choose **Empty**
![clean](/images/clean-1.png)
![clean](/images/clean-2.png)
2. Go to **CloudFront interface**. Choose **Disable** and choose **Disable** to confirm perspectively.
![clean](/images/clean-3.png)
![clean](/images/clean-4.png)
3. Go to **WAF interface**. 
- Choose *Limit-100-Request-Second* distribution.
- choose **Delete**
- Enter `delete   ` to confirm deletion
![clean](/images/clean-4.png)
![clean](/images/clean-5.png)

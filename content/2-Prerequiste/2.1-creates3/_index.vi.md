---
title : "Tạo S3 Bucket"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

### Tạo S3 Bucket ###
1. Trước tiên, bạn cần vào **AWS Management Console** > Tìm **S3**


![findS3](/images/findS3.png)
2. Trong **giao diện S3**, chọn **Create bucket**

![create-S3-but](/images/create-S3-but.png)

3. Trong **giao diện S3 bucket**, nhập các trường sau: 
- Bucket name: nhập `demo-fdf98   `
- Object Ownership: nhập **ACLs disabled (recommended)**
![bucket-name](/images/bucket-name.png)

**Lưu ý**: **Tên bucket** là duy nhất trên toàn cầu. Bạn cần thêm chuỗi ký tự *-fdf98* để **Tên bucket** của bạn khớp với [quy tắc đặt tên bucket.](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html?icmpid=docs_amazons3_console)

4. Đối với **Block Public Access settings for this bucket**, hãy để mặc định.
![default-access](/images/block-access.png)
5. Đối với **Bucket Versioning**, hãy chọn **Disable**.
![versionning](/images/versionning.png)
6. Đối với **Bucket Key**, hãy chọn **Disable**. Sau đó, chọn **Create Bucket**
![bucket-key](/images/bucket-key.png)

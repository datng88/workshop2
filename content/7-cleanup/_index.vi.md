---
title : "Dọn dẹp"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b>7 . </b> "
---
1. Truy cập vào **giao diện S3**.
   - Chọn bucket **demo-fdf98**
   - Chọn **Empty**
   - Nhập `permanently delete   ` để xóa bucket
   - Chọn **Empty**
![clean](/images/clean-1.png)
![clean](/images/clean-2.png)
2. Truy cập vào **giao diện CloudFront**. Chọn **Disable** và sau đó chọn **Disable** một lần nữa để xác nhận.
![clean](/images/clean-3.png)
![clean](/images/clean-4.png)
3. Truy cập vào **giao diện WAF**.
   - Chọn phân phối *Limit-100-Request-Second*
   - Chọn **Delete**
   - Nhập `delete   ` để xác nhận việc xóa
![clean](/images/clean-4.png)
![clean](/images/clean-5.png)

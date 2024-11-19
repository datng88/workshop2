+++
title = "Dọn dẹp"
date = 2022
weight = 7
chapter = false
pre = "<b>7. </b>"
+++
### Dọn dẹp tài nguyên
1. Bạn cần truy cập vào **API Gateway**
    - Chọn **students**
    - Chọn **Delete**
    - Nhập `confirm   ` để xác nhận việc xóa
![clean](/images/8-cleanup/clean-1.png) 
![clean](/images/8-cleanup/clean-2.png)
2. Truy cập vào **Lambda**
   - Chọn hàm **demo**
   - Chọn **Actions**
   - Chọn **Delete**
   - Nhập `confirm   ` để xác nhận việc xóa
![clean](/images/8-cleanup/clean-3.png)
![clean](/images/8-cleanup/clean-4.png)
3. Truy cập vào **bảng DynamoDB**
    - Chọn **Table**
    - Chọn **studentData**
    - Chọn **Delete** 
![clean](/images/8-cleanup/clean-5.png)
    - Chọn **Delete all CloudWatch alarms for studentData.**
    - Nhập `confirm   ` để xác nhận việc xóa
![clean](/images/8-cleanup/clean-6.png)
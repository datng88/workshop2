---
title : "Tạo tài nguyên"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4.2 </b> "
---
1. Đi đến phần **Resources**
   - Chọn **Create resource**
   - Bật tính năng **CORS**
![createres](/images/5-apigw/5.2-createresources/create-1.png)
2. Tạo **Resources** thành công.
![createres](/images/5-apigw/5.2-createresources/create-2.png)

3. Tiếp theo, chọn **Create method**
![createres](/images/5-apigw/5.2-createresources/create-3.png)
4. Trong phần chi tiết **Create method**:
    - **Method type:** ANY
    - **Integration type:** Lambda function
    -  **Lambda proxy integration**
    - Bật **Create method**
![api-4](/images/5-apigw/5.2-createresources/api-4.png)
5. Phương thức ANY đã được tạo thành công.
![api-5](/images/5-apigw/5.2-createresources/api-5.png)
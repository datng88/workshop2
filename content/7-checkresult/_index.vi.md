+++
title = "Kiểm tra kết quả với Postman"
date = 2022
weight = 6
chapter = false
pre = "<b>6. </b>"
+++
1. Vào chi tiết ***API:student*** > **Stages**. Bạn cần sao chép **Invoke URL**.
![api-3](/images/7-checkresult/check-1.png)
2. [Nhấn vào đây](https://www.postman.com/) để tải xuống Postman và để các thiết lập mặc định.
![api-3](/images/7-checkresult/check-3.png)
3. Mở ứng dụng **Postman**
    - Chọn phương thức **POST**
    - Dán URL của bạn vào
    - Chọn phần **Body**
    - Chọn **raw**
    - Dán đoạn mã sau vào **Body**:
```python
{
  "studentid": "345",
  "name": "Student 1",
  "class": "A",
  "age": "18"
}
```
![api-3](/images/7-checkresult/check-4.png)
4. Phản hồi đã trả về thành công.
![api-3](/images/7-checkresult/check-5.png)
5. Truy cập vào **bảng DynamoDB**, chọn **Explore items**. Bảng có một mục đã được trả về.
![api-3](/images/7-checkresult/check-6.png)
6. Quay lại ứng dụng **Postman**:
   - Chọn phương thức **GET**
   - Dán URL của bạn vào
   - Chọn phần **Params**
   - Chọn **Send**
![api-3](/images/7-checkresult/check-7.png)
7. Phản hồi đã trả về dữ liệu của bạn được lưu trong **bảng DynamoDB**
![api-3](/images/7-checkresult/check-8.png)
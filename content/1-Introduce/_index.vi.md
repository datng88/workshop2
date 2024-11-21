---
title : "Giới Thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
### Amazon DynamoDB
**Amazon DynamoDB** là một dịch vụ cơ sở dữ liệu NoSQL serverless cho phép bạn phát triển các ứng dụng hiện đại ở mọi quy mô. Là một cơ sở dữ liệu serverless, bạn chỉ trả tiền cho những gì bạn sử dụng và DynamoDB có khả năng mở rộng xuống bằng 0, không có khởi động lạnh, không có nâng cấp phiên bản, không có cửa sổ bảo trì, không cần vá lỗi, và không có thời gian bảo trì dừng hoạt động. Sử dụng DynamoDB giúp ứng dụng của bạn đạt hiệu suất cao ổn định với thông lượng và dung lượng lưu trữ gần như không giới hạn.

### Amazon API Gateway
**Amazon API Gateway** là một dịch vụ được quản lý toàn diện giúp các nhà phát triển dễ dàng tạo, xuất bản, duy trì, giám sát và bảo mật API ở mọi quy mô. API hoạt động như "cửa trước" cho ứng dụng truy cập dữ liệu, logic nghiệp vụ hoặc chức năng từ các dịch vụ backend của bạn. Với API Gateway, bạn có thể tạo các API RESTful và API WebSocket cho phép ứng dụng giao tiếp hai chiều theo thời gian thực. API Gateway hỗ trợ các ứng dụng containerized và serverless, cũng như các ứng dụng web.

### AWS Lambda
**AWS Lambda** là một dịch vụ điện toán chạy mã của bạn để phản hồi các sự kiện và tự động quản lý tài nguyên điện toán, giúp bạn nhanh chóng biến ý tưởng thành ứng dụng serverless hiện đại và sản xuất.

### Lợi ích của Kiến Trúc Này:
- Khả năng mở rộng: Tự động mở rộng với số lượng người dùng mà không cần can thiệp thủ công.
- Hiệu quả chi phí: Mô hình trả tiền theo mức sử dụng giúp giảm chi phí, đặc biệt là cho các khối lượng công việc không dự đoán được hoặc có lưu lượng thấp.
- Serverless: Toàn bộ ngăn xếp serverless với API Gateway, Lambda và DynamoDB, giúp giảm bớt gánh nặng vận hành máy chủ.
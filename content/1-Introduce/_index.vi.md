---
title : "Giới thiệu"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 1. </b> "
---
### Amazon S3
**Amazon Simple Storage Service (Amazon S3)** là dịch vụ lưu trữ đối tượng cung cấp khả năng mở rộng, tính khả dụng của dữ liệu, bảo mật và hiệu suất hàng đầu trong ngành. Dịch vụ này được thiết kế để cung cấp dung lượng lưu trữ lớn, chi phí thấp trên nhiều khu vực địa lý. Amazon S3 cung cấp cho các nhà phát triển và nhóm CNTT khả năng lưu trữ đối tượng an toàn, bền bỉ và có khả năng mở rộng cao.

### Amazon WAF
**Amazon WAF** là tường lửa ứng dụng web cho phép bạn theo dõi và quản lý các yêu cầu web được chuyển tiếp đến các tài nguyên AWS được bảo vệ. Bằng cách sử dụng AWS WAF, bạn có thể tạo các quy tắc chặn các khai thác web phổ biến (Lớp 7) như HTTP flood, SQL injection và cross site scripting (XSS).

### Amazon CloudFront
**Amazon CloudFront** là dịch vụ mạng phân phối nội dung do Amazon Web Services (AWS) cung cấp. Dịch vụ này tăng tốc độ phân phối nội dung web của bạn bằng cách lưu trữ đệm các bản sao tại các vị trí biên trên toàn thế giới. Điều này làm giảm độ trễ và cải thiện thời gian tải cho người dùng, khiến dịch vụ này trở nên lý tưởng để phân phối nội dung tĩnh và động, chẳng hạn như trang web, video và API.

Bằng cách kết hợp các dịch vụ AWS WAF và CloudFront, bạn có thể nhận được những lợi ích sau:
- **Bảo vệ vị trí biên:** CloudFront phân phối nội dung của bạn trên nhiều vị trí biên trên toàn thế giới, giúp hấp thụ và giảm thiểu các cuộc tấn công DDoS quy mô lớn bằng cách phân tán lưu lượng truy cập.
- **Bảo mật nhiều lớp:** AWS WAF cung cấp khả năng bảo vệ ở lớp ứng dụng (Lớp 7), cho phép bạn tạo các quy tắc tùy chỉnh để chặn lưu lượng truy cập độc hại
- **Hiệu quả về chi phí:** Sử dụng CloudFront với AWS WAF có thể giảm tác động về chi phí của các cuộc tấn công DDoS bằng cách giảm thiểu lượng lưu lượng truy cập tấn công đến máy chủ gốc của bạn
- **Quy tắc có thể tùy chỉnh:** AWS WAF cho phép bạn đặt các quy tắc dựa trên tỷ lệ để tự động chặn các địa chỉ IP vượt quá ngưỡng yêu cầu đã chỉ định, giúp giảm thiểu các cuộc tấn công DDoS ở lớp ứng dụng.

Tận dụng những lợi thế này, bạn có thể tăng cường bảo mật cho các ứng dụng web của mình và hợp lý hóa các quy trình quản lý.
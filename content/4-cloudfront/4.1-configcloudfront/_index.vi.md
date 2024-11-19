+++
title = "Cấu hình Amazon CloudFront"
date = 2022
weight = 4
chapter = false
pre = "<b>4.1 </b>"
+++

### Giới thiệu
1. Trong **AWS Management Console**
   - Nhập và chọn **CloudFront** trong thanh tìm kiếm
![up-cloudfront-1](/images/up-cloudfront-1.png)
   - Chọn **Create a CloudFront distribution**
![up-cloudfront-2](/images/up-cloudfront-2.png)
2. Trong giao diện **Create distribution**
   - Ở **Origin domain**, chọn **S3 bucket** bạn đã tạo trước đó.
   - Ở **Origin access**, chọn **Legacy access identities**
![setting-cloudfront-1](/images/setting-cloudfront-1.png)
   - Chọn **Create new OAI**. Giữ giá trị mặc định và chọn **Create**
![setting-cloudfront-2](/images/setting-cloudfront-2.png)
   - Ở trường **Bucket policy**, chọn **Yes, update the bucket policy** để AWS tự động cập nhật quyền truy cập cho CloudFront vào S3 bucket.
![setting-cloudfront-3](/images/setting-cloudfront-3.png)
   - Cuộn xuống gần cuối trang:
     - Ở phần **Web Application Firewall (WAF)**, chọn **Enable security protections** và **Use monitor mode**
     - Trong phần **Settings**:
       - Chọn **Use North America, Europe, Asia, Middle East, and Africa**
       - Ở phần **Default root object - optional**, nhập *index.html*
![setting-cloudfront-4](/images/setting-cloudfront-4.png)
   - **Lưu ý**: Bạn sẽ bị tính phí 0.6 USD cho 1 triệu yêu cầu và các chi phí bổ sung khác. Bạn nên xem [Giá AWS WAF](https://aws.amazon.com/waf/pricing/) để biết thêm chi tiết.
3. Đã tạo mới distribution thành công.
![setting-cloudfront-5](/images/setting-cloudfront-5.png)
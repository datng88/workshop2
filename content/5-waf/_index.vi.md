---
title: "Cấu hình AWS WAF"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: "<b>5. </b>"
---

1. Trong **AWS Management Console**, tìm **WAF**
![waf-1](/images/waf-1.png)
2. Trong panel bên trái, chọn **Web ACLs**
![waf-2](/images/waf-2.png)
3. Bạn sẽ thấy **Web ACL** đã tạo trước đó. Nhấp vào nó.
![waf-3](/images/waf-3.png)
4. Trong **Web ACL details**. Chọn **Rules** > **Add rules** > **Add my own rules and rule groups**
![waf-4](/images/waf-4.png)
5. Trong **Add rule details**
   - **Rule type**: Rule builder
   - **Name**: `Limit-100-Request-Second`
   - **Rule builder type**: Rate-based rule
   - **Rate-limiting criteria**: 100
   - **Evaluation window**: 5 minutes
   - **Request aggregation**: Source IP address
   - **Scope of inspection and rate limiting**: Consider all requests
![waf-3](/images/waf-5.png)
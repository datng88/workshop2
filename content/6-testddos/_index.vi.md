---
title: "Kiểm tra chức năng chặn DDoS của AWS WAF"
date: "`r Sys.Date()`"
weight: 6
chapter: false
pre: "<b>6. </b>"
---

### Kiểm tra chức năng chặn DDoS của AWS WAF
Trong bước cuối cùng này, chúng ta sẽ kiểm tra khả năng phòng chống DDoS của AWS WAF bằng cách sử dụng công cụ **Auto click**

1. Tải xuống [Auto click](https://download.com.vn/tai-gs-auto-clicker-85876) và mở nó.
2. Trong giao diện ứng dụng:
   - **Click repeat**: Repeat 120 times
   - **Cursor position:** Pick location
   - Di chuyển con trỏ đến nút **Reload** để lấy vị trí.
![click1](/images/click1.png)
![click2](/images/click2.png)
3. Nhấn **Start** để bắt đầu click 120 lần. Sau khi lặp lại quá trình này 2 lần, yêu cầu của tôi bị chặn.
![click4](/images/click4.png)
4. Trong bảng điều khiển, chúng ta có thể thấy có tổng cộng 278 yêu cầu, trong đó 71 yêu cầu bị chặn.
![click3](/images/click3.png)
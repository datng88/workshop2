---
title : "Testing AWS WAF DDoS Blocking"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6. </b> "
---
### Testing AWS WAF DDoS Blocking
In this final step, we test the DDoS prevention capabilities of AWS WAF using **Auto click** tool

1. Download [Auto click](https://download.com.vn/tai-gs-auto-clicker-85876) and open it
2. In application interface:
   - **Click repeat**: Repeat 120 times
   - **Cursor position:** Pick location
   - Move your cursor to **Reload** button to get location
![click1](/images/click1.png)
![click2](/images/click2.png)
3. Click **Start** to start click 120 times. After repeating this process 2 times, my resquest is block
![click4](/images/click4.png)
4. In dashboard, we can see that there were 278 requests in total, of which 71 were blocked.
![click3](/images/click3.png)
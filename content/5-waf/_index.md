---
title : "Configure AWS WAF"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 5. </b> "
---
1. In **AWS Management Console**, find **WAF**
![waf-1](/images/waf-1.png)

2. In the left panel, choose **Web ACLs**
![waf-2](/images/waf-2.png)

3. You will see **Web ACL** created previously. Then, click to it
![waf-3](/images/waf-3.png)

4. In **Web ACL details**. Choose **Rules** > **Add rules** > **Add my own rules and rule groups**
![waf-4](/images/waf-4.png)

5. In **Add rule details**
   - **Rule type**: Rule builder
   - **Name**: `Limit-100-Request-Second`
   - **Rule builder type**: Rate-based rule
   - **Rate-limiting criteria**: 100
   - **Evaluation window**: 5 minutes (300 seconds)
   - **Request aggregation**: Source IP address
   - **Scope of inspection and rate limiting**: Consider all requests
![waf-3](/images/waf-5.png)
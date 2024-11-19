---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
### Amazon S3
**Amazon Simple Storage Service (Amazon S3)** is an object storage service offering industry-leading scalability, data availability, security, and performance. It is designed for large-capacity, low-cost storage provision across multiple geographical regions. Amazon S3 provides developers and IT teams with secure, durable and highly scalable object storage.

### Amazon WAF
**Amazon WAF** is a web application firewall that lets you monitor and manage web requests that are forwarded to protected AWS resources. By using AWS WAF, you can create rules that block common web exploits (Layer 7) like HTTP floods, SQL injection and cross site scripting (XSS).

### Amazon CloudFront
**Amazon CloudFront** is a content delivery network (CDN) service provided by Amazon Web Services (AWS). It speeds up the distribution of your web content by caching copies at edge locations around the world. This reduces latency and improves load times for users, making it ideal for delivering static and dynamic content, such as websites, videos, and APIs.

By combining services AWS WAF and CloudFront, you can get the following advantages: 
- **Edge Location Protection:** CloudFront distributes your content across multiple edge locations worldwide, which helps absorb and mitigate large-scale DDoS attacks by dispersing traffic.
- **Layered Security:** AWS WAF provides protection at the application layer (Layer 7), allowing you to create custom rules to block malicious traffic
- **Cost Efficiency:** Using CloudFront with AWS WAF can reduce the cost impact of DDoS attacks by minimizing the amount of attack traffic that reaches your origin servers
- **Customizable Rules:** AWS WAF allows you to set rate-based rules to automatically block IP addresses that exceed a specified request threshold, helping to mitigate application layer DDoS attacks.
  
Leveraging these advantages, you can enhance the security of your web applications and streamline management processes.
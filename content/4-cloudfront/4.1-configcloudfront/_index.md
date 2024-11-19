+++
title = "Config Amazon CloudFront"
date = 2022
weight = 4
chapter = false
pre = "<b>4.1 </b>"
+++

#### Introduce
1. In the **AWS Management Console**. Enter and select **CloudFront** in search bar
![up-cloudfront-1](/images/up-cloudfront-1.png)

- Select **Create a CloudFront distribution**
![up-cloudfront-2](/images/up-cloudfront-2.png)

2. In the **Create distribution** interface
   - In the **Origin domain**, select the **S3 bucket** you created previously.
   - In the **Origin access**, select **Legacy access identities**
![setting-cloudfront-1](/images/setting-cloudfront-1.png)
   - Select **Create new OAI**. Keep default value and select **Create**
![setting-cloudfront-2](/images/setting-cloudfront-2.png)
   - In the **Bucket policy** field, select **Yes, update the bucket policy** to let AWS automatically update the permission for CloudFront to access into the S3 bucket
![setting-cloudfront-3](/images/setting-cloudfront-3.png)
   - Scroll down near the bottom of the page:
     - In **Web Application Firewall (WAF)** section, select **Enable security protections** and **Use monitor mode**
     - In **Settings** section:
       - Select **Use North America, Europe, Asia, Middle East, and Africa**
       - In the **Default root object - optional section**, enter *index.html*

![setting-cloudfront-4](/images/setting-cloudfront-4.png)
  - **Note**: You will be charged $0.6 for 1 million requests and other additional fees. You should view [AWS WAF pricing](https://aws.amazon.com/waf/pricing/)  for more details.
3. Successfully created new distribution.
![setting-cloudfront-5](/images/setting-cloudfront-5.png)
  
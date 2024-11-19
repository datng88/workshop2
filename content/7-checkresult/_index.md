+++
title = "Check result with Postman"
date = 2022
weight = 6
chapter = false
pre = "<b>6. </b>"
+++
1. Go to ***API:student*** details > **Stages**. You need to copy **Invoke URL**.
![api-3](/images/7-checkresult/check-1.png)
2. [Click here](https://www.postman.com/) to download Postman and leave settings by default
![api-3](/images/7-checkresult/check-3.png)
3. Open **Postman** application
    - Choose **POST** method
    - Paste your URL
    - Choose **Body** section
    - Choose **raw**
    - Paste code following into **Body**:
```python
{
  "studentid": "345",
  "name": "Student 1",
  "class": "A",
  "age": "18"
}
```
![api-3](/images/7-checkresult/check-4.png)
4. The response returned successfully.
![api-3](/images/7-checkresult/check-5.png)
5. Go to **DynamoDB table**, choose **Explore items**. The table has one item returned.
![api-3](/images/7-checkresult/check-6.png)
6. Back to **Postman** application:
   - Choose **GET method**
   - Paste your URL
   - Choose **Params** section
   - Choose **Send**
![api-3](/images/7-checkresult/check-7.png)
7. The respone returned your data saved in **DynamoDB table**
![api-3](/images/7-checkresult/check-8.png)
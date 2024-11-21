+++
title = "Tạo hàm"
date = 2022
weight = 5
chapter = false
pre = "<b>5.1 </b>"
+++

1. Trong **AWS Management Console**. Nhập và chọn **Lambda** trong thanh tìm kiếm
![lambda-1](/images/6-lambda/6.1-createfunction/lambda-1.png)
2. Trong mục **Create a function**:
   - **Function type:** Author from scratch
   - **Function name:** `demo              `
   - **Runtime**: Python 3.11
   - Chọn **Create function**   
   - **Excution role:** Use an existing role (LambdaAccessDynamoDB)
![lambda-2](/images/6-lambda/6.1-createfunction/lambda-2.png)
3. Trong **Code source**. Xóa code cũ và nhập:

```python
import json
import boto3
import logging

# Khởi tạo logger và đặt mức độ log là INFO
logger = logging.getLogger()
logger.setLevel(logging.INFO)

# Kết nối với dịch vụ DynamoDB
dynamodb = boto3.resource('dynamodb')

# Hàm chính cho AWS Lambda
def lambda_handler(event, context):
    data = {'Items': 'Bad Request'}
    statusCode = 200

    path = event['path']
    httpMethod = event['httpMethod']

    table = dynamodb.Table('studentData')

    if httpMethod == 'GET' and path == '/students':
        data = table.scan()
    elif httpMethod == 'POST' and path == '/students':
        if event['body'] is not None:
            body = json.loads(event['body'])
            table.put_item(
                Item={
                    'studentid': body['studentid'],
                    'name': body['name'],
                    'age': body['age'],
                    'class': body['class']
                }
            )
            data = {'Items': 'Student Created Successfully'}
        else:
            data = {'Items': 'Invalid Payload'}
            statusCode = 400
    else:
        statusCode = 400

    response = {
        'statusCode': statusCode,
        'body': json.dumps(data['Items']),
        'headers': {'Content-Type': 'application/json'},
    }

    return response
```
4. Chọn **Deploy**
![lambda-3](/images/6-lambda/6.1-createfunction/lambda-3.png)
5. Hàm của bạn đã được triển khai thành công.
![lambda-3](/images/6-lambda/6.1-createfunction/lambda-4.png)
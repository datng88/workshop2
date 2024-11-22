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

# Khởi tạo một logger và đặt mức log là INFO
logger = logging.getLogger()
logger.setLevel(logging.INFO)

# Kết nối tới dịch vụ DynamoDB
dynamodb = boto3.resource('dynamodb')

# Hàm xử lý chính cho AWS Lambda
def lambda_handler(event, context):
    # Dữ liệu phản hồi mặc định
    data = {
        'Items': 'Yêu cầu không hợp lệ'
    }
    statusCode = 200  # Mã trạng thái HTTP mặc định là 200 (OK)

    # Trích xuất đường dẫn và phương thức HTTP từ đối tượng event
    path = event['path']
    httpMethod = event['httpMethod']

    # Kết nối tới bảng DynamoDB có tên 'studentData'
    table = dynamodb.Table('studentData')

    # Xử lý các yêu cầu GET tới đường dẫn '/students'
    if httpMethod == 'GET' and path == '/students':
        # Sử dụng phương thức scan() để lấy tất cả các mục từ bảng
        data = table.scan()
    
    # Xử lý các yêu cầu POST tới đường dẫn '/students'
    elif httpMethod == 'POST' and path == '/students':
        # Kiểm tra nếu thân yêu cầu không rỗng
        if event['body'] is not None:
            # Phân tích chuỗi JSON trong thân yêu cầu thành một dictionary trong Python
            body = json.loads(event['body'])
            
            # Chèn một mục mới vào bảng 'studentData'
            table.put_item(
                Item={
                    'studentid': body['studentid'],    # ID sinh viên duy nhất
                    'name': body['name'],       # Tên sinh viên
                    'age': body['age'],         # Tuổi sinh viên
                    'class': body['class']      # Lớp của sinh viên
                }
            )
            # Cập nhật dữ liệu phản hồi để chỉ ra thành công
            data = {
                'Items': 'Student Created Successfully'
            }
        else:
            # Xử lý trường hợp thân yêu cầu bị thiếu hoặc không hợp lệ
            data = {
                'Items': 'Invalid Payload'
            }
            statusCode = 400  # Đặt mã trạng thái HTTP là 400 (Yêu cầu không hợp lệ)
    else:
        # Xử lý bất kỳ yêu cầu không được hỗ trợ nào
        statusCode = 400  # Đặt mã trạng thái HTTP là 400 (Yêu cầu không hợp lệ)

    # Xây dựng phản hồi HTTP để trả về cho client
    response = {
        'statusCode': statusCode,                 # Mã trạng thái HTTP
        'body': json.dumps(data['Items']),        # Thân phản hồi dưới dạng chuỗi JSON
        'headers': {
            'Content-Type': 'application/json',   # Chỉ định rằng loại nội dung của phản hồi là JSON
        },
    }

    # Trả về phản hồi đã xây dựng
    return response
```
4. Chọn **Deploy**
![lambda-3](/images/6-lambda/6.1-createfunction/lambda-3.png)
5. Hàm của bạn đã được triển khai thành công.
![lambda-3](/images/6-lambda/6.1-createfunction/lambda-4.png)

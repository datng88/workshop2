+++
title = "Create the fuction"
date = 2022
weight = 5
chapter = false
pre = "<b>5.1 </b>"
+++

1. In the **AWS Management Console**. Enter and select **Lambda** in search bar
![lambda-1](/images/6-lambda/6.1-createfunction/lambda-1.png)
2. In the **Create a fuction** section
   - **Function type:** Author from scratch
   - **Function name:** `demo    `
   - **Runtime**: Python 3.11
   - Select **Create function**   
   - **Excution role:** Use an existing role (LambdaAccessDynamoDB)
![lambda-2](/images/6-lambda/6.1-createfunction/lambda-2.png)
3. In the **Code source**. Delete the old code and enter:

```python
import json
import boto3
import logging

# Initialize a logger and set the log level to INFO
logger = logging.getLogger()
logger.setLevel(logging.INFO)

# Connect to the DynamoDB service
dynamodb = boto3.resource('dynamodb')

# Main handler function for AWS Lambda
def lambda_handler(event, context):
    # Default response data
    data = {
        'Items': 'Bad Request'
    }
    statusCode = 200  # Default HTTP status code is 200 (OK)

    # Extract the path and HTTP method from the event object
    path = event['path']
    httpMethod = event['httpMethod']

    # Connect to the DynamoDB table named 'studentData'
    table = dynamodb.Table('studentData')

    # Handle GET requests to the '/students' path
    if httpMethod == 'GET' and path == '/students':
        # Use the scan() method to retrieve all items from the table
        data = table.scan()
    
    # Handle POST requests to the '/students' path
    elif httpMethod == 'POST' and path == '/students':
        # Check if the request body is not empty
        if event['body'] is not None:
            # Parse the JSON string in the request body to a Python dictionary
            body = json.loads(event['body'])
            
            # Insert a new item into the 'studentData' table
            table.put_item(
                Item={
                    'studentid': body['studentid'],    # Unique student ID
                    'name': body['name'],       # Student's name
                    'age': body['age'],         # Student's age
                    'class': body['class']      # Student's class
                }
            )
            # Update response data to indicate success
            data = {
                'Items': 'Student Created Successfully'
            }
        else:
            # Handle case where the request body is missing or invalid
            data = {
                'Items': 'Invalid Payload'
            }
            statusCode = 400  # Set HTTP status code to 400 (Bad Request)
    else:
        # Handle any unsupported requests
        statusCode = 400  # Set HTTP status code to 400 (Bad Request)

    # Construct the HTTP response to return to the client
    response = {
        'statusCode': statusCode,                 # HTTP status code
        'body': json.dumps(data['Items']),        # Response body as a JSON string
        'headers': {
            'Content-Type': 'application/json',   # Specify that the response content type is JSON
        },
    }

    # Return the constructed response
    return response
```
4. Select **Deploy**
![lambda-3](/images/6-lambda/6.1-createfunction/lambda-3.png)
5. Your function deployed successfully.
![lambda-3](/images/6-lambda/6.1-createfunction/lambda-4.png)

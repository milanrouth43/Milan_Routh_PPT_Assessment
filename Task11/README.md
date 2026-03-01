# Task 11: S3 Upload Email Notification using Lambda and SNS

## Objective
To implement an event-driven serverless architecture that automatically notifies administrators via email whenever a new object is uploaded to a specific Amazon S3 bucket.

## Implementation Steps

### 1. Simple Notification Service (SNS) Configuration
- Created a Standard SNS Topic named `S3-Upload-Alerts`.
- Created an Email subscription for the topic and confirmed the subscription via the confirmation email sent to the specified address.

### 2. Identity and Access Management (IAM)
- Provisioned a custom IAM Role for the Lambda execution environment.
- Attached `AmazonS3ReadOnlyAccess` (to read the event details) and `AmazonSNSFullAccess` (to publish messages to the topic) policies to the role.

### 3. AWS Lambda Function Deployment
- Created a Lambda function using the Python runtime.
- Assigned the custom IAM Role to the function to grant necessary permissions.
- Authored a Python script using the `boto3` library to parse the incoming S3 event payload, extract the bucket name and object key, and publish a formatted message to the SNS Topic ARN.

### 4. Event Trigger Configuration
- Configured an S3 Event Notification trigger directly on the Lambda function.
- Set the trigger to monitor `s3:ObjectCreated:*` events (PUT, POST, COPY) within the target bucket.

### 5. Validation
- Uploaded a test file to the target S3 bucket.
- Successfully received the automated email notification containing the exact file name and bucket name.

## Proofs of Completion
- sns_confirmed.png: Screenshot of the SNS console showing the email subscription in a 'Confirmed' status.
- lambda_trigger.png: Screenshot of the Lambda console showing the S3 event trigger successfully attached.
- email_received.png: Screenshot of the final email notification received in the inbox demonstrating the successful execution of the event-driven workflow.
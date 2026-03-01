# Task 13: Start/Stop EC2 using Lambda + API Gateway

## Objective
To learn serverless automation and API integration by using AWS API Gateway to trigger a Lambda function that controls the state (Start/Stop) of an EC2 instance.

## Implementation Steps

### 1. IAM Role Configuration
- Created a custom IAM Role for AWS Lambda.
- Attached the `AmazonEC2FullAccess` policy to grant the Lambda function the necessary permissions to modify EC2 instance states.

### 2. Lambda Function Deployment
- Provisioned a new Lambda function using the Python 3.12 runtime.
- Wrote a custom `boto3` script to initialize an EC2 client and execute the `start_instances` command against a specific target EC2 Instance ID.
- Configured the function to return a 200 OK status and a JSON success message upon execution.

### 3. API Gateway Integration
- Configured an Amazon API Gateway (HTTP API) as the front-end trigger for the Lambda function.
- Set the endpoint security to 'Open' for immediate testing and accessibility.

### 4. Verification and API Output
- Invoked the API endpoint directly via a web browser.
- Successfully received the JSON response payload confirming execution.
- Verified in the EC2 Management Console that the target instance transitioned from a "Stopped" to a "Running" state.

## Proofs of Completion
- lambda_api_trigger.png: Screenshot of the Lambda console showing the API Gateway trigger configuration.
- api_browser_output.png: Screenshot of the browser window displaying the successful API response payload.
- ec2_starting.png: Screenshot of the EC2 console confirming the instance state change triggered by the automation.
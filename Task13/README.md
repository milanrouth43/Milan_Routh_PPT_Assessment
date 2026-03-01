# Task 13: Start/Stop EC2 using Lambda + API Gateway

## Objective
To implement serverless automation by creating a REST API that triggers a Lambda function to control (Start/Stop) an EC2 instance dynamically.

## Steps Taken
1. IAM Role: Created `Lambda_EC2_Control_Role` with `AmazonEC2FullAccess` to allow the function to manage instance states.
2. Lambda Function: Deployed a Python script using `boto3` that accepts query parameters (`?action=start` or `?action=stop`) to control the target instance.
3. API Gateway: Configured a REST API with a GET method integrated with the Lambda function (Proxy Integration enabled).
4. Deployment: Deployed the API to a `dev` stage and tested the Invoke URL to successfully toggle the instance state.

## Resources Used
* AWS Lambda (Python 3.9)
* Amazon API Gateway (REST API)
* Amazon EC2 (Target Instance)
* IAM Role (EC2 Access)

## Proofs
* API_Stop_Response.png: Screenshot of the browser response confirming the API call successfully triggered the "Stop" action.
* EC2_Stopped_Proof.png: Screenshot of the EC2 console verifying the instance actually stopped.
* API_Gateway_Dashboard.png: Screenshot of the API Gateway resource and method configuration.
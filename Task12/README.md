# Task 12: Website Down Alert using Lambda (Canary) + SNS

## Objective
To implement an automated monitoring system using a "Canary" approach. A Lambda function checks website availability and triggers an SNS email notification if the site is unreachable.

## Steps Taken
1. SNS Topic: Created a topic named `WebsiteDownAlert` and subscribed an email endpoint.
2. IAM Role: Configured `LambdaSNS_Canary_Role` with `AmazonSNSFullAccess` to allow publishing alerts.
3. Lambda Function: Deployed a Python script using `urllib3` to send HTTP requests to the target URL.
4. Logic: If the HTTP status is not 200 or the connection fails, the function publishes a message to the SNS topic.

## Resources Used
* AWS Lambda (Python 3.9)
* Amazon SNS (Standard Topic)
* IAM Role (Service Permissions)

## Proofs
* Lambda_Function_Code.png: Screenshot of the Python logic and execution logs showing the alert trigger.
* Email_Alert_Proof.png: Screenshot of the automated email received during the failure simulation.
* SNS_Topic_Config.png: Screenshot of the SNS topic with confirmed email subscription.
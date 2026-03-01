# Task 12: Website Down Alert using Lambda (Canary) + SNS

## Objective
The primary objective of this task is to understand automated monitoring and alerting mechanisms. This is achieved by configuring a serverless monitor to continuously verify website uptime and alert administrators during downtime.

## Implementation Steps

### 1. Notification System Configuration
- Created an Amazon SNS (Simple Notification Service) Standard Topic to handle alerts.
- Configured an Email subscription and successfully confirmed the endpoint to receive notifications.

### 2. Synthetics Canary Deployment
- Utilized AWS CloudWatch Synthetics to provision an automated Canary check.
- Used the "Heartbeat Monitoring" blueprint, which automatically deploys a Lambda function to simulate a user pinging the website endpoint.
- Configured the Canary to test the endpoint on a continuous 5-minute schedule.

### 3. Automated Alerting Integration
- Integrated a CloudWatch Alarm directly into the Canary deployment.
- Linked the alarm state to the SNS Topic created in step 1, ensuring that any failed health check immediately triggers an automated email notification to the administrator.

### 4. Validation and Testing
- Purposefully configured the Canary to monitor a non-existent URL to simulate a website outage.
- Verified the architecture by successfully capturing the failed Canary state in CloudWatch and receiving the automated SNS alert email.

## Proofs of Completion
- sns_subscription.png: Verification of the active SNS email subscription.
- canary_dashboard.png: CloudWatch console screenshot showing the active Canary check system.
- email_alert_received.png: Evidence of the automated CloudWatch alarm email successfully delivered to the inbox.
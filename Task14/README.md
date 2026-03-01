# Task 14: CloudWatch Alarm (70% CPU → Auto Stop + Email)

## Objective
To understand automated monitoring and resource management by configuring a CloudWatch alarm that triggers cost-saving and notification actions.

## Implementation Steps
1. Configured an Amazon SNS topic to handle email alerts for system thresholds.
2. Created a CloudWatch Metric Alarm monitoring the `CPUUtilization` of a target EC2 instance.
3. Defined a static threshold of 70% for the alarm trigger.
4. Integrated an EC2 Action to automatically "Stop" the instance when the threshold is breached to prevent resource wastage.
5. Linked the SNS notification to the alarm state to ensure immediate administrative visibility.

## Proofs of Completion
- cloudwatch_alarm_config.png: Screenshot of the alarm threshold and metric configuration.
- cloudwatch_actions.png: Screenshot confirming the automated Stop action and SNS notification settings.
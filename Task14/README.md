# Task 14: CloudWatch Alarm (High CPU → Auto Stop)

## Objective
To configure an automated monitoring and response system using Amazon CloudWatch. The goal is to detect high CPU usage (>70%) and automatically stop the instance to prevent resource exhaustion or cost overruns.

## Steps Taken
1. SNS Topic: Created `HighCPU_Alert` to send email notifications when the alarm triggers.
2. CloudWatch Alarm: Configured a metric alarm for `CPUUtilization` with a threshold of 70%.
3. EC2 Action: Added an automated action to "Stop this instance" when the alarm state is reached.
4. Stress Testing: Used the Linux `stress` tool (`stress --cpu 1`) to artificially spike CPU usage to 100%, successfully triggering the alarm and shutting down the server.

## Resources Used
* Amazon CloudWatch (Alarms & Metrics)
* Amazon EC2 (Action: Stop Instance)
* Amazon SNS (Email Notification)
* Linux Utility: `stress`

## Proofs
* Alarm_Triggered.png: Screenshot of the CloudWatch dashboard showing the alarm in the "ALARM" state due to high CPU.
* EC2_Auto_Stopped.png: Screenshot of the EC2 instance status changing to "Stopping" automatically after the alarm triggered.
* Email_Alarm_Notification.png: Screenshot of the email alert received from AWS SNS confirming the high CPU event.
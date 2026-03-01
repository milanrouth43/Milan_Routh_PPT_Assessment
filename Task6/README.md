# Task 6: S3 Replication and Lifecycle Policy

## Objective
To understand cost optimization and backup strategy by configuring cross-region replication and automated lifecycle rules in Amazon S3.

## Implementation Steps
1. Bucket Preparation: Created a Source bucket and a Destination bucket in different AWS Regions. Enabled Bucket Versioning on both buckets to support replication.
2. Replication Configuration: Created a Replication Rule  on the Source bucket targeting the Destination bucket. Configured AWS to automatically generate an IAM role with the necessary cross-bucket permissions.
3. Lifecycle Policy: Created a Lifecycle Rule [cite: 14, 15] on the Source bucket to optimize costs, automatically transitioning current versions of objects to the Standard-IA storage class after 30 days.

## Proofs
- versioning_enabled.png: AWS console screenshot showing Bucket Versioning enabled on the source bucket.
- replication_rule.png: AWS console screenshot showing the active Cross-Region Replication rule.
- lifecycle_rule.png: AWS console screenshot showing the active Lifecycle configuration rule.
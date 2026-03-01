# Task 9: Access S3 from Ubuntu using IAM Roles & Policies

## Objective
To learn role-based access control by securely accessing S3 from an EC2 instance without using long-term security credentials. 

## Implementation Steps
1. IAM Role Creation: Created an IAM Role named `EC2-S3-ReadOnly-Role` with the `AmazonS3ReadOnlyAccess` policy attached. 
2. Role Assignment: Modified the security settings of an existing Ubuntu EC2 instance to attach the newly created IAM Role. 
3. AWS CLI Verification: Connected to the Ubuntu instance and executed `aws s3 ls` to verify that the instance could successfully list S3 buckets using its assigned role permissions. 

## Proofs
- iam_role_attached.png: EC2 console screenshot showing the IAM Role successfully attached to the instance. 
- command_output : Terminal output showing the successful execution of the S3 list command.
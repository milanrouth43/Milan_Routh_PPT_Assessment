# Task 8: Create IAM Users and Groups

## Objective
To understand access control and security policies by managing users and permissions using AWS IAM.

## Implementation Steps
1. User Group Creation: Created an IAM group named `EC2-Admins` to manage collective permissions.
2. Policy Attachment: Attached the `AmazonEC2FullAccess` managed policy to the group, granting members full control over EC2 resources.
3. User Provisioning: Created an IAM user named `Student-User` with console access enabled.
4. Permission Assignment: Added the user to the `EC2-Admins` group, ensuring the user inherits the necessary permissions through group membership rather than direct attachment.

## Proofs
- iam_group_policy.png: AWS console screenshot showing the group and its attached policy.
- iam_user_list.png: AWS console screenshot showing the created user and their group membership.
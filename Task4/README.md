# Task 4: ASG and ELB in EC2

## Objective
To understand high availability and scaling concepts by configuring an Auto Scaling Group with a Load Balancer

## Implementation Steps
1. Launch Template Creation: - Created an EC2 Launch Template (`Task4-Template`) specifying the AMI, `t2.micro` instance type, key pair, and security group.
2. Load Balancer Setup (ELB): - Created a Target Group for HTTP traffic on port 80.
   - Deployed an Internet-facing Application Load Balancer (`Task4-ALB`) spanning multiple Availability Zones and routed its listener to the Target Group.
3. Auto Scaling Group (ASG) Configuration: - Created an ASG (`Task4-ASG`) using the previously created Launch Template.
   - Attached the ASG to the existing Load Balancer Target Group
   - Configured scaling policies with a Desired capacity of 2, Minimum of 1, and Maximum of 3 instances.

## Proofs
- launch_template.png: AWS console screenshot showing the configured Launch Template.
- load_balancer.png: AWS console screenshot showing the active Application Load Balancer.
- auto_scaling_group.png: AWS console screenshot showing the ASG successfully spinning up instances based on the desired capacity.
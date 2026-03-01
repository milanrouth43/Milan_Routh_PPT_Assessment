# Task 7: Create EFS and Connect to Multiple Ubuntu Instances

## Objective
To learn scalable file systems in AWS by mounting shared storage across multiple EC2 instances.

## Implementation Steps
1. EFS Creation: Created an Amazon Elastic File System (EFS) using the default VPC and ensured mount targets were available across all Availability Zones.
2. Security Configuration: Updated the VPC Security Group to allow inbound NFS traffic (Port 2049) so the EC2 instances could communicate with the EFS volume.
3. Instance Provisioning: Launched two identical Ubuntu EC2 instances in the same VPC.
4. Mounting & Verification: - Installed `nfs-common` on both instances.
   - Mounted the EFS file system to the `/mnt/efs` directory on both instances using the NFS client.
   - Created a test file on the first instance and successfully verified its immediate availability on the second instance, proving shared storage connectivity.

## Proofs
- efs_created.png: AWS console screenshot showing the active EFS volume and mount targets.
- ubuntu1_mount.png: Terminal screenshot of the first instance showing the successful mount command and file creation.
- ubuntu2_shared_file.png: Terminal screenshot of the second instance showing the successful mount command and visibility of the shared file.
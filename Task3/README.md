# Task 3: Attach EBS Volume from Different AZ using Snapshot

## Objective
To learn EBS snapshots and cross-AZ storage handling by migrating a volume between Availability Zones.

## Implementation Steps
1. Initial Volume & Snapshot: - Created a 1GB EBS volume in Availability Zone A (e.g., us-east-1a).
   - Created a snapshot of this volume to back up its state.
1. Cross-AZ Restoration: - Restored the snapshot to create a new EBS volume, explicitly selecting Availability Zone B (e.g., us-east-1b) during creation.
2. Attachment: - Launched a new EC2 instance specifically in Availability Zone B.
   - Attached the newly restored EBS volume to this EC2 instance.

## Proofs
- snapshot_creation.png: AWS console screenshot showing the completed EBS snapshot.
- cross_az_volume.png: AWS console screenshot showing the restored volume in the new Availability Zone.
- volume_attached.png: AWS console screenshot showing the volume successfully attached to the target EC2 instance.
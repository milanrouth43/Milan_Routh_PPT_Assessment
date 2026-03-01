# Task 2: Disk Partitioning (Ubuntu - MBR & Windows - GPT)

## Objective
To understand storage structure and disk management by implementing MBR partitioning on Linux and GPT partitioning on Windows.

## Implementation Steps
1. Volume Creation: Created 1GB EBS volumes in the same Availability Zone as the instances.
2. Linux Configuration (MBR):
   - Attached volume to Ubuntu EC2.
   - Used `fdisk` utility to create a Master Boot Record (MBR) partition.
   - Formatted with `ext4` filesystem and mounted to `/mnt/data`.
3. Windows Configuration (GPT):
   - Launched a Windows EC2 instance and attached a secondary volume.
   - Initialized the disk as GPT (GUID Partition Table) in Disk Management.
   - Created a 'New Simple Volume' and assigned a drive letter.

## Proofs
- ubuntu_partition.png: Terminal screenshot showing `lsblk` output with mounted partition.
- windows_partition.png: Windows Disk Management screenshot showing GPT volume status.

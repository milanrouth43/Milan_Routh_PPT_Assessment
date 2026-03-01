# Task 10: VPC 3-Tier Architecture

## Objective
To design and implement a highly available 3-tier network architecture. This task demonstrates proficiency in cloud networking, including public/private subnet segregation, NAT Gateway configuration for secure outbound traffic, and SSH tunneling for administrative access to private resources.

## Technical Components
- Virtual Private Cloud (VPC): A logically isolated section of the cloud network.
- Subnets: Segregated into Public (Web/Bastion) and Private (App/Database) tiers across multiple Availability Zones.
- Gateways: Internet Gateway (IGW) for public access and NAT Gateway for private subnet internet connectivity.
- Routing: Custom Route Tables to manage traffic flow between tiers and the internet.

## Detailed Implementation Steps

### 1. Networking Foundation
- Initiated the VPC Wizard to create a custom network CIDR block.
- Provisioned four subnets: two public subnets for external-facing resources and two private subnets for secure application workloads.
- Deployed an Internet Gateway and attached it to the VPC to enable external communication.

### 2. Connectivity and Security
- Configured a NAT Gateway in a public subnet to allow instances in the private subnets to download updates without being exposed to the public internet.
- Established Route Tables:
    - Public Route Table: Associated with public subnets with a 0.0.0.0/0 route pointing to the IGW.
    - Private Route Table: Associated with private subnets with a 0.0.0.0/0 route pointing to the NAT Gateway.
- Implemented Security Groups to act as virtual firewalls, restricting SSH access only to authorized IP ranges.

### 3. Architecture Validation
- Launched a Bastion Host in the public tier to act as a secure gateway.
- Launched an Application Server in the private tier with no public IP address.
- Performed an SSH tunnel (jump box method) to successfully connect from the local machine to the Bastion host, and finally to the private App Server.
- Verified internet connectivity on the private server via the NAT Gateway.

## Proofs of Completion
- vpc_resource_map.png: Visual representation of the VPC architecture, subnets, and routing connections.
- ssh_tunnel_verification.png: Terminal output showing successful multi-hop SSH access to the private subnet instance.
- network_config_details.txt: Summary of CIDR blocks, Subnet IDs, and Routing rules used in the architecture.
# Project 4: Secure EC2 Architecture

## Objective

Launch and secure EC2 instances in both public and private subnets using:

- Bastion Host
- SSH Key Pairs
- Security Groups

---

## Architecture Diagram

> *(Include Bastion Host in public subnet, and App Server in private subnet)*

---

## Setup Steps

1. Create:
   - Public Subnet (Bastion Host)
   - Private Subnet (App Server)

2. Launch EC2 Instances:
   - Bastion Host with SSH access (allow SSH from your IP)
   - App Server (only allow SSH from Bastion's private IP)

3. Configure SSH Agent Forwarding or ProxyCommand.

---

## Validation Steps

```bash
# Connect to Bastion Host
ssh -i my-key.pem ec2-user@<bastion-public-ip>

# From Bastion, connect to App Server
ssh -i my-key.pem ec2-user@<app-private-ip>

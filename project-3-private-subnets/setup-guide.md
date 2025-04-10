# Project 3: Private Subnets & Secure Routing

## Objective

Build a secure VPC setup using:

- Public & Private subnets
- NAT Gateway for secure internet access from private instances
- Route Tables and Internet Gateway

---


## Setup Steps

1. Create a VPC and two subnets:
   - `Public Subnet` (for NAT)
   - `Private Subnet` (for workload)

2. Create & attach an IGW to the VPC.

3. Launch NAT Gateway in the Public Subnet.

4. Configure Route Tables:
   - Public Subnet → route to IGW
   - Private Subnet → route to NAT Gateway

5. Launch EC2 instances in both subnets.

---

## Validation Steps

- SSH into public instance.
- Use it to SSH into private instance.
- From private instance, test internet:

```bash
curl https://aws.amazon.com

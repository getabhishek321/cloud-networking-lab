# Project 1: Basic VPC Setup

## Objective

Set up a foundational AWS Virtual Private Cloud (VPC) with the following components:

- 1 VPC (custom CIDR block)
- 2 Subnets (1 Public, 1 Private)
- Internet Gateway
- Route Table associated with the public subnet
- EC2 instance in the public subnet (used to verify connectivity)

---

## ⚙️ Step-by-Step Setup

### 1. Create a Custom VPC

```bash
aws ec2 create-vpc --cidr-block 10.0.0.0/16

# Project 2: VPC Traffic Flow & Security

## Objective

Understand and control how traffic moves within a VPC by implementing:

- Network ACLs (NACLs)
- Security Groups (SGs)
- Subnet-level traffic segmentation

---


## Setup Steps

### 1. Set Up Two Subnets

- Public Subnet A
- Public Subnet B (for testing traffic between subnets)

### 2. Launch Two EC2 Instances (one in each subnet)

- Use Amazon Linux 2
- Assign public IPs
- Allow SSH via SG on both instances

### 3. Configure Security Groups

- Allow inbound SSH (port 22)
- Allow ICMP for ping (type: Echo Request)

### 4. Create Custom NACLs

- Add **allow** rules for ports 22 and ICMP
- Deny specific ports (optional)

---

## Validation Steps

- SSH into one EC2
- Ping the other EC2’s private IP
- Experiment by denying ping in NACLs and observing results

---

## Key Takeaways

- NACLs work at the subnet level and are stateless.
- Security Groups work at the instance level and are stateful.
- Layered security = defense in depth.


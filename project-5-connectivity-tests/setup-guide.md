# Project 5: Connectivity & Testing

## Objective

Validate network connectivity and permissions using CLI tools and logs:

- `ping`, `curl`, `traceroute`
- SG & NACL testing
- Network troubleshooting basics

---

## Architecture Diagram

> *(Visual showing two EC2 instances in different subnets and tools used)*

---

## Setup Steps

1. Deploy EC2s in public and private subnets.

2. Allow ICMP, HTTP, HTTPS in SGs and NACLs (as needed).

3. Test access:
```bash
ping <private-ip>
curl https://google.com
traceroute <public-ip>

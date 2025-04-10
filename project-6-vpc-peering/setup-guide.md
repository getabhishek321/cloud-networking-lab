
# Project 6: VPC Peering for Cross-VPC Communication

## Objective

Connect two VPCs securely using VPC Peering and configure routing between them.

---

## Setup Steps

1. Create two VPCs (e.g., `10.0.0.0/16` and `10.1.0.0/16`)

2. Launch one EC2 in each VPC.

3. Create a VPC Peering Connection:
   - Initiate from one VPC
   - Accept in the other

4. Update Route Tables in **both** VPCs to allow traffic.

5. Allow ICMP or SSH in SGs.

---

## Validation Steps

- SSH or ping from EC2-A (VPC1) to EC2-B (VPC2)
- Test bidirectional traffic

---

## Key Takeaways

- VPC Peering is non-transitive.
- Route Tables must be manually updated.
- Works best for intra-region communication.

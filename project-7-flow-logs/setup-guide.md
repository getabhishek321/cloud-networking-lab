# Project 7: Network Visibility with Flow Logs & CloudWatch

## Objective

Enable and analyze VPC Flow Logs to monitor traffic patterns and security events.

---

## Setup Steps

1. Go to VPC → Flow Logs → Create Flow Log.

2. Choose:
   - Resource: VPC / Subnet / ENI
   - Destination: CloudWatch Logs (create log group)
   - Format: Use default

3. Launch an EC2 and generate some traffic.

---

## Validation Steps

- Go to CloudWatch → Logs → View Log Group
- Use **Log Insights** to run queries like:

```sql
fields srcAddr, dstAddr, action, protocol
| sort @timestamp desc
| limit 19

# Security Configuration Matrix

## Instance Details
- Instance ID: i-079a97faf5faecfe8
- Instance Type: t3.micro
- Public IP: 35.158.103.164
- Private IP: 172.31.6.162

## Security Group: week2-web-server-sg

### Inbound Rules
| Protocol | Port | Source | Purpose | Risk Level |
|----------|------|--------|---------|------------|
| TCP | 22 | 178.6.50.50/32 | SSH administrative access | Low (restricted IP) |
| TCP | 80 | 0.0.0.0/0 | Public web traffic (HTTP) | Low (expected) |

### Outbound Rules
| Protocol | Port | Destination | Purpose |
|----------|------|-------------|---------|
| All | All | 0.0.0.0/0 | Unrestricted outbound traffic |

## Security Assessment
- ✅ SSH access is restricted to a single trusted IP address
- ✅ No unnecessary inbound ports are open
- ✅ HTTP access is enabled for web server functionality
- ⚠️ Outbound traffic is unrestricted and could be limited for higher security

## Security Testing Summary
- SSH connection from allowed IP: Successful
- HTTP access on port 80: HTTP 200 OK
- ICMP (ping): Blocked as expected
- MySQL port (3306): Blocked as expected

## Recommendations
1. Enable monitoring and alerts for SSH access attempts
2. Consider using AWS Session Manager instead of direct SSH
3. Enable VPC Flow Logs for additional network visibility

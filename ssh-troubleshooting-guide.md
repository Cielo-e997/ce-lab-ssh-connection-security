# SSH Connection Troubleshooting Guide

## Common SSH Problems

### 1. Permission denied (publickey)
**Possible causes:**
- Wrong private key
- Wrong username
- Key file permissions are too open

**Checks:**
```bash
ls -l ~/.ssh/bootcamp-week2-key.pem
ssh -i ~/.ssh/bootcamp-week2-key.pem ec2-user@YOUR_PUBLIC_IP
ssh -vvv bootcamp-web

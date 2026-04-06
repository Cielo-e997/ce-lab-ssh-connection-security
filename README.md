# Lab M2.02 - SSH Connection and Security Best Practices

## SSH Configuration
Configured SSH using `~/.ssh/config` to connect with an alias instead of typing the full command.

Command used:
ssh bootcamp-web

---

## Security Group Testing

Tested different access scenarios:

- SSH (port 22) → allowed only from my IP → SUCCESS
- HTTP (port 80) → open to public → SUCCESS (HTTP 200 OK)
- ICMP (ping) → blocked → EXPECTED
- Port 3306 → blocked → EXPECTED

Results are documented in:
- security-test-results.txt

---

## SCP File Transfer

Tested file transfer using SCP:

- Local → EC2
- EC2 → Local
- Directory transfer

Commands and results:
- file-transfer-log.txt

---

## SSH Security Audit

Verified SSH configuration on the instance:

- PasswordAuthentication → disabled
- PermitRootLogin → disabled
- PubkeyAuthentication → enabled

See:
- ssh-config-audit.txt

---

## Security Configuration

Full security setup documented in:
- security-matrix.md

Includes:
- inbound rules
- outbound rules
- risk analysis

---

## Troubleshooting

Common issues encountered:

- Permission denied → fixed by correcting key permissions
- Connection timeout → fixed by checking security group rules
- Host key verification error → fixed using ssh-keygen -R

See:
- ssh-troubleshooting-guide.md

---

## Screenshots

The screenshots/ folder contains:

- SSH connection using alias
- Security tests (curl, ping, port checks)
- SCP file transfer

---

## Conclusion

This lab demonstrates secure SSH access, validation of security group rules, file transfer using SCP, and basic troubleshooting of SSH connectivity issues.
# Detection: Unauthorized Local Admin User Creation

## 🔧 Attack Simulated
Used the `net.exe` command-line tool to create a new local user and added it to the local Administrators group.

### Commands Run:
```cmd
net user eviluser P@ssw0rd123! /add
net localgroup administrators eviluser /add

🔍 Sysmon Events Observed

Event ID 1 – Process Creation
Image: C:\Windows\System32\net.exe

CommandLine:

net user eviluser P@ssw0rd123! /add

net localgroup administrators eviluser /add

User: Administrator

Hashes: Available in Event details

Event ID 13 – Registry Value Set (Optional)
If group membership modified via registry

🧠 Analyst Notes

Creating new local administrator accounts is a common persistence technique used by attackers. This can be detected by monitoring for suspicious uses of net.exe, especially involving Administrators.


🧩 MITRE ATT&CK Mapping
T1136.001: Create Account – Local Account

T1078: Valid Accounts

T1098: Account Manipulation

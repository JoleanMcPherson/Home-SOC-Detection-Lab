# 🧠 Detection Reports

This folder contains detailed detection reports based on attacker simulation exercises performed in my Home SOC Detection Lab.

Each report documents:
- A simulated attack technique (e.g. PowerShell abuse, privilege escalation, LOLBins)
- The commands used to simulate the behavior
- Sysmon logs and Event IDs triggered by the activity
- Detection insights and investigation notes
- Mapped MITRE ATT&CK techniques

These reports are written in Markdown to demonstrate my ability to:
- Perform hands-on detection engineering
- Analyze log data using Sysmon
- Document findings clearly for security teams or reporting
- Align detections with common attacker tactics and procedures

---

## 📁 Current Reports

| File | Description |
|------|-------------|
| `new-admin-user-detection.md` | Detects unauthorized creation of a local administrator account via `net.exe` |
| `powershell-download-detection.md` | Detects use of PowerShell to download external files using `Invoke-WebRequest` |
| `suspicious-exe-detection.md` | Detects renamed LOLBin (`PsExec.exe` → `evil.exe`) executed to simulate malware |

---

## 🛣️ Coming Soon

Planned detections:
- Scheduled task abuse
- Obfuscated PowerShell commands
- Registry persistence
- Lateral movement (e.g. SMB, WMI)
- SIEM rule equivalents for these detections

---

📌 This folder is a key part of my detection engineering portfolio and demonstrates my growing capability to recognize malicious behavior from system logs and respond like a SOC analyst.

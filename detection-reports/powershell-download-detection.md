# Detection: PowerShell File Download via Invoke-WebRequest

## 🔧 Attack Simulated
Used PowerShell to download a file from the internet — mimicking an attacker retrieving a payload.

### Command Run:
```powershell
powershell -Command "Invoke-WebRequest https://raw.githubusercontent.com/MicrosoftDocs/windowsserverdocs/main/WindowsServerDocs/storage/images/StorageSpacesDirect_DeploymentScenarios.png -OutFile C:\Users\Administrator\Downloads\payload.png"
```
## 🔍 Sysmon Events Observed

### Event ID 1 – Process Creation
Image: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe

CommandLine: Invoke-WebRequest with -OutFile argument

ParentImage: Usually explorer.exe or cmd.exe

Hashes: Available in Event details

## 🧠 Analyst Notes

PowerShell is often used in fileless attacks and to fetch malicious payloads. Monitoring PowerShell command-line usage is a critical detection method for early-stage threat activity.

In real-world environments, look for:

URLs from unknown or non-whitelisted domains

Use of encoded commands or obfuscation

## 🧩 MITRE ATT&CK Mapping
T1059.001: Command and Scripting Interpreter – PowerShell

T1105: Ingress Tool Transfer

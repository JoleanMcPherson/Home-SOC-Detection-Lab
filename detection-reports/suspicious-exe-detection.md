# Detection: Suspicious Executable Run (PsExec Renamed)

## Attack Simulated
Downloaded PsExec from Sysinternals and renamed it to `evil.exe` to simulate attacker behavior.

## Sysmon Events Observed
- **Event ID 1**: Process Creation
- Image: `C:\Users\Administrator\Downloads\PsTools\evil.exe`
- OriginalFileName: `PsExec.exe`
- Hashes: SHA256 observed
- CommandLine: `evil.exe`

## Analyst Notes
Renaming known tools is a common attacker technique to bypass name-based detection. Sysmon's hashing and original filename features help detect this.

## MITRE Mapping
- **T1218.011**: Signed Binary Proxy Execution: PsExec
- **T1036.003**: Masquerading: Rename System Utilities

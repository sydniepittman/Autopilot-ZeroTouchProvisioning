# Phase 3: Hardware Hash Capture

Windows Autopilot recognizes a device using a hardware hash (a fingerprint derived from firmware and TPM attestation data). 

## Script

Run from an elevated PowerShell session on the target device:

```powershell
Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Force
Install-Script -Name Get-WindowsAutoPilotInfo -Force
Get-WindowsAutoPilotInfo.ps1 -OutputFile C:\HWID.csv
```
Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Force: temporarily lifts PowerShell's default script-blocking restriction so the downloaded script is allowed to run.
Install-Script -Name Get-WindowsAutoPilotInfo -Force: downloads the `Get-WindowsAutoPilotInfo` community script from the PowerShell Gallery.
Get-WindowsAutoPilotInfo.ps1 -OutputFile C:\HWID.csv:runs the script, querying the device's firmware/TPM to generate the hash and writing the result to a CSV formatted for direct Intune import.

## Output

`HWID.csv` contains three fields:

| Field | Description |
|---|---|
| Device Serial Number | Hardware serial (VirtualBox-generated for a VM) |
| Windows Product ID | Tied to the current OS install (legacy field) |
| Hardware Hash | The base64-encoded fingerprint Intune uses to recognize the device |

<img width="1213" height="389" alt="Hardware Hash capture " src="https://github.com/user-attachments/assets/d6b03599-c9b0-4bc7-9c21-31c561589a58" />
<img width="503" height="53" alt="ScriptVerification (1)" src="https://github.com/user-attachments/assets/058c218b-4dba-4850-8689-709d1f56fcdb" />



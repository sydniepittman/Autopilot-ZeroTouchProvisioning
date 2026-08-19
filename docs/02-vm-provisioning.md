# Phase 2: VM Provisioning

This project uses a separate, purpose-built VM rather than reusing an existing domain-joined machine, for two reasons: it keeps this project's state clean for documentation, and Autopilot requires the device to have real internet reachability throughout provisioning.

## VM Configuration

| Setting | Value | Why |
|---|---|---|
| OS | Windows 11 Enterprise | Autopilot/Entra join requires Pro, Enterprise, or Education, not Home |
| Network Adapter | NAT (or Bridged) | Needs outbound internet access to reach Entra ID/Intune cloud endpoints |
| Firmware | EFI enabled | Required for Windows 11 |
| Secure Boot | Enabled | Windows 11 hardware requirement |
| TPM | 2.0 | Required for the hardware hash generation in Phase 3 |

"C:\Users\Sydni\OneDrive\Desktop\AD Projects\Autopilot\VMConfig.jpg"

## Installation

Installed from the official Windows 11 Enterprise evaluation ISO. 

"C:\Users\Sydni\OneDrive\Desktop\AD Projects\ServerInstall.png"



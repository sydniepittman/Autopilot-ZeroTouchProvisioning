# Windows Autopilot / Intune Zero-Touch Provisioning Lab

A demonstration of using Windows Autopilot device registration and zero-touch provisioning through Microsoft Intune in VirtualBox.

## Project Summary

The purpose of this lab is to simulate the real-world process an IT department follows to provision a new employee laptop without physically touching the hardware: registering a device's hardware identity in advance, building a deployment profile, and validating the full out-of-box enrollment experience end to end.

**Stack:** VirtualBox · Windows 11 Enterprise · Microsoft Intune (trial) · Microsoft Entra ID · Microsoft 365 Business Premium (trial)

## Skills Demonstrated

- Cloud identity fundamentals (Microsoft Entra ID, tenants, licensing)
- Mobile Device Management / Unified Endpoint Management (Intune)
- Windows Autopilot device registration and hardware attestation (TPM)
- Deployment profile configuration (Entra ID join, OOBE customization)
- Group-based policy assignment
- End-to-end enrollment validation

## Architecture

```
[VirtualBox VM: Windows 11 Enterprise]
        |
        | NAT adapter (internet-facing — required for cloud enrollment)
        v
[Microsoft Entra ID tenant] <---> [Microsoft Intune]
        |                              |
   Device identity              Deployment profile,
   (Entra join)                 compliance policy,
                                 app assignment
```

## Walkthrough

| Phase | Description |
|---|---|
| [01 - Tenant & Licensing Setup](docs/01-tenant-setup.md) | Standing up a Microsoft 365 tenant and licensing Intune |
| [02 - VM Provisioning](docs/02-vm-provisioning.md) | Building the test device in VirtualBox |
| [03 - Hardware Hash Capture](docs/03-hash-capture.md) | Generating the device's Autopilot identity |
| [04 - Intune Device Import](docs/04-device-import.md) | Registering the device with the Autopilot service |
| [05 - Deployment Profile](docs/05-deployment-profile.md) | Configuring the provisioning experience |
| [06 - Group Assignment](docs/06-group-assignment.md) | Targeting the profile to the device |
| [07 - OOBE Enrollment](docs/07-oobe-enrollment.md) | Validating the full zero-touch enrollment flow |

## Prerequisites

- VirtualBox 7.x (with EFI/TPM 2.0/Secure Boot support)
- Windows 11 Enterprise ISO
- A Microsoft 365 tenant with Intune licensing 



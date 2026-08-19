# Phase 4: Intune Device Import

This phase registers the device's identity with the Windows Autopilot Deployment Service so it can be recognized the next time this hardware boots to OOBE.

## Getting the file off the VM

Installed via Devices → Insert Guest Additions CD image, then ran the installer from inside the guest and rebooted.
Configured a shared folder, which exposed a host directory inside the guest as `\\VBOXSVR\<foldername>` — used to copy `HWID.csv` out to the host.

## Import steps

1. [intune.microsoft.com](https://intune.microsoft.com) → Devices → Windows → Windows enrollment.
2. Under Windows Autopilot Deployment Program** → **Devices → Import.
3. Uploaded `HWID.csv`.
4. Waited for backend processing, then clicked "Sync" to pull the registration into the visible list.

## Result

Device appeared in the **Windows Autopilot devices** list:

| Field | Value |
|---|---|
| Serial number | `VirtualBox-7702897d-8...` |
| Manufacturer | innotek GmbH *(VirtualBox's original developer pre-Oracle acquisition — a permanent artifact in its virtual BIOS)* |
| Model | VirtualBox |
| Group tag | *(blank — not used in this project; see notes below)* |
| Profile status | Not assigned |

<img width="904" height="529" alt="SyncComplete" src="https://github.com/user-attachments/assets/52e086ae-4f16-403b-8aff-bec13dcdc4d0" />




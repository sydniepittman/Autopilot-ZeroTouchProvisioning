# Phase 6: Group Assignment

Intune targets policy at groups not indivudals, creating security groups allows for scalabitly later and more efficiency when provisioning new devices.

## Step 1: Create the group

entra.microsoft.com → Identity → Groups → All groups → New group

| Setting | Value |
|---|---|
| Group type | Security  |
| Name | Autopilot-Lab-Devices |
| Membership type | Assigned  |
| Members | The Autopilot-registered device, added manually |

"C:\Users\Sydni\OneDrive\Desktop\AD Projects\Autopilot\AutopilotLabDevicesMembers.jpg"

## Step 2: Assign the deployment profile

Intune → Deployment Profiles → Homelab_Autopilot_Demo → Assignments → Include → Autopilot-Lab-Devices → Save

## Result

<img width="1578" height="810" alt="DeploymentProfileAssigned" src="https://github.com/user-attachments/assets/f5b8d4b5-3944-4d33-ae43-c5127df5fa23" />


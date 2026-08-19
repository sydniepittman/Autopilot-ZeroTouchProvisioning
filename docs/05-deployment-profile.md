# Phase 5: Deployment Profile

Setting up the deployment profile to define what kind of identity the device establishes and what the setup experience looks like for the end user.

## Navigation

Devices -> Windows -> Windows enrollment -> Deployment Profiles -> Create profile -> Windows PC

## Configuration

| Setting | Value 
|---|---|---|
| Name | `Homelab_Autopilot_Demo` 
| Description | Cloud native, user driven profile for lab testing |
| Deployment mode | User-driven 
| Join type | Microsoft Entra joined
| License Terms | Hide 
| Privacy settings | Hide 
| Hide change account options | Yes 
| User account type | Standard
| White Glove | No 

## Result

Profile created and visible under Windows Autopilot deployment profiles:

| Name | Join type | Assigned |
|---|---|---|
| Homelab_Autopilot_Demo | Microsoft Entra joined | No |


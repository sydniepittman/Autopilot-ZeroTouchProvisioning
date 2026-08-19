# Phase 7: OOBE Enrollment — end-to-end validation

## The reset

Returning the VM to a first-boot OOBE state after allowing time for the deplyment profile assignment to propagate.


"C:\Users\Sydni\OneDrive\Desktop\AD Projects\Autopilot\HelloPrompt.png"

## Result

Landed at a fully configured desktop:

| Field | Value |
|---|---|
| Device name | `LAB-25391a8a181` |
| Signed in as | Organizational account (not a personal Microsoft account) |
| Network | Connected |
| Windows Update | Up to date |

"C:\Users\Sydni\OneDrive\Desktop\AD Projects\Autopilot\SystemInfo.png"

"C:\Users\Sydni\OneDrive\Desktop\AD Projects\Autopilot\EntraJoined.jpg"

## Summary of the full chain

```
Hardware hash captured (Phase 3)
   -> Registered with Autopilot service (Phase 4)
   -> Deployment profile configured (Phase 5)
   -> Assigned via group targeting (Phase 6)
   -> Recognized at OOBE, Entra joined, silently MDM-enrolled (Phase 7)
   -> Fully managed, policy-compliant desktop
```



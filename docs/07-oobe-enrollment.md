# Phase 7: OOBE Enrollment — end-to-end validation

## The reset

Returning the VM to a first-boot OOBE state after allowing time for the deplyment profile assignment to propagate.


<img width="1034" height="769" alt="HelloPrompt" src="https://github.com/user-attachments/assets/b3027603-b4ee-41ca-80fa-00bf4770a00d" />

## Result

Landed at a fully configured desktop:

| Field | Value |
|---|---|
| Device name | `LAB-25391a8a181` |
| Signed in as | Organizational account (not a personal Microsoft account) |
| Network | Connected |
| Windows Update | Up to date |

<img width="1031" height="762" alt="SystemInfo" src="https://github.com/user-attachments/assets/7306dbe9-bf6a-4b98-87f2-ab62142bcce9" />

<img width="1547" height="479" alt="EntraJoined" src="https://github.com/user-attachments/assets/572b33c9-42d4-4544-b9e2-058d777f787d" />

## Summary of the full chain

```
Hardware hash captured (Phase 3)
   -> Registered with Autopilot service (Phase 4)
   -> Deployment profile configured (Phase 5)
   -> Assigned via group targeting (Phase 6)
   -> Recognized at OOBE, Entra joined, silently MDM-enrolled (Phase 7)
   -> Fully managed, policy-compliant desktop
```


